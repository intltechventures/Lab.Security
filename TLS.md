
# TLS Resources 

## References
- https://en.wikipedia.org/wiki/Transport_Layer_Security

- TLS 1.3
  + https://tools.ietf.org/html/rfc8446
    * "The Transport Layer Security (TLS) Protocol Version 1.3"

  + https://datatracker.ietf.org/doc/rfc8446/


## Certificate Resources
- [Let's Encrypt Certificate Authority](https://letsencrypt.org/)


## Vendor Support Notes

### Microsoft Azure

- https://github.com/MicrosoftDocs/azure-docs/blob/master/articles/azure-monitor/platform/data-security.md#sending-data-securely-using-tls-12

- Azure Feedback Forum Postings...
  + https://feedback.azure.com/forums/169385-web-apps/suggestions/35097916-tls-1-3-is-now-approved-this-should-be-implemente

  + https://feedback.azure.com/forums/217313-networking/suggestions/37797601-tls-1-3-and-hsts-support-for-azure-application-gat


### Microsoft Applications, Developer Support

- 2020-01-30 Microsoft TLS 1.3 Support Reference
  + https://devblogs.microsoft.com/premier-developer/microsoft-tls-1-3-support-reference/
    * "TLS/1.3 is supported in all versions of Chromium-based Edge (and will be
      supported on all platforms.  The Chromium based Edge just went GA so this
      should be good to go.  Chrome and Firefox and other chromium-based
      browsers support TLS 1.3."

    * "As the TLS 1.3 was only ratified at the end of CYH1 there is no official roadmap that is published as release of this article.  The supported protocols still only go up to TLS 1.2.  There is not roadmap of TLS 1.3 support but the TLS best practices site does state “TLS 1.2 is a standard that provides security improvements over previous versions. TLS 1.2 will eventually be replaced by the newest released standard TLS 1.3 which is faster and has improved security”

    * "TLS 1.3 is also supported on Windows 1903 as of release of this article
      for testing purposes only, not production environment."

    * "For SQL, it is currently not supported, it does support TLS 1.2.
      Confirming support for TLS 1.3 is in the roadmap and will share details
      when released. "



- Taking Transport Layer Security (TLS) to the next level with TLS 1.3 
  + https://www.microsoft.com/security/blog/2020/08/20/taking-transport-layer-security-tls-to-the-next-level-with-tls-1-3/
  + https://redmondmag.com/articles/2020/08/20/microsoft-tls-1-3-support-plans.aspx
    * "Microsoft is planning to add TLS 1.3 support to the .NET framework with the arrival of .NET 5.0, which is expected to reach general availability in November of [2020]."
    * However, developers should "rely on the underlying OS to provide the TLS version" because the OS will default to the strongest available TLS protocol, Microsoft's dev blog explained. It added that "starting with .NET Framework 4.7, the default configuration is to use the OS TLS version."


## News Articles
* https://wiki.openssl.org/index.php/TLS1.3
* https://www.ietf.org/blog/tls13/
* https://www.cloudflare.com/learning-resources/tls-1-3/
* [The New Illustrated TLS Connection](https://tls13.ulfheim.net/)

### 2019 

### 2018
  * https://www.zdnet.com/article/its-2018-and-network-middleware-still-cant-handle-tls-without-breaking-encryption/
