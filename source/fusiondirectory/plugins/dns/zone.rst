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

A
+

IPv4 address record.

.. image:: images/dnsrecord-A.png
   :alt: Screenshot of record type A

AAAA
++++

IPv6 address record.

.. image:: images/dnsrecord-AAAA.png
   :alt: Screenshot of record type AAAA

AFSDB
+++++

Location of database servers of an AFS cell.

.. image:: images/dnsrecord-AFSDB.png
   :alt: Screenshot of record type AFSDB

CAA
+++

DNS Certification Authority Authorization, constraining acceptable CAs for a host/domain.

.. image:: images/dnsrecord-CAA.png
   :alt: Screenshot of record type CAA

CERT
++++

Certificate record.

.. image:: images/dnsrecord-CERT.png
   :alt: Screenshot of record type CERT

CNAME
+++++

Alias of one name to another: the DNS lookup will continue by retrying the lookup with the new name.

.. image:: images/dnsrecord-CNAME.png
   :alt: Screenshot of record type CNAME

DKIM (TXT)
++++++++++

DomainKeys Identified Mail (DKIM) is an email authentication method designed to detect forged sender addresses in email (email spoofing).

.. image:: images/dnsrecord-DKIM.png
   :alt: Screenshot of record type DKIM

DMARC (TXT)
+++++++++++

DMARC (Domain-based Message Authentication, Reporting and Conformance) is an email authentication protocol. It is designed to give email domain owners the ability to protect their domain from unauthorized use, commonly known as email spoofing.

.. image:: images/dnsrecord-DMARC.png
   :alt: Screenshot of record type DMARC

DS
++

The record used to identify the DNSSEC signing key of a delegated zone.

.. image:: images/dnsrecord-DS.png
   :alt: Screenshot of record type DS

KEY
+++

Key record.

.. image:: images/dnsrecord-KEY.png
   :alt: Screenshot of record type KEY

KX
++

Key exchanger record.

.. image:: images/dnsrecord-KX.png
   :alt: Screenshot of record type KX

LOC
+++

Location record, specifies a geographical location associated with a domain name.

.. image:: images/dnsrecord-LOC.png
   :alt: Screenshot of record type LOC

MX
++

Mail exchange record, maps a domain name to a list of message transfer agents for that domain.

.. image:: images/dnsrecord-MX.png
   :alt: Screenshot of record type MX

NAPTR
+++++

Naming authority pointer, allows regular-expression-based rewriting of domain names.

.. image:: images/dnsrecord-NAPTR.png
   :alt: Screenshot of record type NAPTR

NS
++

Name server record, delegates a DNS zone to use the given authoritative name servers.

.. image:: images/dnsrecord-NS.png
   :alt: Screenshot of record type NS

NSEC
++++

Next secure record, part of DNSSEC, used to prove a name does not exist.

.. image:: images/dnsrecord-NSEC.png
   :alt: Screenshot of record type NSEC

PTR
+++

Pointer to a canonical name. The most common use is for implementing reverse DNS lookups.

.. image:: images/dnsrecord-PTR.png
   :alt: Screenshot of record type PTR

RRSIG
+++++

Signature for a DNSSEC-secured record set.

.. image:: images/dnsrecord-RRSIG.png
   :alt: Screenshot of record type RRSIG

SIG
+++

Signature record (replaced by RRSIG for DNSSEC).

.. image:: images/dnsrecord-SIG.png
   :alt: Screenshot of record type SIG

SPF (TXT)
+++++++++

Sender Policy Framework (SPF) is an email authentication method designed to detect forging sender addresses during the delivery of the email.

.. image:: images/dnsrecord-SPF.png
   :alt: Screenshot of record type SPF

SRV
+++

Generalized service location record, used for newer protocols instead of creating protocol-specific records such as MX.

.. image:: images/dnsrecord-SRV.png
   :alt: Screenshot of record type SRV

SSHFP
+++++

Resource record for publishing SSH public host key fingerprints in the DNS System, in order to aid in verifying the authenticity of the host.

.. image:: images/dnsrecord-SSHFP.png
   :alt: Screenshot of record type SSHFP

TXT
+++

Text record, originally for arbitrary human-readable text in a DNS record. Since the early 1990s, however, this record more often carries machine-readable data.

.. image:: images/dnsrecord-TXT.png
   :alt: Screenshot of record type TXT

The records with (TXT) appended are actually stored as TXT records in the zone, but FusionDirectory still provides a specific interface to help you correctly use them.
