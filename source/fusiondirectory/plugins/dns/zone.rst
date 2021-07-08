.. include:: /globals.rst

Zone
----

A DNS zone with all the records it contains.

  .. image:: images/dns-zone.png
     :alt: Edition of a DNS Zone object

Zone
^^^^

.. image:: images/dnszone-dnszone-main.png
   :alt: Screenshot of section Zone of tab DNS zone of type DNS zone

* Base: Object base
* Zone name: Zone name
* Reverse zones: Reverse zones for this zone in the form xx.xx.in-addr.arpa. or x.x.ip6.arpa.

SOA record
^^^^^^^^^^

.. image:: images/dnszone-dnszone-soa.png
   :alt: Screenshot of section SOA record of tab DNS zone of type DNS zone

* Primary DNS server: Domain name of the name server that was the original or primary source of data for this zone
* Mail address: Domain name which specifies the mailbox of the person responsible for this zone
* Serial number: Version number of the original copy of the zone
* Refresh: Time interval before the zone should be refreshed
* Retry: Time interval that should elapse before a failed refresh should be retried
* Expire: Time value that specifies the upper limit on the time interval that can elapse before the zone is no longer authoritative
* TTL: Minimum TTL field that should be exported with any RR from this zone

Records
^^^^^^^

.. image:: images/dnszone-dnszone-records.png
   :alt: Screenshot of section Records of tab DNS zone of type DNS zone

The DNS records for this zone

Supported record types:

* A

.. image:: images/dnsrecord-A.png
   :alt: Screenshot of record type A

* AAAA

.. image:: images/dnsrecord-AAAA.png
   :alt: Screenshot of record type AAAA

* AFSDB

.. image:: images/dnsrecord-AFSDB.png
   :alt: Screenshot of record type AFSDB

* CAA

.. image:: images/dnsrecord-CAA.png
   :alt: Screenshot of record type CAA

* CERT

.. image:: images/dnsrecord-CERT.png
   :alt: Screenshot of record type CERT

* CNAME

.. image:: images/dnsrecord-CNAME.png
   :alt: Screenshot of record type CNAME

* DKIM (TXT)

.. image:: images/dnsrecord-DKIM.png
   :alt: Screenshot of record type DKIM

* DMARC (TXT)

.. image:: images/dnsrecord-DMARC.png
   :alt: Screenshot of record type DMARC

* DS

.. image:: images/dnsrecord-DS.png
   :alt: Screenshot of record type DS

* KEY

.. image:: images/dnsrecord-KEY.png
   :alt: Screenshot of record type KEY

* KX

.. image:: images/dnsrecord-KX.png
   :alt: Screenshot of record type KX

* LOC

.. image:: images/dnsrecord-LOC.png
   :alt: Screenshot of record type LOC

* MX

.. image:: images/dnsrecord-MX.png
   :alt: Screenshot of record type MX

* NAPTR

.. image:: images/dnsrecord-NAPTR.png
   :alt: Screenshot of record type NAPTR

* NS

.. image:: images/dnsrecord-NS.png
   :alt: Screenshot of record type NS

* NSEC

.. image:: images/dnsrecord-NSEC.png
   :alt: Screenshot of record type NSEC

* PTR

.. image:: images/dnsrecord-PTR.png
   :alt: Screenshot of record type PTR

* RRSIG

.. image:: images/dnsrecord-RRSIG.png
   :alt: Screenshot of record type RRSIG

* SIG

.. image:: images/dnsrecord-SIG.png
   :alt: Screenshot of record type SIG

* SPF (TXT)

.. image:: images/dnsrecord-SPF.png
   :alt: Screenshot of record type SPF

* SRV

.. image:: images/dnsrecord-SRV.png
   :alt: Screenshot of record type SRV

* SSHFP

.. image:: images/dnsrecord-SSHFP.png
   :alt: Screenshot of record type SSHFP

* TXT

.. image:: images/dnsrecord-TXT.png
   :alt: Screenshot of record type TXT

The records with (TXT) appended are actually stored as TXT records in the zone, but FusionDirectory still provides a specific interface to help you correctly use them.
