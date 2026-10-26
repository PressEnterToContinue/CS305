# CS305
SNHU CS305 Software Security Course
Module Eight Portfolio Item

This repo contains my Practices for Secure Software Report and refactored code base for Artemis Financial from Project Two.

Q: Who was the client and what did they need?
A: Artemis Financial is a consulting company that builds financial plans for its customers. They wanted a checksum added to their web application to verify data during transfers, and they wanted those transfers to be secure. I added a SHA-256 checksum and switched the app to HTTPS only.

Q: What did I do well, and why does secure coding matter?
A: I scanned the dependencies before and after my changes so I could prove my code didn't add any new vulnerabilities. I also reviewed my code by hand and caught a few things a scanner wouldn't. Secure coding matters because fixing a breach costs way more than preventing one. Breaches also cost client trust and potential business, which is a significant concern.

Q: What was challenging or helpful?
A: Getting the tools working was the most difficult part. The dependency-check plugin was too old to run, and Eclipse was compiling for a Java version that Spring Boot couldn't handle. Running a baseline scan first was the most helpful thing I did.

Q: How did I add layers of security and what would I use in the future?
A: HTTPS for encryption, a SHA-256 checksum for integrity, dependency scanning, and manual code review. In the future I would use the OWASP Top 10, NIST guidance, and dependency scans to establish the priority of present risks.

Q: How did I ensure the code was functional and secure?
A: I ran the application until it was error-free and confirmed the /hash page loaded over HTTPS. I then re-ran the dependency scan and compared it to the baseline scan. I didn't introduce anything new because the results were identical to each other.

Q: What tools or practices will help in the future?
A: OWASP Dependency-Check, Java Keytool, Java's built-in crypto libraries, and testing against a baseline scan before making changes to existing code.

Q: What would I show employers?
A: The report in this repo. It shows I can pick and justify an encryption algorithm, configure HTTPS with certificates, run and dependency scan, and explain my process and findings.
