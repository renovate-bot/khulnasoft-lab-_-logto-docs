---
sidebar_position: 9
---

# 🌍 Custom domain

You can use your own domain name for your Logto tenant. This feature lets you present a consistent brand by having your own domain name on the sign-in and registration pages, as well as on the Management API.

:::note
Please note, this custom domain feature is exclusively available for Logto Cloud.
:::

## Advantages of Using a Custom Domain

By using your own domain name for your Logto tenant, you'll benefit from several advantages:

- Branding and Trust: Your users will see your domain name in the browser's address bar when they sign in to your application. By avoiding redirects to a third-party domain site, your users are provided with a sense of security and trust.
- Versatility: Having a sub-domain can be beneficial if you wish to use your own wildcard SSL certificate, cross-domain cookies, or if you need to utilize iframes.

## How Does it Work?

Logto uses a [CNAME record](https://en.wikipedia.org/wiki/CNAME_record) to map your domain name to the Logto domain name, and will subsequently generate an SSL certificate for your domain name automatically.

The custom domain will exist in conjunction with the default Logto domain name. This gives you the flexibility to use either domain name when initiating the authentication process.

## Frequently Asked Questions

### Is it possible to use a bare domain?

Bare domains, also known as "naked domains", "APEX domains" or "root domains", are domains without a prefix, such as `example.com`. Unfortunately, Logto does not support the use of bare domains for now. You are required to use a sub-domain, like `auth.example.com`.

### Can I use self-managed SSL certificates?

Logto does not support self-managed SSL certificates for now. An SSL certificate for your domain name will be generated by Logto automatically.

### Will users need to re-authenticate when switching to a custom domain?

Users will be able to maintain their authenticated state even when switching to a custom domain, and the custom domain will be visible during the next authentication process.