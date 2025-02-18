<img src="https://uploads-ssl.webflow.com/61e714dee6e03a006b829c3a/621cf6cde8ae4f61b08896b4_MORF%20Logo.svg" width="200" height="100" alt="Morf Logo">

# Authenticating with Morf Services

In order to use any Morf Service (API), you must provide a token for authentication.   This token is known as a `siteKey` and is tied to a specific domain. In the [Morf Editor](https://editor.getmorf.io), you'll notice the `siteKey` in the config section at the top of the Morf form JSON.

```
"config": {
    "submit": "",
    "siteKey": "4fbfd303f2f74c6ea2ec3bc9ab44d454",
    "successUrl": "",
    "theme": "",
    "externalId": ""
}
```

This siteKey (`4fbfd303f2f74c6ea2ec3bc9ab44d454`) is tied to the getmorf.io domain. You are prevented from rendering and submitting a Morf form using this `siteKey` on a domain other than `getmorf.io`. In order to render and submit forms on other domains, you'll need to [request a valid siteKey](#requesting-a-sitekey) that is tied to that domain.

## Authentication Mechanisms

There are two ways of using the `siteKey` token.  
* as part of an API call where the token is present in the header; and 
* as part of a query where the token is present as a parameter in the URL.
    
## Requesting a siteKey

In order to request a `siteKey`, email the Morf team at [support@getmorf.io](mailto:support@getmorf.io?subject=Morf%20siteKey%20Request).  

You'll need to provide: 
* your name;
* your organization's name; and
* a valid domain(s) from where the `siteKey` will be used.

Any form submissions using this `siteKey` will consume one of your organization's licensed submission transactions. If you are using the Morf free trial a submission will consume one of your 1,000 free transactions.

Once you recieve your `siteKey`, use it to replace the `siteKey` in the config section of your form or in any queries to Morf services.
