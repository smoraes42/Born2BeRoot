## MAC - Mandatory Acces Controls
* Mandatory Layer enforces access policies based on rules defined by system administrators
* Goes beyond traditional DAC (Discretionary Acces Controls) that as a means of restricting 
access to objects based on the identity of subjects and/or groups to which they belong. 
MAC  essentially means tht every action a program could perform that affects 
system in any way is checked against  a security ruleset
This ruleset, in contrast to DAC methods, cannot be modified by users.
Using virtually any mandatory access control system will significantly improve
the security of your computer, although there are differences in how it can be implemented.

## Security Policies
* SELinux
    * System Level - Deny Everything
    * Application Level - Allow Everything - May be overriden by System Level 
* AppArmor
    * System Level - Allow Everything
    * Application Level - Deny Everything

