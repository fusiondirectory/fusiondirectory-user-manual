.. include:: /globals.rst

.. _fd-macros-label:

Macros 
======

You can use macros to automate the creation of attributes based on rules inside the templates.

* How to use a macro

macro must always be enclosed in %. 


.. code-block:: bash

   %sn%           The value of "Last name" field, entered during account creation.
   
   
* Macros

**a**

The **a** macro can be used to return the unaccented version of the parameter.

Examples: 



.. code-block:: shell

   %a|sn%           "Last name" field returned in unaccented. 
                     If "sn=Valérie" then the returned value is "Valerie"
                     
**b**

The **b** macro can be used to convert to base64.

**c**

The **c** macro can be used to put a comment. An example :                      


.. code-block:: bash

   %c|this is just a comment%           returns an empty string. 
                     
                     

It can also be used to make a template uid unique when 2 templates have the same uid pattern:                      


.. code-block:: bash

   %al|sn%%c|template1%
   %al|sn%%c|template2%
   
   
**d**

The **d** macro can be used to generate dates and times.

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
   
   
   
**i**

The **i** macro can be used to have the first letter of a word in capital letters and the rest in lower case letters.


Examples:    


.. code-block:: bash

   %i|sn% if our sn is "MY LAST NAME" we will have "My Last Name" in description.
   
We do not allow element to be transformed by itself.

Example : we cannot do %i|sn% in %sn% because it would make a loop.

If we try it we will have this kind of error 


.. code-block:: bash

   Recursive dependency in the template fields: "givenName" cannot depend on "givenName" as "givenName" already depends on "givenName".
      
   
**l**

The **l** macro can be used to return the lowercase version of the parameter.    


.. code-block:: bash

   %l|sn%           "Last name" field returned in lowercase. 
                     If "sn=Valérie" then the returned value is "valérie"
                     
                     
**p**

The **p** macro can be used to remove whitespaces. It can also be used for any search and replace based on preg_replace. 

For this provide 2 arguments
 
* first one is regexp
* second one is replacement string. 

Default values are /\s/ and empty string, to remove all whitespaces as in previous behavior.

Examples:    


.. code-block:: bash

   %p|sn%           "Last name" field, without whitespaces. "O Connor" becomes "OConnor".
   %p[/\s/,-]|sn%   "Last name" field, with whitespaces replaced by dashes. "O Connor" becomes "O-Connor".
   
   
**r**

The **r** macro can be used to generate random strings, for instance for passwords.

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

The **s** macro can be used to generate substrings.

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

The **t** macro can be used to return the transliterated version of the parameter. The parameters are the list of locales to use for transliteration (first one will be used by non-interactive uses of the template).

Examples:    


.. code-block:: bash

   %t[de_DE]|sn%           "Last name" field returned transliterated.
                           If "sn=Süßkartoffel" then the returned value is "Suesskartoffel"
                           
                           
Note that the locale used must be installed on the server (and web server needs to be restarted after locale installation). 


* Array macro

**C**

The **C** macro (added in version 1.0.10) returns the count of values in the attribute. It can be 0.                            


.. code-block:: bash

   %C|arrayAttribute%           returns the number of values in arrayAttribute
   
   
**F**

The **F** macro returns the first value of the array


**J**

The **J** macro returns the values joined together. It takes the separator as parameter. 


.. code-block:: bash

   %J[:]|arrayAttribute%           returns the values joined and separated by : character
   

**L**

The **L** macro returns the last value of the array


* Combining examples


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
