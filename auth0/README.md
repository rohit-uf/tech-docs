# AUTH0

- user needs to signup / existing users need to be migrated to auth0 to be able to login
- To migrate existing users:
  - write a script to validate authentication for new users in an existing database -> Paid feature

## Embedded Login

![image](https://user-images.githubusercontent.com/103091956/178416382-f56dcfab-e07b-49c7-9a7e-9b7f10cbb411.png)
- [https://www.clariontech.com/blog/an-effective-social-authentication-solution-with-auth0](https://www.clariontech.com/blog/an-effective-social-authentication-solution-with-auth0)

- Does not work on native (Android/IOS) platform
- Third party cookies must be enabled (Will not work on brave, latest version of safari)
- both applications must either use embedded login or universal login

### Limitations
1. [CORS](https://auth0.com/docs/authenticate/login/cross-origin-authentication#limitations)
2. [Salesforce](https://help.salesforce.com/s/articleView?id=sf.external_identity_login_all_steps.htm&type=5)

### FAQ

- [how-do-i-configure-sso-single-sign-on-with-auth0](https://community.auth0.com/t/how-do-i-configure-sso-single-sign-on-with-auth0/82450)
- [embedded-with-custom-domain-vs-universal-login](https://community.auth0.com/t/embedded-with-custom-domain-vs-universal-login/26094)
- [single page app sso](https://auth0.com/docs/troubleshoot/product-lifecycle/past-migrations/migrate-from-embedded-login-to-universal-login#single-page-apps)


## [API Endpoint: auth0.com/docs/api ](https://auth0.com/docs/api)


## [Auth0.js](https://auth0.com/docs/libraries/auth0js#using-checksession-to-acquire-new-tokens)
## [SSO Auth0.js](https://auth0.com/docs/libraries/auth0js#single-sign-on-with-embedded-authentication)

## [Lock API](https://auth0.com/docs/libraries/lock/lock-api-reference)

