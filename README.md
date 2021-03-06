OpenSSL D interface
-------------------

**Notice:**
This project is forked from [D-Programming-Deimos/openssl](https://github.com/D-Programming-Deimos/openssl) to give better supports for our projects.


From the OpenSSL website: "The OpenSSL Project is a collaborative effort to
develop a robust, commercial-grade, full-featured, and Open Source toolkit
implementing the Secure Sockets Layer (SSL v2/v3) and Transport Layer Security
(TLS v1) protocols as well as a full-strength general purpose cryptography
library. The project is managed by a worldwide community of volunteers that
use the Internet to communicate, plan, and develop the OpenSSL toolkit and its
related documentation."

Library version: 1.1.0h

Status: (Almost) complete, typical application should build fine. Most of the
functions from <openssl/kssl.h> are not available due to missing Kerberos
headers.

The OpenSSL headers are huge (>35k LOC) and make quite liberal use of the C
preprocessor, and thus a fully automatic translation is as desirable as
it is infeasible. This repository contains the result of a semi-automatic
approach, and while all header files have been ported (and successfully
compile), some preprocessor artifacts still need to be ported (currently
commented out and tagged with a FIXME note).

The OPENSSL_NO_* family of conditional compilation switches has been
translated to D version()s, none of which is set by default.

License: The OpenSSL toolkit is under a dual license, i.e. both the conditions
of the OpenSSL License and the original SSLeay license apply to the toolkit.
See the OpenSSL distribution for details. These interface files are a derived
work and do not impose any additional restrictions.


## Build on Windows
1. Download Win64 OpenSSL from [here](http://slproweb.com/products/Win32OpenSSL.html).
2. Install it to a folder. (For example: C:\OpenSSL-Win64).
3. Replace the two libraries in lib\x64 with the latest ones (In C:\OpenSSL-Win64\lib\VC).

**Note:** The Win64 OpenSSL v1.1.0 serials are recommended.