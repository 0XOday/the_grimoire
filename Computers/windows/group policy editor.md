
Group Policy Editor

GUI tools such as Settings and Control Panel make changes to user profiles and the system configuration that are ultimately stored in a database called the registry. However, the registry also contains thousands of other settings that are not configurable via these tools. The Group Policy Editor (gpedit.msc) provides a more robust means of configuring many of these Windows settings than editing the registry directly. Also, vendors can write administrative templates to make third-party software configurable via policies.

Using Group Policy Editor to view the local password policy. This computer does not have a strong set of policies. (Screenshot courtesy of Microsoft.)

On a network with hundreds or thousands of computers, group policy is a much more efficient way of imposing policy settings than manually configuring each machine.

Some policies are configured by inputting a discrete value, but most use an enabled/disabled/not defined toggle. It is important to read each policy carefully when choosing whether it should be enabled or disabled and to understand the default behavior of leaving a setting not defined.

The Local Security Policy editor (secpol.msc) can be used to modify security settings specifically.
