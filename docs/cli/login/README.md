# Logging into the CLI

To start using the Pipedream CLI, you'll need to link your Pipedream account to the CLI. If you don't yet have a Pipedream account, you can also sign up from the CLI.

[[toc]]

## Existing Pipedream account

Once you [install the CLI](/cli/install/), you'll need to link it with your Pipedream account.

If you already have a Pipedream account, run

```text
pd login
```

This will open up a new window in your default browser. If you're already logged into your Pipedream account in this browser, this will immediately link the CLI to this account, writing your API key for that account to your [`pd` config file](/cli/reference/#cli-config-file).

Otherwise, you'll be directed to login.

Once you're done, go back to your shell and you should see confirmation that your account is linked:

```text
> pd login
Logged in as dylburger (dylan@pipedream.com)
```

## Signing up for Pipedream via the CLI

If you haven't signed up for a Pipedream account, you can create an account using the CLI:

```text
pd signup
```

This will open up a new window in your default browser. You'll be asked to sign up for Pipedream here. Once you do, your account will be linked to the CLI, writing your API key for that account to your [`pd` config file](/cli/reference/#cli-config-file).

Once you're done, go back to your shell and you should see confirmation that your account is linked:

```text
> pd signup
Logged in as dylburger (dylan@pipedream.com)
```

## Logging out of the CLI

You can log out of the CLI by running:

```text
pd logout
```

This will remove your API key from the [`pd` config file](/cli/reference/#cli-config-file).

## Using the CLI to manage multiple accounts

If you have multiple Pipedream accounts, you can use [profiles](/cli/reference/#profiles) to ensure the CLI can manage resources for each.

<Footer />