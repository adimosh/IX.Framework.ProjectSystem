IX Framework Project System
===========================

This NuGet package is built to serve only the IX.Framework package projects.
Normally, unless you wish to extend the framework, you won't need to use this
package in any way.

If you wish to benefit from the same project system, however, plase note that
there are a set of rules:

Warning!!!
----------

Should you wish to reference this package, please always remember to reference
it with PrivateAssets set to "all", lest some package references will flow down
and be direct references in subsequent projects.

Debug builds
------------

- IXCONTRACTSNONPUBLIC, DEBUG and TRACE are defined by default
- package generation is off by default

Release builds
--------------

- RELEASE is defined by default
- package generation is on by default

All builds
----------

- JETBRAINS_ANNOTATIONS is defined by default
- Environment variable IxDevOpsBuild configures build as part of a CI setup
- Environment variables IxVersionPrefix and IxVersionSuffix define versioning,
if they are present, otherwise some defaults are used