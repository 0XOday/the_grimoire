When a computer is joined to a domain rather than a workgroup, it is put under the control of the domain administrators. To communicate on a domain, the computer must have its own account in the domain. This is separate from any user accounts allowed to sign-in

Windows does not support joining the computer to a domain during an attended installation. The computer can be join during an unattended installation by using an answer file or script. Otherwise, you use either the *Access work or school* options in the *Account* settings app or the System Properties (sysdm.cpl) dialog to join a domain. The computer must be on the domain network and configured by DHCP with an appropriate IP address and DNS servers. Each domain is identified by a FQDN, such as *ad.paladin.lan* and the local computer must be able to resolve the name via DNS to join. The credentials of an account with appropriate administrative privilege's on the domain must be input to authorize the new computer account. 

The same interface can be used to detach the computer and revert to workgroup use. This requires a user account that is a member of the Local Administrators group.

To use services in the domain, the user must sign in to the PC using a domain account. The *Other user* option in the sign-in screen will provide a domain option if it is not the default. You can also enter a username in the format *Domain\username* to specify a domain login.

Note : Conversely when a machine is joined to a domain, *\Username* or *hostname\username* will authenticate against a local user account.