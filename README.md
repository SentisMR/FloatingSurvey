# Sentis Floating Survey

This is a Google Tag Manager integration for deploying Sentis hosted surveys using the Floating Survey library.

## Google Tag Fields

| Name| Type | Required | Default Value | Description |
| --- | --- | --- | --- | --- |
| Survey ID | Integer | True |   | Unique ID for the survey to render |
| Survey URL | String | True |   | Domain where the survey is hosted |
| Title| String | False | Empty | Survey window title |
| Call-to-action text | String | False | Empty | Call to action text |
| Floating Window Colour | String | False | Empty | Specify the hex or rgb background colour for the floating window and call-to-action |
| Floating Window Font Family | String | False | Empty | Specify the font family for the floating window and call-to-action |
| Asset URL | String | False | Sentis CDN | Root URL path of image assets |
| Enable Call-to-action Animation | Boolean | False | True | Enable/Disable launcher animation if user is inactive in survey |
| Display Sentis Branding | Boolean | False | True | Show/Hide footer branding |