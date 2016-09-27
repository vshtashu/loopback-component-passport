# loopback-component-passport

**NOTE: This module supersedes [loopback-passport](https://www.npmjs.org/package/loopback-passport). Please update your package.json accordingly.**

The module provides integration between [LoopBack](http://loopback.io) and
[Passport](http://passportjs.org) to support third-party login and account 
linking for LoopBack applications.

<img src="./ids_and_credentials.png" width="600px" />

> Please see the [official documentation](http://docs.strongloop.com/pages/viewpage.action?pageId=3836277) for more information.

## All local accounts requires verification

### Enhancements provided to stock loopback-component-passport

Allows email from social media accounts to be set as username and email in user model.
** Works in userIdentity model for now.

Just add  "emailAsUserEmail": true &  "emailAsUsername": true in providers.json similar to profileUrl as in case of facebook as :

```
    "profileURL": "https://graph.facebook.com/v2.7/me?fields=name,first_name,middle_name,last_name,gender,email,birthday,picture,cover,verified",
```

Addition of profile data in user model. Support for complete profile or selective profile field described as "profileField".
** Works in userIdentity model for now.

```
    "addInProfiles": {
      "profileField": "_json"   // optional if not required pass empty object
    }
```