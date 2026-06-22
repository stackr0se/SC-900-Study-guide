# Authentication and authorization

Authentication, Who are you? (AuthN)
- Authentication is the process of providing that a person is who they say they are Authetnication grants access.

Authorization, What are you allowed to do? (AuthZ
- Authorization determins the level of access or the permissions an authenticated person has to your data and resources.

# Identity as the prmary security permiter

Identity has become the new security perimeter that enables organizations to secure their assets.
An identity, which can be used to authenticate and authorize someone or something, may be associated with:
- User
- Application
- Device
- Other

Four pillars of an identity infranstructure:
- Administration: Focused on creating, managing and maintaining identities across users, devices and services
- Authentication: Ensures enough proof to confirm an identity using methods such as mfa
- Authorization: Determins what the authenticated entity is allowed to do
- Auditing: Tracks who accesed what, when and how
<img width="492" height="355" alt="image" src="https://github.com/user-attachments/assets/a2f43b7f-1d4a-4b56-bc83-63bc9112c90f" />

# Modern authentication and the role of the identity provider

Modern authentication is an term for authentication and authorization methods between a client and a server.
- 1: At the cetner of modern authentication is the role of the identity provider (IdP)
- 2: Idp offers authentication, authorization and auditing services
- 3: IdP enables organizations to establish authentication and authorization polices, monitor user behavior and more
- 4: Fundamental capbilities of an IdP and 'modern authentication' include support for secure authentication methods, single sign-on, federation with other IdP's and more
- 5: Microsoft Entra ID is an example of a cloud-based identity provider

<img width="1263" height="608" alt="image" src="https://github.com/user-attachments/assets/f77620fa-d676-4052-904a-5b279bb80abc" />

# The concept of federation

A simplified way to think about federation:
- The website uses the authentication services of identity provider A (IdP-A)
- The user authenticates with identity provider B (IdP-B)
- IdP-A has a trust relationship configured with IdP-B
- When the user signs in to the website, it can trust the user's credentials and allow access
<img width="607" height="378" alt="image" src="https://github.com/user-attachments/assets/366b8c6e-72de-485d-94f4-1189b07a5ecc" />
