

Certificate Manager

A digital certificate is a means of proving the identity of a subject, such as a user, computer, or service. The validity of each certificate is guaranteed by the issuing certification authority (CA). The Certificate Manager console (certmgr.msc) shows which certificates have been installed and provides a mechanism for requesting and importing new certificates.

The tool displays many subfolders, but the most widely used are:

    The Personal folder stores the certificates that have been issued to the user account. User certificates can be used for tasks such as authenticating to a network access server, encrypting data, and adding a digital signature to a document or message to prove its authenticity.
    Trusted Root Certification Authorities contains a superset of the certificates of all issuers that are trusted, including Microsoft’s own CA root, local enterprise CAs and third-party CAs. Most of these certificates are managed via Windows Update.
    Third-party Root Certification Authorities contains trusted issuers from providers other than Microsoft or a local enterprise.

Using Certificate Manager to view certificates for the current user. The trusted root certificates added here allow the computer to trust any subject certificates issued by these CAs. Note that as these are root certificates, each is issued to the organization by itself. (Screenshot courtesy of Microsoft.)

certmgr.msc manages certificates for the current user. There is also a computer certificate store, which can be managed via certlm.msc.

Trusting an unsafe CA raises critical security vulnerabilities. For example, a rogue CA certificate might allow a website to masquerade as a legitimate bank or other service and trick the user into submitting a password because the browser seems to trust the web server’s certificate. In some cases, you may need to use Certificate Manager to remove compromised certificates.

Third-party browser applications usually maintain a separate store of personal certificates and trusted root CAs.
