# Authentication

When you sign up for Pipedream, an API key is generated for your account. You can use this key to authorize requests to the API.

You can find this API key in your [Account Settings](https://pipedream.com/settings/account) (**Settings** -> **Account**).

[[toc]]

## Authorizing API requests

Pipedream uses [Bearer Authentication](https://oauth.net/2/bearer-tokens/) to authorize your access to the API. When you make API requests, pass an `Authorization` header of the following format:

```text
Authorization: Bearer <api key>
```

For example, here's how you can use `cURL` to fetch profile information for the authenticated user:

```bash
curl 'https://api.pipedream.com/v1/users/me' \
  -H 'Authorization: Bearer <api_key>'
```

## Using the Pipedream CLI

If you're using [the CLI](/cli/reference/) to interact with Pipedream, you can [link the CLI to your Pipedream account](/cli/login/). This will automatically pass your API key with every API request.

## Revoking your API key

You can revoke your API key in your [Account Settings](https://pipedream.com/settings/account) (**Settings** -> **Account**). Click on the **REVOKE** button directly to the right of your API key.

This will revoke your original API key, generating a new one. Any API requests made with the original token will yield a `401 Unauthorized` error.

<Footer />