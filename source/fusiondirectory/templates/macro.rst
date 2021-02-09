.. include:: /globals.rst

.. _fd-macros-label:

Macros 
======

You can use macros to automate the creation of attributes based on rules inside the templates. They can also be used in trigger definitions.

How to use a macro
------------------

A macro is enclosed in % and contains an LDAP attribute name. 
It may optionnaly states modifiers to apply to the attribute, followed by a | between modifiers and the attribute name.
Some modifiers accepts parameters enclosed in [] and separated by commas.
Modifiers are applied from left to right.

.. code-block:: bash

   %sn%           The value of "Last name" field, entered during account creation.

There are some special variables which may also be used instead of an LDAP attribute name, most of them are specific to triggers (see :ref:`triggers-special-variables`), but the following ones are also available to templates:

* **%callerDN%** gives the DN of the author of the modification
* **%callerCN%** gives the CN of the author of the modification
* **%callerUID%** gives the UID of the author of the modification
* **%callerSN%** gives the SN of the author of the modification
* **%callerGIVENNAME%** gives the GIVENNAME of the author of the modification

Some modifiers do not even require an LDAP attribute name as they generate a value on their own, such as **r** or **d**.
   
Modifiers
---------

**a**

The **a** modifier can be used to remove accents, in one of two modes:

* ascii (default): In this mode accents and non-ascii characters are removed.
* uid: In this mode accents and all invalid characters for an uid value are removed. if **Strict naming policy** is **on** in the configuration, this will also convert to lowercase.

Examples: 



.. code-block:: shell

   %a|sn%           "Last name" field returned unaccented.
                     If "sn=Valérie" then the returned value is "Valerie"
   %a[uid]|sn%      "Last name" field returned as valid uid.
                     If "sn=Poivre D'Arvor" then the returned value is "poivredarvor"
                     
**b**

The **b** modifier can be used to convert to base64.

**c**

The **c** modifier can be used to put a comment. An example :                      


.. code-block:: bash

   %c|this is just a comment%           returns an empty string. 
                     
                     

It can also be used to make a template uid unique when 2 templates have the same uid pattern:                      


.. code-block:: bash

   %al|sn%%c|template1%
   %al|sn%%c|template2%
   
   
**d**

The **d** modifier can be used to generate dates and times.

* First parameter is date string (defaults to “now”)
* Second one is date format (defaults to “d.m.Y”, to be used in date fields).

Examples:    


.. code-block:: bash

   %d|%                              15.03.2017
   %d[tomorrow]|%                    16.03.2017
   %d[today+6days]|%                 21.03.2017
   %d[now,l jS \of F Y h:i:s A]|%    Wednesday 15th of March 2017 02:12:18 PM
   
as POSIX date fields expects a specific format you need to add 'epoch' as second parameter to the d modifier.

.. code-block:: bash

   %d[today+30days,epoch]|%                 15.04.2017
   
**e**

The modifier **e** can be used to generate incremental numbers.
As the **r**, **d** and **n** modifiers it should be used alone, with no attribute name.

This modifier will add an incremental number to the value. The number will be incremented relative to the last generated value.
It does not check or ensure unicity by itself. It does not ensure that values will be contiguous, as an incremented value may happen in a template usage that fails in the end.

* First parameter is an id to reference this incremental number. Several masks sharing this id will share the value pool.
* Second parameter is starting number, defaults to 1.
* Third parameter is step, defaults to 1.

Examples:

.. code-block:: bash

   %e[employeeNumber]|%     Number starting at 1
   %e[twoDigitsNumber,10]|% Number starting at 10
   %e[evenNumber,0,2]|%     Number starting at 0 and going 2 by 2
   
   

**i**

The **i** modifier can be used to have the first letter of a word in capital letters and the rest in lower case letters.


Examples:    


.. code-block:: bash

   %i|sn% if our sn is "MY LAST NAME" we will have "My Last Name" in description.
   
We do not allow element to be transformed by itself.

Example : we cannot do %i|sn% in %sn% because it would make a loop.

If we try it we will have this kind of error 


.. code-block:: bash

   Recursive dependency in the template fields: "givenName" cannot depend on "givenName" as "givenName" already depends on "givenName".
      
   
**l**

The **l** modifier can be used to return the lowercase version of the parameter.    


.. code-block:: bash

   %l|sn%           "Last name" field returned in lowercase. 
                     If "sn=Valérie" then the returned value is "valérie"
                     
**n**

The modifier **n** can be used to generate numbers.
As the **r** and **d** modifiers it should be used alone, with no attribute name.

This modifier will make sure the result value is unique for the filled field in the LDAP. The number will get as high as needed to ensure that.

* First parameter is whether the number should always be there or only in case of duplicates (1 or 0, defaults to 0).
* Second parameter is starting number, defaults to 1.
* Third parameter is step, defaults to 1.

Examples:

.. code-block:: bash

   %n|%           If not unique, adds a number starting at 1
   %n[1]|%        A number starting at 1
   %n[0, 2]|%     If not unique, adds a number starting at 2
   %n[1,10]|%     A number starting at 10
   %n[1,20,10]|%  A number starting at 20 and going up ten by ten

**p**

The **p** modifier can be used to remove whitespaces. It can also be used for any search and replace based on preg_replace. 

For this provide 2 arguments
 
* first one is regexp
* second one is replacement string. 

Default values are /\s/ and empty string, to remove all whitespaces as in previous behavior.

Examples:    


.. code-block:: bash

   %p|sn%           "Last name" field, without whitespaces. "O Connor" becomes "OConnor".
   %p[/\s/,-]|sn%   "Last name" field, with whitespaces replaced by dashes. "O Connor" becomes "O-Connor".
   
   
**r**

The **r** modifier can be used to generate random strings, for instance for passwords.

It can take up to three arguments

* min length
* max length
* character type.

Third argument should be either 

* **l** for letters
* **d** for digits 
* **b** for both. 

Default is both.

The default length is 8 and if there is only one argument it will be used as a fixed length.

Examples:    


.. code-block:: bash

   %r[6,10]|%       a random string with a random length between 6 and 10 chars containing both letters and digits
   %r|%             a random string of length 8
   %r[12]|%         a random string of length 12
   %r[5,10,d]|%     a random string of a random length between 5 and 10 containing only digits
   
   
**s**

The **s** modifier can be used to generate substrings.

Examples:    


.. code-block:: bash

   %s[1,3]|sn%           a substring of "Last name" field, taking 3 characters and starting at position 1.
   %s[0,1]|sn%           the first character of "Last name" field.
   %s[1]|sn%             the first character of "Last name" field (short syntax).
   %s[5]|sn%             a substring of "Last name" field, taking 5 first characters.
   %s[2,4-8]|sn%         a substring of "Last name" field, taking minimum 4 characters (more if needed for unicity) 
                         and starting at position 2.
   %s[4-8]|sn%           a substring of "Last name" field, taking minimum 4 characters (more if needed for unicity).
   %s[-5,2]|sn%          a substring of "Last name" field, taking 2 characters and starting 5 characters from the end.
   %s[-5,5]|sn%          a substring of "Last name" field, taking the last 5 characters.
   
   
**t**

The **t** modifier can be used to return the transliterated version of the parameter. The parameters are the list of locales to use for transliteration (first one will be used by non-interactive uses of the template).

Examples:    


.. code-block:: bash

   %t[de_DE]|sn%           "Last name" field returned transliterated.
                           If "sn=Süßkartoffel" then the returned value is "Suesskartoffel"
                           
                           
Note that the locale used must be installed on the server (and web server needs to be restarted after locale installation). 

.. _array-modifiers:

Array modifiers
---------------

Array modifiers are used for multivaluated LDAP attributes and are represented as uppercase letters. If no array modifier is used on a multivaluated attribute, the "first" value is used.

**C**

The **C** modifier (added in version 1.0.10) returns the count of values in the attribute. It can be 0.                            


.. code-block:: bash

   %C|arrayAttribute%           returns the number of values in arrayAttribute
   
   
**F**

The **F** modifier returns the first value of the array


**J**

The **J** modifier returns the values joined together. It takes the separator as parameter. 


.. code-block:: bash

   %J[:]|arrayAttribute%           returns the values joined and separated by : character
   

**L**

The **L** modifier returns the last value of the array

**M**

The **M** modifier returns values that matches the regular expression passed as parameter. As it returns an array, an other modifier is usually used after such as J or C.

.. code-block:: bash

   %M[/a$/]C|arrayAttribute%           returns the number of values ending with the letter a

Combining examples
------------------


.. code-block:: bash

   %al|sn%           "Last name" field returned in lowercase unaccented. 
                      If "sn=Valérie" then the returned value is "valerie"


.. code-block:: bash

   %au|sn%           "Last name" field returned in uppercase unaccented. 
                      If "sn=Valérie" then the returned value is "VALERIE"                      


.. code-block:: bash

   %alp|sn%          "Last name" field returned in lowercase unaccented without whitespaces. 
                      If "sn=Valérie DUPONT" then the returned value is "valeriedupont"


.. code-block:: bash

   %us[0,4]|sn%      a substring of "Last name" field, taking 4 characters, starting at position 0 and converting in uppercase. 
                     If "sn=Valérie" then the returned value is "VALÉ".           


.. code-block:: bash

   %ls[1,4]|sn%      a substring of "Last name" field, taking 4 characters, starting at position 1 and converting in lowercase. 
                     If "sn=Valérie" then the returned value is "alér".          


.. code-block:: bash

   %las[4]|sn%     a substring of "Last name" field, taking the first 4 characters and converting in unaccented lowercase. 
                   If "sn=Valérie" then the returned value is "vale".                                                                


.. code-block:: bash

   %r[8,8,l]u|%     a random string of length 8, containing uppercase letters.
