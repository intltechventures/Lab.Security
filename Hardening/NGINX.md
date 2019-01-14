
Tips for Security Hardening NGNIX
====
(a work in progres...)


### NGIX Documentation
* https://docs.nginx.com/nginx/admin-guide/security-controls/
* https://www.nginx.com/resources/wiki/start/
  * https://www.nginx.com/resources/wiki/start/topics/tutorials/config_pitfalls/
* https://www.nginx.com/blog
  * https://www.nginx.com/blog/pci-dss-best-practices-with-nginx-plus/
  * https://www.nginx.com/blog/securing-perimeter-achieving-zero-trust-nginx-plus-sso-rest/
  * https://www.nginx.com/blog/securing-applications-microsoft-azure-app-service-nginx-plus/
* http://nginx.org/en/docs/
  * http://nginx.org/en/docs/http/ngx_http_limit_conn_module.html


### OWASP
* https://www.owasp.org/index.php/SCG_WS_nginx


### SELinux
* http://selinuxproject.org/page/User_Resources
* https://selinuxproject.org/page/Guide/Installation
* https://www.linode.com/docs/quick-answers/linux/install-selinux-on-ubuntu/
* https://wiki.ubuntu.com/SELinux


### Cloud Hosting Companies
* DigitalOceann.com
  * https://www.digitalocean.com/community/tutorials/how-to-secure-nginx-on-ubuntu-14-04
  * https://www.digitalocean.com/community/tutorials/how-to-secure-nginx-with-naxsi-on-ubuntu-16-04
  * https://www.digitalocean.com/community/tutorials/how-to-set-up-nginx-with-http-2-support-on-ubuntu-18-04
  * https://www.digitalocean.com/community/tutorials/how-to-secure-nginx-with-let-s-encrypt-on-ubuntu-18-04
* DreamHost .com
  * https://help.dreamhost.com/hc/en-us/articles/222784068-The-most-important-steps-to-take-to-make-an-nginx-server-more-secure
* Hostway.com
  * https://support.hostway.com/hc/en-us/articles/360002191344-Some-tips-to-secure-NGINX
* linode.com
  * https://www.linode.com/docs/web-servers/nginx/tls-deployment-best-practices-for-nginx/


### Modules
* ModSecurity
  * https://www.modsecurity.org/
  * https://github.com/SpiderLabs/ModSecurity


### Github Resources
* fail2ban
  * https://github.com/fail2ban/fail2ban
* https://github.com/michyweb/nginx-security-conf


### Mozilla Resources
* https://mozilla.github.io/server-side-tls/ssl-config-generator/

### DZone Resources
* https://dzone.com/articles/how-to-secure-nginx-with-naxsi-on-ubuntu-1604


### Security Scanning Resources
* https://securityheaders.com/
* https://report-uri.com/home/tools


### Misc. Articles [TO-DO: Analyze and Rationalize this list]
* https://geekflare.com/nginx-webserver-security-hardening-guide/
  * https://geekflare.com/install-modsecurity-on-nginx/
  * https://geekflare.com/modsecurity-owasp-core-rule-set-nginx/
* https://www.upguard.com/blog/how-to-build-a-tough-nginx-server-in-15-steps
* https://gist.github.com/plentz/6737338
* https://www.tecmint.com/nginx-web-server-security-hardening-and-performance-tips/
* https://tylermade.net/2017/05/01/nginx-security-hardening/
* https://hostadvice.com/how-to/how-to-harden-nginx-web-server-on-ubuntu-18-04/
* https://www.scalescale.com/tips/nginx/nginx-security-guide/#
* https://scotthelme.co.uk/https-cheat-sheet/


### General Suggesdtions [TO-DO: Find and cite NGNIX documentation pages for these]
* Turn On SELinux
* Limit concurrent connections from one IP to [n] to defeat DoS attacks. (e.g. n=10)
* Disable all Nginx modules that we don’t need to reduce the attack surface area.
* Disable Nginx headers to deny attackers information about the server.
* Enable security headers such as “X-XSS-Protection” and “X-Frame-Options” to block common attacks


### RFC References
* [RFC-6792: HTTP Strict Transport Security (HSTS)](https://tools.ietf.org/html/rfc6797)
  * https://scotthelme.co.uk/hsts-cheat-sheet/


