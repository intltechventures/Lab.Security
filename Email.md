
# Email Security Check Resources

## Background 

- https://en.wikipedia.org/wiki/Email_authentication

- https://dmarc.org/wiki/Glossary


## Checks for Legitimacy

### References

- **SPF (Sender Policy Framework)**: 
  + This is a published DNS record that lists exactly which IP addresses and servers are authorized to send emails on behalf of your domain. Receiving servers check this list to confirm the email came from an approved source.
  + https://en.wikipedia.org/wiki/Sender_Policy_Framework
    * "an email authentication method that allows checking whether the sending mail server is authorized to originate mail from the email sender's domain.[1][2] This authentication only applies to the email sender listed in the "envelope from" field during the initial SMTP connection. If the email is bounced, a message is sent to this address,[2] and for downstream transmission it typically appears in the "Return-Path" header. To authenticate the email address which is actually visible to recipients on the "From:" line, other technologies, such as DMARC, must be used. Forgery of this address is known as email spoofing,[3] and is often used in phishing and email spam."
  + https://dmarc.org/wiki/Glossary#SPF


- **DKIM (DomainKeys Identified Mail)**: 
  + This adds a cryptographic digital signature to the email header. The receiving server uses the sender's public key (also published in DNS) to decrypt the signature, verifying that the email actually originated from your domain and was not altered in transit.
  + https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail
    * "an email authentication method that permits a person, role, or organization that owns the signing domain to claim some responsibility for a message by associating the domain with the message."    
  + https://dmarc.org/wiki/Glossary#DKIM


- **DMARC (Domain-based Message Authentication, Reporting, and Conformance)**: 
  + This policy ties SPF and DKIM together. It instructs receiving servers on how to handle emails that fail SPF or DKIM checks. You can set it to monitor (none), send to spam (quarantine), or block the email entirely (reject).
  + https://en.wikipedia.org/wiki/DMARC
    * "an email authentication protocol. It is designed to give email domain owners the ability to protect their domain from unauthorized use, commonly known as email spoofing. The purpose and primary outcome of implementing DMARC is to protect a domain from being used in business email compromise attacks, phishing email and email scams."
  + https://dmarc.org/
  + https://dmarc.org/overview/
  + https://dmarc.org/wiki/Glossary#DMARC
  + **Related RFCs**: 
    * **RFC 9989: Domain-Based Message Authentication, Reporting, and Conformance (DMARC)**
      * https://www.rfc-editor.org/rfc/rfc9989.html
    * **RFC 9990: Domain-Based Message Authentication, Reporting, and Conformance (DMARC) Aggregate Reporting**
      https://www.rfc-editor.org/rfc/rfc9990.html
    * **RFC 9991: Domain-Based Message Authentication, Reporting, and Conformance (DMARC) Failure Reporting**
      * https://www.rfc-editor.org/rfc/rfc9991.html
    * Notes:
      * Summary of Changes in DMARCbis
        * https://dmarc.org/2025/12/summary-of-changes-in-dmarcbis/
        * https://datatracker.ietf.org/wg/dmarc/documents/
  + ''''Obsoleted RFCs''':
    * RFC 7489: Domain-based Message Authentication, Reporting, and Conformance (DMARC)
      * https://datatracker.ietf.org/doc/html/rfc7489



### Possibly Useful Tools/Utilities 

- DMARC Record Lookup
  + https://easydmarc.com/tools/dmarc-lookup



### Articles

- NIST; Technical Note (NIST TN) - 1945; Email Authentication Mechanisms: DMARC, SPF and DKIM
  + https://www.nist.gov/publications/email-authentication-mechanisms-dmarc-spf-and-dkim
    * "In recent years the IETF has been making a range of efforts to secure the email infrastructure and its use. Infrastructure protection includes source authentication by RFC 7208 Sender Policy Framework (SPF), message integrity authentication by RFC 6376 Domain Keys Identified Mail (DKIM), and domain owner feedback on the effectiveness of these methods by RFC 7489 Domain- based Message Authentication, Reporting and Conformance (DMARC). The High Assurance Domains (HAD) secure email project at NIST has been supporting the development of these initiatives by developing and deploying test infrastructure. This report describes our cumulative experiences with a test system for DMARC and its related protocols."
    * Published: February 16, 2017
    * Author: J. S. Nightingale


- SANS Technology Institute, Internet Storm Center; SPF and DMARC use on GOV domains in different ccTLDs
  + https://isc.sans.edu/diary/29384
    * Published: 2022-12-30
    * Author: Jan Kopriva 

- What are DMARC, DKIM, and SPF? 
  + https://www.cloudflare.com/learning/email-security/dmarc-dkim-spf/


- Authenticating Email Using SPF, DKIM & DMARC
  + https://www.coalitioninc.com/topics/authenticating-email-using-SPF-DKIM-&-DMARC


- SPF, DKIM, DMARC: What They Are and Why They Matter
  + https://powerdmarc.com/all-about-spf-dkim-dmarc/


- SPF and DKIM: Protocols To Ensure Email Security
  + https://threatcop.com/blog/spf-and-dkim/


- Getting Started With DMARC
  + https://dmarcly.com/blog/getting-started-with-dmarc


- Can someone explain DMARC, SPF, and DKIM to me like I'm 5? 
  + https://www.reddit.com/r/sysadmin/comments/16gvtdj/can_someone_explain_dmarc_spf_and_dkim_to_me_like/
    * https://www.reddit.com/r/sysadmin/comments/16gvtdj/comment/k0aidyz/
      * "**SPF**: These are the servers I will send from. If it says it's from me, but comes from somewhere else, it's likely fake"
      * "**DKIM** : This is my signature, if it's not on the email, it probably didn't come from my server."
      * "**DMARC** : If you get mail that doesn't match the above, here's what I want you to do with it."



### Breach Examples

- 2026-06-25: Photo ZIP campaign targeting hospitality industry delivers Node.js implant for persistent access 
  + https://www.microsoft.com/en-us/security/blog/2026/06/25/photo-zip-campaign-targeting-hospitality-industry-delivers-node-js-implant-persistent-access/
  + Re: 
  + https://www.linkedin.com/posts/rodmoura_cybersecurity-incidentresponse-threatintelligence-share-7476104426080894976-EnbR
    * "A guest emails the front desk: bedbugs, a photo attached, and a threat to call the health inspector. The receptionist — who handles forty of these a day — opens the photo."
    * "That's the whole breach. No zero-day. No genius exploit. Just a tired person doing their job."


