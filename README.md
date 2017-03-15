# devCA

Automates the setup of a custom Certificate Authority and provides routines for signing and revocation of certificates. To use, first customize the commands in this file and the settings in openssl.cnf,then run:

```make init

Then, copy in certificate signing requests, and ensure their suffix is .csr before signing them with the following command:

```make sign

To revoke a key, name the certificate file with the cert option as shown below:

```make revoke cert=foo.cert

This will revoke the certificate and call gencrl; the revocation list will then need to be copied somehow to the various systems that use your CA cert.