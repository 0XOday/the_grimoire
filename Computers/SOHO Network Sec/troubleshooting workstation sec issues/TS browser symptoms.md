* Malware like to target the web browser 
* redirection is one symptom of compromise
	* check the *HOST* file
		* HOST file is considered legacy means of mapping domains to IPs 
* Certificate warnings 
* Self signed or issued by a CA that is not trusted 
* the cert is expired or listed as revoked 
Improper use of certificates is also an indicator for a type of on-path attack by a malicious proxy:

1. A user requests a connection to a secure site and inspects the site’s certificate.
2. Malware on the host or some type of evil-twin access point intercepts this request and presents its own spoofed certificate to the user/browser. Depending on the sophistication of the attack, this spoof certificate may or may not produce a browser warning. If the malware is able to compromise the trusted root certificate store, there will be no warning.
3. If the browser accepts this certificate or the user overrides a warning, the malware implements a proxy and forwards the request to the site, establishing a session.
4. The user may think he or she has a secure connection to the site, but in fact the malware is in the middle of the session and is able to intercept and modify all the traffic that would normally be encrypted.