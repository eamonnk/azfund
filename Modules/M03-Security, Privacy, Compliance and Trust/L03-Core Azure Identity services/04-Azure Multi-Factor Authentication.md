<h1><strong><span style="color: #0000CD;">Azure MFA</span></strong></h1>



*Azure Multi-Factor Authentication* (MFA) provides additional security for your identities by requiring two or more elements for full authentication. These elements fall into three categories:

- *Something you know* could be a password or the answer to a security question.
- *Something you possess* might be a mobile app that receives a notification, or a token-generating device.
- *Something you are* is typically some sort of biometric property, such as a fingerprint or face scan used on many mobile devices.

<p style="text-align:center;"><img src="../Linked_Image_Files/mfa.png" width="600" height="150" alt="Image of a username and password entry screen, mobile phone, usb key, smart card, image representing various types of biometric authentication, and certificate all in a line, representing how they can all be tied together to provide MFA"></p>



Using MFA increases identity security by limiting the impact of credential exposure. To fully authenticate, an attacker who has a user's password would also need to have possession of their phone or their fingerprint, for example. Authentication with only a single factor is insufficient and, without MFA, an attacker would be unable to use those credentials to authenticate. MFA should be enabled wherever possible as MFA adds enormous benefits to security.

MFA comes as part of the following Azure service offerings:

- *Azure Active Directory Premium licenses*. These licenses provide full-featured use of Azure Multi-Factor Authentication Service (cloud) or Azure Multi-Factor Authentication Server (on-premises).
- *Multi-Factor Authentication for Office 365*. A subset of Azure Multi-Factor Authentication capabilities are available as a part of your Office 365 subscription.
- *Azure Active Directory global administrators*. Because global administrator accounts are highly sensitive, a subset of Azure Multi-Factor Authentication capabilities are available as a means to protect these accounts.



> **Note**: You can read more about MFA at <a href="https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-mfa-howitworks" target="_blank"><span style="color: #0066cc;" color="#0066cc">How it works: Azure Multi-Factor Authentication </span></a>.
