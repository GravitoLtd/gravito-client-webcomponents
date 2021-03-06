# Getting Started

Any application that uses Gravito As their identity provider should be registered as a customer with Gravito.Click [here](https://docs.gravito.net/) to know how to Register with Gravito.
On succesfull registeration you will get your client config. details Create an window scope object by name **gravitoWC_identityConfig** with this config inside the index.html page of your web app.

```html
<script>
  window.gravitoWC_identityConfig = {
    client_id: "client_id",
    grant_type: "client_credentials",
    scope: "API",
  };
</script>
```

Then install the library by placing following tag inside the index.html. make sure you create config object before loading the script.

```
<script src="https://cdn.gravito.net/webcomponents/webcomponent.js"></script>
```

Now you place the login web-components where you want to use them.

```html
<!-- TO LOGIN WITH GOOGLE -->
<gravito-google-button
  appid="YOUR_GOOGLE_CLIENT_ID.apps.googleusercontent.com"
  redirecturl="URL_TO_REDIRECT_AFTER_LOGIN"
  buttontext="Login with google"
>
</gravito-google-button>

<!-- TO LOGIN WITH FACEBOOK -->
<gravito-fb-button
  appid="YOUR_FACEBOOK_APPID"
  redirecturl="URL_TO_REDIRECT_AFTER_LOGIN"
  buttontext="Login with facebook"
>
</gravito-fb-button>

<!-- TO LOGIN USING GRAVITO MAGICLINK -->
<gravito-magiclink-button redirecturl="URL_TO_REDIRECT_AFTER_LOGIN">
</gravito-magiclink-button>
```

# Example

![Preview](https://gravitocdn.blob.core.windows.net/logos/webcomponetsdocs.PNG)
