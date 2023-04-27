## Setup

### Create Azure OpenAI Service resource in Azure Portal

1. Open the Microsoft Azure Portal at https://portal.azure.com and sign in to your Azure Subscription. Make sure you are viewing the Home page of the Azure portal by clicking the hamburger menu in the top-left and selecting "Home".

2. Click "+ Create a Resource"

3. In the search box, type "openai" and select "Azure OpenAI"

4. Click the "Azure OpenAI" pane, and then click "Create". (Leave the "Plan" field as "Azure OpenAI".)

NOTE: If you see the message in red, "Azure OpenAI Service is currently available to customers via an application form. The selected subscription has not been enabled for use of the service and does not have quota for any pricing tiers.", you need to apply for access to the service and wait for approval to continue. [Click here to request access to Azure OpenAI service](https://aka.ms/oai/access).

5. Choose a unique set of characters to make your resource group and domain name unique. You might choose something like `openai-19800101` with your birthday to make it easy to remember. From now on, we'll use `openai-lab-build`, but remember to substitute your selection from now on.

5. Complete the "Basics" tab as follows

  * Subscription: leave unchanged
  * Resource Group: Click "create new" and enter `openai-lab-build` 
  * Region: Select `South Central US`
  * Name: Enter `openai-lab-build`
  * Pricing Tier: Select `Standard S0`

6. Click the link "[Review the Azure OpenAI code of conduct](https://learn.microsoft.com/en-us/legal/cognitive-services/openai/code-of-conduct)" and read the code of conduct, then close the tab to return to the Azure Portal.

7. Click Next. On the next page "Tags" also click Next. On the final tab "Create Azure OpenAI", click "Create".

8. Deployment may take up to 2 minutes. Once deployment is complete, proceed to the next step.

### Create OpenAI Deployments

1. From the Azure Portal Home page, click the Resource you just created, `openai-lab-build`.

2. From the Overview tab, click the button "Explore" to launch the Azure OpenAI Studio.

3. You will see the message "No deployment detected". Click the "Deployments" link under "Management" in the left navigation.

4. Click "+ Create New Deployment". Complete the "Deploy Model" form as follows, then click "Create"

  * Model Name: Select `text-davinci-003`
  * Model version: Leave as `1`
  * Deployment Name: Enter `text-davinci-003`

5. Once more, click "+ Create New Deployment". Complete the "Deploy Model" form as follows, then click "Create"

  * Model Name: Select `gpt-35-turbo`
  * Model version: Leave as `0301`
  * Deployment Name: Enter `gpt-35-turbo`

Now, proceed to [1 Explore%20Models.md](1%20Explore%20Models.md) 