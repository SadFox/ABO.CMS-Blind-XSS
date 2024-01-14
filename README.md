# ABO.CMS-Blind-XSS
ABO.CMS Blind XSS

Exploit Title: Blind XSS in ABO.CMS 
Date: 25.10.2023
Exploit Author: sadfox
Vendor Homepage: https://abocms.ru
Version: All editions of ABO.CMS
Tested on: ABO.CMS 5.9.3
CVE : CVE-2023-46952

The Referer header contains a blind XSS. A mandatory condition is the presence of a input Form (for example, form for Support request) on the site. Then when submitting the Form, if you pass 
Referer: http://evil.oastify.com/ref"<img src=/> then the <img src=/> tag will be embedded in the CMS admin panel at http://demo.target.ru/admin.php?lang=rus&name=forms&action=datalist&id=<LAST-ENTRY-ID>.
