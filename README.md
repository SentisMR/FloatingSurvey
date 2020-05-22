# Sentis Floating Survey

This is a Google Tag Manager integration for deploying Sentis hosted surveys using the Floating Survey library.

## Implementation

Import the Sentis Floating Survey template from the Google Tag Manager Community Template gallery.

- Sign in to the Google Tag Manager interface.

- Click the Templates tab in the left side navigation bar.

- Click the Search Gallery button in the Tag Templates slot. Use the Search box to find the template.

    - In the search box, enter Sentis Floating Survey.

- Select the Sentis Floating Survey template, and then click Add to workspace.

- Agree to the permissions required by the custom template.

If successful, the template should be available for use in the Tag Templates section. You can now deploy your survey using the template.

The template displays in the template list.

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