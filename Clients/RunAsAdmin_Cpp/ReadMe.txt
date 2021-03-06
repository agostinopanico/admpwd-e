========================================================================
    APPLICATION : RunAsAdmin Project Overview
========================================================================

This project demonstrates how to make use of password retrieval capability
of AdmPwd.E, as published via integration library.

RunAsAdmin.exe runs any executable in security context of one of the following
accounts:
-- local admin account
-- domain user account

or both cases, it's expected that password of account is managed by 
AdmPwd.E - tool retrieves the password via PDS using AdmPwd.E integration library.
PDS reads the password from Active Directory either from computer account, 
or from managed domain account

User who runs the tool does not need to know password of local admin at all, 
as long as he/she has been delegated permission to Read Admin Password from
Active Directory mon computer object or user account.

Tool fetches the password from AD for user, and uses it to start new process.
User does not need to know/enter the password at all - everything happens 
behind the scenes.

Note: For demo purpose, code is written in C++/CLR and as such, compiled code 
requires Visual C++ 2015 Redistributable to be installed on the machine.
