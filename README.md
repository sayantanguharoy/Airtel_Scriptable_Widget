![airtel-widget](https://user-images.githubusercontent.com/43070628/145957412-053c6f1a-e226-44b5-92d4-ff42425fa662.jpg)


# Airtel Widget for iOS
iOS widget that shows airtel daily data usage using [Scriptable](https://scriptable.app) app.

### Setup:
NOTE: Setting up widget (getting Airtel API auth data) is HARD, but its one time process.

### Setup widget:
* Add widget to Scriptable app.
* On line 1, `const dailyDataLimit = 3072` change it with your daily limit in MB (1 GB = 1024 MB)
* On widget parameter, add you mobile number (as in screenshot below)
<img src="https://user-images.githubusercontent.com/43070628/145957438-8ca210a1-8abf-4d06-8753-ec8fa7d00112.jpg" width=360>

### Get Airtel API authentication data:
* Proxy Airtel Thanks and get authentication for Airtel API (Endpoint: `https://myairtelapp.bsbportal.com/app/guardian/api/services/v1/prepaid?&siNumber=yourNumber`) (You can check how to proxy iOS app on youtube)
* From that endpoint get header value for (user-agent, X-Bsy-Utkn, X-Bsy-Did, X-Bsy-Dt)
* Create `AirtelAuth.json` file in Scriptable folder in files app and save data in following format:
```json
{
    "us": "Value for user-agent",
    "tk": "Value for X-Bsy-Utkn",
    "id": "Value for X-Bsy-Did",
    "dt": "Value for X-Bsy-Dt"
}
```

Thats it.

widget design credit: [sillium](https://gist.github.com/Sillium/313164aec3d835c076ebfcd330f1be14)
