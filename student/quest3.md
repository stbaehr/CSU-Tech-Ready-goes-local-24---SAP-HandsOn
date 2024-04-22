# Quest 3 - Use Copilot Studio and create a Power Automate Flow

[ < Quest 2 ](quest2.md) - **[ Quest 4 > ](quest4.md)**

Use Copilot Studio and create a Power Automate Flow
During this quest you will create a Copilot in Copilot Studio and connect to SAP system ES5 via Power Automate Flow. 


* Open an Incognito Tab in your Browser            
 ![Sign In](../media/quest3/1-Incognito.png) <br>


* Open https://copilotstudio.microsoft.com/
* User: your Group User
* If appears - close `Contact Information` screen with the `X`
 ![Sign In](../media/quest3/0-Contact-Info.png) <br>

* Use an environment located in the US!
 ![Sign In](../media/quest3/2-GetStarted.png) <br>


* Select `Done`
 ![Sign In](../media/quest3/3-PowerVirtualAgent-is-now-MicrosoftCopilotStudio.png) <br>


* Enter "Copliot Name" and an "external website" e.g. https://www.sap.com to crawl
* and select "Create"
 ![Sign In](../media/quest3/4-CreateCopilot.png) <br>


* Select "Skip"                              
 ![Sign In](../media/quest3/5-NewFeatures.png) <br>

* Select "Ask your Copilot a question e.g. `Tell me about SAP`"
 ![Sign In](../media/quest3/6-MySAPCopilot.1.png) <br>

* Copilot will use information from the given website to answer
* Copilot will give references where the information is coming from              
 ![Sign In](../media/quest3/7-MySAPCopilot.2.png) <br>

* Select Settings
* Select Generative AI
* Enable "Dynamic chaining with generative actions"
* Click `Save`
 ![Sign In](../media/quest3/9-MySAPCopilot-Settings.png) <br>

* Select "Actions"
* `Add an action`
 ![Sign In](../media/quest3/10-MySAPCopilot-Actions.png) <br>


* Scroll down and select "New Action" => "Create a new flow"
 ![Sign In](../media/quest3/11-MySAPCopilot-AddAnAction.png) <br>


* Select `Get started`                   
 ![Sign In](../media/quest3/12-PowerAutomateGetStarted.png) <br>


* Select `Respond to Copilot`
 ![Sign In](../media/quest3/12-PowerAutomate-Run-a-flow-from-Copilot.png) <br>


* Select `Add an output`
 ![Sign In](../media/quest3/13-PowerAutomate-AddAnOutput.png) <br>


* Select `Text`                      
 ![Sign In](../media/quest3/14-PowerAutomate-AddAnOutput-Text.png) <br>


* Enter name `ReturntoCopilot`
* Select `+` above `Respond to Copilot`
* Select `Add an action`
 ![Sign In](../media/quest3/15-PowerAutomate-AddAnAction.png) <br>


* Search for `Variable`
* Select `See more`
* Select `Initialize Variable`                                       
 ![Sign In](../media/quest3/16-PowerAutomate-AddAnAction2.png) <br>


* Provide a Name
* Select Type `String`
* Provide `Initial Value`
* Select `Respond to Copilot`
 ![Sign In](../media/quest3/17-PowerAutomate-Provide-a-Name.png) <br>


* Click into `Enter a value to respond with`
* Click the `flash`
 ![Sign In](../media/quest3/18-PowerAutomate-ValueToRespond.png) <br>


* Select your `ReturnVariable`
 ![Sign In](../media/quest3/19-PowerAutomate-ReturnVariable.png) <br>


* Change the flow name and make it unique
 ![Sign In](../media/quest3/20-PowerAutomate-AddAnOutput.png) <br>


* Click `Save draft`
* Click `Publish`
 ![Sign In](../media/quest3/21-PowerAutomate-Publish.png) <br>


* Switch back to Copilot Studio
* Refresh the available actions
 ![Sign In](../media/quest3/22-BackToCopilot.png) <br>


* Scroll down the list of actions and select your flow
 ![Sign In](../media/quest3/23-Copilot-SelectYourFlow.png) <br>

* Select `Next`


* Edit Action Details
* Edit the Model Description: `This flow returns product information from the SAP system`
* Select `Back`
 ![Sign In](../media/quest3/25-Copilot-ConnectionDetails-2.png) <br>


* Scroll down to `Outputs` and select `Edit`
* Select `Add`
* Select our `ReturntoCopilot` output variable
* Click `Save`
* Click `Finish`
 ![Sign In](../media/quest3/26a-Copilot-Output.png) <br>


 * Click your action `Run a flow from Copilot - TechReady`
 ![Sign In](../media/quest3/26b-Copilot-Action.png) <br>


 * Test our CoPilot again `show me product information from SAP`
 * This time we receive information from Power Automate Flow                 
 ![Sign In](../media/quest3/27-Copilot-TestYourCopilot.png) <br>


 * Switch back to the Power Automate Flow tab
 * Click on `Run a flow from Copilot`                            
  ![Sign In](../media/quest3/27a-AutomateFlow-Input1.png) <br>


 * Select `+ Add an input`
 * Select `Text`
 * Write `ProductID` as Input                                
 ![Sign In](../media/quest3/27c-AutomateFlow-Input3.png) <br>


 * Select the "+" above `Initialize variable` and select `Add an action`
 ![Sign In](../media/quest3/28-AutomateFlow-AddAnAction2.png) <br>



 * Search for the `odata` connector, scroll down the list and select the `Read OData entity` connector
  ![Sign In](../media/quest3/29-AutomateFlow-odata-Connector.png) <br>


 * Select Odata Entity Name `ProductSet` from drop down menu
 * Click into `ProductID` field and select the `flash` 
  ![Sign In](../media/quest3/30-AutomateFlow-odata-Parameter.png) <br>



 * Select `ProductID` from drop down menu                        
  ![Sign In](../media/quest3/30b-AutomateFlow-odata-ProductID.png) <br>

 <br>

 * Fill the fields <br>
        URI: `https://sapes5.sapdevcenter.com/sap/opu/odata/iwbep/GWSAMPLE_BASIC` <br>
        Authentication Type: `Basic` <br>
        User: `P********` <br>
        PW: `************` <br>
 * Click `Safe draft`                            
  ![Sign In](../media/quest3/30c-SAP-odata-connection.png) <br>



 * Select "Initialize variable"
 *  Click into the Value field, delete the text in the field and select the `flash`
   ![Sign In](../media/quest3/31-AutomateFlow-ReturnInfo.png) <br>


 * Click `See More` near to `Read Odata entity`
 * Select `Name`, `Price` and `Description`
 ![Sign In](../media/quest3/32-AutomateFlow-ReturnInfo2.png) <br>



 [!NOTE]
> Note: Your SAP Product Copilot and Power Automate Flow are configured and you go on to Quest 4 





## Where to next?
[ < Quest 2 ](quest2.md) - **[ Quest 4 > ](quest4.md)**

[🔝](#)
