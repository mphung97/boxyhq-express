# SAML Jackson + Express.js Example App

This demo app shows how to add SAML SSO to a Express.js app using SAML Jackson.

## Setup the app
Please follow the below instructions.

### Setup Database

```bash
# Generate a private/public key combination, this is needed for signing the SAML AuthnRequest
# openssl req -x509 -newkey rsa:2048 -keyout key.pem -out public.crt -sha256 -days 365000 -nodes
# Base64 encoded value of public key `cat public.crt | base64`
PUBLIC_KEY=
# Base64 encoded value of private key `cat key.pem | base64`
PRIVATE_KEY=

docker compose up --build -d
```

### Install dependencies

```bash
npm install
```

### Setup environment

Update the `apps/express/.env` with your own values.

### Run the app

```bash
npm run dev:express
```

### Setup SAML SSO

[Mock SAML](https://mocksaml.com)

## Contributing

Thanks for taking the time to contribute! Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make will benefit everybody and are very appreciated.

Please try to create bug reports that are:

- _Reproducible._ Include steps to reproduce the problem.
- _Specific._ Include as much detail as possible: which version, what environment, etc.
- _Unique._ Do not duplicate existing opened issues.
- _Scoped to a Single Bug._ One bug per report.

## Community

- [Discord](https://discord.gg/uyb7pYt4Pa) (For live discussion with the Community and BoxyHQ team)
- [Twitter](https://twitter.com/BoxyHQ) (Get the news fast)
