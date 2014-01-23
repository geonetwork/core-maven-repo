This dependency is here because I needed a version of Sardine that had the latest httpcomponents as a dependency and which used
a CloseableHttpClient or builder for creating SardineImpl.  This code is generated from

* https://github.com/dkocher/sardine.git

which is a fork of

* https://github.com/lookfirst/sardine

as soon as

* https://github.com/lookfirst/sardine/pull/160

or

* https://github.com/lookfirst/sardine/pull/161

Is merged and a new Sardine release is made we can delete these.  The current Sardine version is 5.0.2 and we will need one of the
next releases... Maybe 5.1?