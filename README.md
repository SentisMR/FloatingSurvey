# Sentis Floating Survey

This is a Google Tag Manager integration for deploying Sentis hosted surveys using the Floating Survey library.

## Implementation

### Step 1: Creating a Google Tag Account & Workspace

Note: if your developers have already integrated the google tag manager workspace into your website, you can skip ahead to Step 2

-	Sign into Google Tag Manager (GTM) at https://tagmanager.google.com/
-	Create a new GTM account by entering an appropriate name and selecting Canada under the country dropdown:
-	Enter a name under container setup and select web. We recommend using a name that represents the environment and domain that will be hosting the floating survey, ex: staging.acme.com.
-	Press create and read & accept the terms of service.
-	Copy the scripts from the popup and supply these to your developer/site maintainer to add to your website. This script allows your site to load the contents of a tag that is managed in the google tag manager portal. 
-	After pressing OK, you should now see your new Tag Manager Workspace.

### Step 2: Importing our Tag Template

Now that we have our workspace, the first thing we will do is import the Floating Survey Template. If a template file has not been provided, it can be retrieved from: https://github.com/SentisMR/FloatingSurvey.

Start by selecting Templates from the side menu. Under “Tag Templates” create a new template.
 
Import the Floating Survey Template (expand the top right corner menu and select import). 

If you are self-hosting the floating survey package, you will need to edit the imported template and add the location of the script under the “Injects Scripts” permissions. If you are not self-hosting the assets, the default Sentis CDN will be used.
Save the template. 

### Step 3: Creating our trigger
Start by selecting triggers from the side menu and press “New”. Click the trigger configuration to select from a list of default events to subscribe to. For our use case, we will select DOM Ready. This will ensure our tag is only loaded once your website is ready to go.
If you would like the floating survey to be available on all pages that your developers have made the Google Tab Script available on, select “All DOM Ready Events”. If you would like to be more specific about where the floating survey is available, select “Some DOM Ready Events” and specify your filters. ex: Page URL equals https://acme.com/info would make the Floating Survey available only on the /info page. You can find out more details about triggers here: https://support.google.com/tagmanager/answer/7679316?hl=en/

### Step 4: Creating our Tag
Select “Tags” in the side menu of your workspace and press “New”. 
In the editor popup, specify a name for the new tag. ex. Website Evaluation Survey. Once you have your name, click the “Tag Configuration” area and scroll down until you see the “Custom” section that should contain our previously imported Floating Survey tag and select it.
Enter the configuration details provided by Sentis for the survey being deployed. The only required values are Survey ID and Survey URL.  NOTE: You must provide Sentis with the domain for the site that will be hosting the floating survey. This domain must be added in the survey settings to set the required request headers related to the iFrame permissions. Your tag will not work unless this value is set.
Google automatically provides some advanced settings for each tag. In the Advanced Settings section, you can specify a timeframe your floating survey is available.

### Step 5: Reviewing and Publishing our new Tag
At the top of your workspace, it should now show that you have “Workspace Changes”.  Click Submit and review your changes under the Workspace Changes section. If everything is in order, give your commit a name and description, select the action you wish to do (save and publish or just save), then click Publish. If you chose to save and publish, your changes should now be reflected on your website after reloading your page.
NOTE: The top bar of your workspace has a versions tab. This tab will show you a history of changes made. If you do accidentally publish a mistake, you can revert your live tag to a previous version by selecting “Publish” under the desired version. If you wish to restore a previous version as the latest, select “Set as Latest Version”. Once set, you may need to “Publish” the new version that is created. 

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