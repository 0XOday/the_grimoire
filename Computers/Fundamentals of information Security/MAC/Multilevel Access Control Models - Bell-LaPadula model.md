
1. What is it?
The Bell-LaPadula Model is a security model focused on maintaining the confidentiality of information within a multilevel security system. It was developed for government and military applications to protect classified information.

2. What does it do/how does it work?
The Bell-LaPadula Model enforces two primary rules:
• No Read Up (Simple Security Property): A subject at a lower security level cannot read data at a higher security level. This prevents users from accessing 
sensitive information beyond their clearance level.
• No Write Down (*-Property): A subject at a higher security level cannot write data to a lower security level. This prevents sensitive information from being 
leaked to less secure areas. By enforcing these rules, the model ensures that sensitive information remains 
confidential and is not inadvertently disclosed to unauthorized users
3. Why/when would I use it?
You would use the Bell-LaPadula Model in environments where the confidentiality of information is critical, such as military or government organizations that handle classified data. It is designed to protect against unauthorized disclosure of information, ensuring that users cannot access or leak sensitive data