# SAML Testing SP/IdP

Online version available at: https://samlmock.dev (_Provided by Thameera_)

## Running the App

**Node.js is required to be able to run the app**

To launch the SAML Testing app run the following commands on the root dir:

```bash
npm i
npm run dev
```

After the first run, the app can be started with the `npm run dev` command

The WebUI for the will be available at [http://localhost:3333](http://localhost:3333).

## SP-Mode Instructions

### Okta IdP Configuration

Before any testing it is required to setup the IdP side of things.

The following config allows for basic SSO from Okta:

- _Single Sign-on URL_ > http://localhost:3333/callback
- _Audience URI_ > saml-mock
- _Name ID format_ > Unspecified

All parameters are specific to the Okta IdP and may not correlate with other IdPs

**NOTE:** SAML Request signature validation can be set up but it may not work as expected with Okta

### Doing a SAML flow

1. Set the `Identity Provider SSO URL` obtained from Okta on the "View SAML Setup instructions" as the `Sign-in URL`
2. Change any variables and request template as required.
3. Click submit on top-right.
4. Log in on the Okta's org login page if prompted.
5. The callback page will show the received SAML response from Okta.
6. Optionally, click the button to inspect the response in samltool.io.
7. Optionally, click the Log Out button to send a Logout Request to the IdP.

If you click on the Log Out button you will be redirected to a screen where you can edit this request.

## IdP-Mode Instructions

Not tested yet
