A security Control is a safeguard or prevention method to avoid, counteract, or minimize risks relating to personal or company property. For example, a firewall is a type of security control because it controls network communications by allowing only traffic that has specifically been permitted by a system administrator. There are many ways of classifying security controls, but one way is to class them as physical, procedural, or logical. 
* Physical controls work in the built environment to control access to sites, doors locks
* Procedural controls are applied and enforced by people. Examples include incident response processes, management oversight, and security awareness training programs.
* Logical controls are applied and enforced by digital or cyber systems and software. examples include user authentication, antivirus software, and firewalls.
One of the most cornerstones of logical security is an access control system. The overall operation of an access control system is usually described in terms of three functions, referred to as the AAA triad:
* Authentication means that everything using the system is identified by an account and that an account can only be operated by someone who can supply the correct creds
* Authorization means access to resources is allowed only to accounts with defined permissions. Each resource has an access control list specifying  what users can do. Resources often have different access levels; for example, being able to read a file or being able to read and edit it.
* accounting means logging when and by whom a resource was accessed.

Access Control Lists
A permission is a security setting that determines the level of access an account has to a particular resource. A permission is usually implemented at an access control list attached to each resource. Within a ACL, each access control entry (ACE) identifies a subject and the permissions it has for a the resource. A subject could be a human users, a computer or a software service. A subject could be identified in several ways. on a network firewall, subjects might be identified by MAC address, IP address and/or port number. in the case of directory permissions in Windows, each user and security group account has a unique security ID (SID)

*Implicit Deny*
ACL security is typically founded on the principle of implicit deny. implicit deny means that unless there is a rule specifying that access should be granted, any request for access is denied. This principle can be seen clearly in firewall policies. A firewall filters access requests using a set of rules. The rules are processed in order from top to bottom. if a request does not fit any of the rules, it is handled by the last default rule which is to refuse the request. 
*least Privilege*
A complementary principle to implicit deny is that of least privlege. This means that a user should be granted the minimum possible rights necessary to perform the job. This can be complex to apply in practice, however. Designing a permissions system that respects the principle of least privilege while not generating too many support requests from users is a challenging task.
