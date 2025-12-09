Task 2 – Phishing Email Analysis  

1. objective

		This report analyzes a sample phishing email pretending to be from PayPal.  After examining the sender address, link, 	message content, and email-header authentication results, the email is confirmed to be a **phishing attempt** designed to steal 	user credentials.

---

2. Phishing Indicators Identified

		1. Fake Sender Email
			Email claims to be from PayPal, but the sender address is: support@paypalsecure-alert.com`
			Real PayPal uses: @paypal.com`
			
			This mismatch indicates spoofing.

		 2. Suspicious Link
			Email contains the link:'http://paypal-security-verify-login.fake-site.com'

			This is not a real PayPal domain and can steal login details.

		 3. Generic Greeting
			The email begins with: "Dear User" Legitimate companies address customers by name.

		4. Urgent / Threatening Language
			Message says: "You have 24 hours to act."

			This is a common phishing tactic to create panic and force quick action.

		 5. Header Authentication Failures
			From the email-header.txt file:- "SPF: fail"  (Sender not authorized by the domain)
							- "DKIM: none" (No digital signature from PayPal)
							- "DMARC:fail" (Fails alignment policy required by the domain)
			
			These failures strongly indicate spoofing.
---
3. Conclusion
The analyzed message is a "phishing email".  
It attempts to trick the user into clicking a fake link and providing sensitive login information.  
The sender is spoofed, the link is malicious, the tone is urgent, and the header authentication clearly fails.
---
 4. Files Included
- 'sample-email.txt' — Full phishing email content  
- 'email-header.txt' — Email header used for analysis
-  'screenshots' 
- 'README.md' — This report
