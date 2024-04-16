# Quest 3 - Use Copilot Studio and create a Power Automate Flow

[ < Quest 2 ](quest2.md) - **[ Quest 4 > ](quest4.md)**

Use Copilot Studio and create a Power Automate Flow
During this quest you will create a Copilot in Copilot Studio and connect to SAP system ES5 via Power Automate Flow. 

* Open `Incognito Tab` in your Browser                           
 ![Sign In](../media/quest3/1-Incognito.png)

* Open https://copilotstudio.microsoft.com/
* User: your Group User
* Microsoft Authenticator registration might be needed

* Use an environment located in the US!  - and select `Get Started`
 ![Sign In](../media/quest3/2-GetStarted.png)



* Select `Done`
![Sign In](../media/quest3/3-PowerVirtualAgent-is-now-MicrosoftCopilotStudio.png)



* Enter "Copliot Name" and an "external website" e.g. https://www.sap.com to crawl
* and select "Create"
 ![Sign In](../media/quest3/4-CreateCopilot.png)


* Select "Skip"                              
 ![Sign In](../media/quest3/5-NewFeatures.png)

* Select "Ask your Copilot a question e.g. `Tell me about SAP`"
 ![Sign In](../media/quest3/6-MySAPCopilot.1.png)

* Copilot will use information from the given website to answer
* Copilot will give references where the information is coming from              
 ![Sign In](../media/quest3/7-MySAPCopilot.2.png)

* Select Settings
* Select Generative AI
* Enable "Dynamic chaining with generative actions"
* Click `Save`
 ![Sign In](../media/quest3/9-MySAPCopilot-Settings.png)

* Select "Actions"
* `Add an action`
 ![Sign In](../media/quest3/10-MySAPCopilot-Actions.png)


* Scroll down and select "New Action" => "Create a new flow"
 ![Sign In](../media/quest3/11-MySAPCopilot-AddAnAction.png)


* Select `Get started`                   
 ![Sign In](../media/quest3/12-PowerAutomateGetStarted.png)


* Select `Respond to Copilot`
 ![Sign In](../media/quest3/12-PowerAutomate-Run-a-flow-from-Copilot.png)


* Select `Add an output`
 ![Sign In](../media/quest3/13-PowerAutomate-AddAnOutput.png)


* Select `Text`                      
 ![Sign In](../media/quest3/14-PowerAutomate-AddAnOutput-Text.png)


* Enter name `ReturntoCopilot`
* Select `+` above `Respond to Copilot`
* Select `Add an action`
 ![Sign In](../media/quest3/15-PowerAutomate-AddAnAction.png)


* Search for `Variable`
* Select `See more`
* Select `Initialize Variable`                                       
 ![Sign In](../media/quest3/16-PowerAutomate-AddAnAction2.png)


* Provide a Name
* Select Type `String`
* Provide `Initial Value`
* Select `Respond to Copilot`
 ![Sign In](../media/quest3/17-PowerAutomate-Provide-a-Name.png)


* Click into `Enter a value to respond with`
* Click the `flash`
 ![Sign In](../media/quest3/18-PowerAutomate-ValueToRespond.png)


* Select your `ReturnVariable`
 ![Sign In](../media/quest3/19-PowerAutomate-ReturnVariable.png)


* Change the flow name and make it unique
 ![Sign In](../media/quest3/20-PowerAutomate-AddAnOutput.png)


* Click `Save draft`
* Click `Publish`
 ![Sign In](../media/quest3/21-PowerAutomate-Publish.png)


* Switch back to Copilot Studio
* Refresh the available actions
 ![Sign In](../media/quest3/22-BackToCopilot.png)


* Scroll down the list of actions and select your flow
 ![Sign In](../media/quest3/23-Copilot-SelectYourFlow.png)

* Select `Next`


* Edit Action Details
* Edit the Model Description: `This flow returns product information from the SAP system`
* Select "Back"
 ![Sign In](../media/quest3/25-Copilot-ConnectionDetails-2.png)


* Scroll down to `Outputs` and select `Edit`
* Select `Add`
* Select our `ReturntoCopilot` output variable
* Click `Save`
* Click `Finish`
 ![Sign In](../media/quest3/26a-Copilot-Output.png)


 * Click your action `Run a flow from Copilot - TechReady`
 ![Sign In](../media/quest3/26b-Copilot-Action.png)


 * Test our CoPilot again `show me product information from SAP`
 * This time we receive information from Power Automate Flow
 ![Sign In](../media/quest3/27-Copilot-TestYourCopilot.png)


 * Switch back to the Power Automate Flow tab
 * Click on `Run a flow from Copilot`
  ![Sign In](../media/quest3/27a-AutomateFlow-Input1.png)


 * Select `+ Add an input`
 * Select `Text`
 * Write `ProductID` as Input
 ![Sign In](../media/quest3/27c-AutomateFlow-Input3.png)


 * Select the "+" above `Initialize variable` and select `Add an action`
 ![Sign In](../media/quest3/28-AutomateFlow-AddAnAction2.png)



 * Search for the `odata` connector, scroll down the list and select the `Read OData entity` connector
  ![Sign In](../media/quest3/29-AutomateFlow-odata-Connector.png)


 * Select Odata Entity Name `ProductSet` from drop down menu
 * Click into `ProductID` field and select the `flash` 
  ![Sign In](../media/quest3/30-AutomateFlow-odata-Parameter.png)



 * Select `ProductID` from drop down menu
  ![Sign In](../media/quest3/30b-AutomateFlow-odata-ProductID.png)



 * Fill the fields
 * URI: `https://sapes5.sapdevcenter.com/sap/opu/odata/iwbep/GWSAMPLE_BASIC`
 * Authentication Type: `Basic`
 * User: `P********`
 * PW: `************`
 * Click `Safe draft`
  ![Sign In](../media/quest3/30c-SAP-odata-connection.png)



 * xxx
 ![Sign In](../media/quest3/xxx)


 * xxx
 ![Sign In](../media/quest3/xxx)





* xxx
 ![Sign In](../media/quest3/xxx)













* Once you have uploaded several documents, restart the conversation and ask the bot some related questions 
> [!NOTE]
> Even if the document has been uploaded in English, you can still ask it with different languages
![Sign In](../media/quest3/04-ChatWithYourData.png)
e.g. `Wie war das Quartalsergebnis von SAP?` oder
"vergleiche das Quartalsergebnis von SAP mit Microsoft" und 
"wie war der Cloud Umsatz von SAP?"
![Sign In](../media/quest3/05-MoreChats.png)


* Feel free to publish the Chatbot following the steps in the previous quest


## Where to next?
[ < Quest 2 ](quest2.md) - **[ Quest 4 > ](quest4.md)**

[🔝](#)
