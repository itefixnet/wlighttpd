**Wlighttpd** is a basic web server solution for Windows environments. It is a packaging of lighttpd and Cygwin. You can use Wlighttpd as a secure solution with a small footprint for serving https requests.

[lighttpd](https://www.lighttpd.net/ "Lighttpd - Fly light") is a secure, fast, compliant, and very flexible web server that has been optimized for high-performance environments. lighttpd uses memory and CPU efficiently and has lower resource use than other popular web servers. Its advanced feature-set (FastCGI, CGI, Auth, Output-Compression, URL-Rewriting and much more) makes lighttpd the perfect web server for all systems, small and large. [Cygwin](http://www.cygwin.com/) is a Linux-like environment for Windows. It consists of a DLL, which emulates substantial Linux API functionality, and a collection of tools.

### Installation

Wlighttpd comes as a ZIP file containing an [NSIS](https://nsis.sourceforge.io/Main_Page) installer. Simply unzip your downloaded copy and run the installer :

> 1.  Accept License agreement.
> 2.  Specify an installation location.
> 3.  Installation starts. By clicking 'Details' button, you can get more detailed information about installation.

### Usage

The installer will set up the **Wlighttpd - Lighttpd** service, configurable by the contents of the _**etc/lighttpd/lighttpd.conf**_ file

You need to:

*   update the configuration file according to your needs. The default one comes with a self signed certificate and redirects http to https for non-local requests. There are many options that can be configured via the configuration file. Check [lighttpd wiki](https://redmine.lighttpd.net/projects/lighttpd/wiki) for more information.

*   replace the self-signed ssl certificate by your own.

You can now start the service and monitor the activity via log files at _**/var/log**_ folder.

The service is set up in automatic mode and run by the LOCAL SERVICE Account (limited access).

Lighttpd provided supports following plugins/features:

**Plugins**
```
mod_access,  mod_accesslog,  mod_ajp13,  mod_alias,  mod_auth,  mod_authn_file,  mod_cgi,  mod_deflate.  mod_dirlisting.  mod_evhost,  mod_expire,  mod_extforward,  mod_fastcgi,  mod_indexfile,  mod_openssl,  mod_proxy,  mod_redirect  mod_rewrite  mod_rrdtool  mod_scgi  mod_setenv  mod_simple_vhost,  mod_sockproxy,  mod_ssi,  mod_staticfile,  mod_status,  mod_userdir,  mod_vhostdb,  mod_webdav,  mod_wstunnel
```
**Features**
```
auth-crypt, compress-deflate, compress-gzip, large-files, network-ipv6, network-openssl, regex-conditionals
```
