
# DogeCash API collection

The `collection.json` file includes all the DogeCash API endpoints and it can be imported into [Insomnia](https://insomnia.rest), an open source API requests tool. It should be compatible with Postman as well.

## HMAC-SHA256 authentication

The API uses HMAC-SHA256 authentication, as Insomnia doesn't provide this auth method by default, we made a plugin that will handle all the signing for you.

To install it, in Insomnia, go `Settings > Plugins` and install the following NPM package: `@dogecash/insomnia-plugin-dogecash-signature-generator`.

Once installed and enabled, in your DogeCash API collection add the following environment:
```json
{
	"url": "https://api.dogecash.net/api",
	"public": "e413d45eba7b07cb445ccf345f61855ef67a32d9a96a4c00c6f2aaafef6b9778",
	"dogecashSignature": {
		"enabled": true,
		"secret": "09e96a7a3a4069fee4dc952d3bdd03cf2aefb79c2ec258d10341283d6b4af087bca774603c7b40ce4b664490ceec6b2fa66e30e3677cc346033255269911627a"
	}
}
```

Being `public` your public API key, and `secret` your secret key.

Now you should be ready to try out the API!

## Help

If you find any issues, feel free to join our [Discord](https://discord.gg/xRSCZ6N8fH) and open a ticket. We'll be happy to help.