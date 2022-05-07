Part 1:

Question 1
The company would need to use a UBA (User behavior analytics) tool to monitor
and compare analytics to predefined baseline values. To respond to fields
that have crossed their acceptable threshold, the company would need a SOAR 
service, wich automates security processes and responds to security incidents.
SOAR uses playbooks, which would be set up specifically for the company, automatically
responding to potential threats, decreasing incident response time.

Global mitigations that the whole company could use would include setting up playbook rules such as: 
VSI user accounts should be locked out after 5 incorrect attempts and
preventing any user from resetting their password more than once during a 24h period.

For each user, mitigations could include frequent changes of their passwords, never leaving any physical copies
of their passwords near their workspace, opting in for two-factor authentication whenever possible,
and familiarize themselves with the company's security policy as well as always patching
their computer for security vulnerabilities whenever possible.

Question 2
If three or more “Bad Logins" are detected coming from a single IP address (that is
not a VSI IP address), that IP address should be blacklisted and prevented from
accessing the user account login in the future.

Part 2:

Question 1
Based on the geographic map, we recommend that a firewall rule be put in place
to block any incoming HTTP traffic where the source IP comes from Kharkiv, Ukraine.

Geographic Map: https://i.imgur.com/gbN48Te.png

Baseline Activity: https://i.imgur.com/2yfHZTq.png

Attack Activity: https://i.imgur.com/aP33E16.png

Question 2
We would advise blocking any IP address which generates three or more consecutive POST requests to the
VSI login page. This would prevent any brute-force attacks, regardless of source IP.

Block any IP address which generates three or more consecutive POST requests
identified by the user agent string “Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.2;
SV1; .NET CLR 2.0.50727987787; InfoPath.1)”. During the attack, 1,296 requests had
that user agent string, while very little traffic during normal operation has that user
agent string.
