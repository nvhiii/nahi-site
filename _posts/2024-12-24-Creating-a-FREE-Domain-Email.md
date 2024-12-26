---
layout: post
title: "Creating a Free Domain Email"
date: 2024-12-22 23:00:00 +0000
tags: [tutorial]
footnotes:
  - "[ZohoMail Video Link](https://www.zoho.com/mail/how-to/create-business-email-address.html#setting-up-zoho-mail)"
---

### Want a Cool Domain Email?

1. Ensure you have a bought domain. (Will not work with Github Pages) + Create a zohomail account (free).

2. Go to your domain's DNS manager. Basically, go to where your domain's nameservers point for DNS resolution.

3. In the Zohomail UI, copy the TXT name + TXT val provided to ensure ownership of domain, and paste it into your DNS manager UI as a TXT record.

4. Now, go to zoho mail Now after verification, you can create sysadmin email + 4 other accounts (if you want), under the free tier. You can set up things like email forwarding, restricted stuff, etc.

5. After desired accounts are created, you must go to the section in zohomail which provides the mailing (MX) records for your domain. Copy the 3 rows, and input them as separate MX records in your DNS provider UI.

6. Then, use zohomail's provided SPF and DKIM records and also paste them as individual TXT records in your DNS provider UI

7. You are done!
