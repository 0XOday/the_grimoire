1. What is it?
The Biba Model is an access control model designed to maintain the integrity of data within a system. It addresses the issues of data corruption and unauthorized 
modifications, particularly in environments where data integrity is paramount.
2. What does it do/how does it work?
The Biba Model enforces two primary rules:
• No Write Up (Simple Integrity Property): A subject at a lower integrity level cannot write to a higher integrity level. This prevents users from contaminating more reliable data.
• No Read Down (Star Integrity Property): A subject at a higher integrity level cannot read data at a lower integrity level. This ensures that high-integrity users 
do not receive corrupted or unreliable information.
These rules help maintain the accuracy and reliability of data by preventing unauthorized alterations and ensuring that only trusted users can modify high-integrity 
data.
3. Why/when would I use it?
You would use the Biba Model in environments where data integrity is critical, such as financial systems, healthcare records, or any application that requires accurate data. 
This model is particularly useful for preventing the introduction of errors and ensuring the trustworthiness of data in a multilevel security context.
