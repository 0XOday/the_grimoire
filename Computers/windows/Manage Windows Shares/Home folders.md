On domain, data storage and PC configurations should be as centralized as possible so that they can be more easily monitored and backed up. This means that user data should be stored on file servers rather than on local client computers. Various settings in Active Directory can be used to redirect user profile data to network storage. 

A *home folder* is a private drive mapped to a network share in which users can store personal files. The home folder location is configured via the account properties on the *Profile* tab using the connect to box. Enter the share in the form 
```
\\server\home%\%username%
```
,where 
```
\\SERVER\HOME%
```
is a shared folder created with the appropriate permissions to allow users users to read and write their own subfolder only.

When the user signs in, the home folder appears under This PC with the allocated drive letter. 

