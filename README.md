# Getting Started

Any application that uses Gravito As their identity provider should be registered as a customer with Gravito.Click [here](https://docs.gravito.net/) to know how to Register with Gravito.
On succesfull registeration you will get your client config. details Create an window scope object by name __gravitoWC_identityConfig__ with this config inside the index.html page of your web app.
```
<script>

window.gravitoWC_identityConfig  = {
	client_id: 'client_id',
	client_secret: 'client_secret',
	grant_type: 'client_credentials',
	scope: 'API',
	authority: 'https://dev-identity.gravito.net'
}

</script>
```

Then install the library by placing following tag inside the index.html. make sure you create config object before loading the script.
```
<script src="https://gravitocdn.blob.core.windows.net/webcomponents/webcomponent.js"></script>
```
Now you place the login web-components where you want to use them.
```
<!-- TO LOGIN WITH GOOGLE -->
<gravito-google-button 	
	appid="YOUR_GOOGLE_CLIENT_ID.apps.googleusercontent.com" 
	redirecturl="URL_TO_REDIRECT_AFTER_LOGIN" 
	gravitoendpointurl="https://dev-api.gravito.net/api" 
	buttontext="Login with google">
</gravito-google-button>

<!-- TO LOGIN WITH FACEBOOK -->
<gravito-fb-button 
	appid="YOUR_FACEBOOK_APPID" 
	redirecturl="URL_TO_REDIRECT_AFTER_LOGIN" 
	gravitoendpointurl="https://dev-api.gravito.net/api" 
	buttontext="Login with facebook">
</gravito-fb-button>

<!-- TO LOGIN USING GRAVITO MAGICLINK -->
<gravito-magiclink-button 
	redirecturl="URL_TO_REDIRECT_AFTER_LOGIN"
	gravitoendpointurl="https://dev-api.gravito.net/api">
</gravito-magiclink-button>
```
# Example
![alt text](https://gravitocdn.blob.core.windows.net/logos/gitHubDoc.PNG)