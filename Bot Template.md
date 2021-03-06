# Walkthrough to building a bot using Bot Connector .Net template
Download the open source bot builder SDK
```markdown
https://dev.botframework.com/ 
```
Getting Started
``` markdown
Follow the instructions from the provided link or follow my instructions. Note that my instructions are for 
the people that are newer and require a little more guidance.

https://docs.botframework.com/en-us/csharp/builder/sdkreference/gettingstarted.html

Instructions:
1) Install Visual Studio 2017 from www.visualstudio.com
2) Download and Install Bot Application template from http://aka.ms/bf-bc-vstemplate

* Note: Once the Bot Application zip file is downloaded, be sure to move it to the Visual Studio 2017 
  template directory
  
\...\Documents\Visual Studio 2017\Templates\ProjectTemplates\Visual C#\

3) Open Visual Studio 2017, select File > New > Projects > Visual C# > Bot Application

* Note: Don't worry if you see only 1 Bot Application template

4) Name your first Bot and select OK
```
![botapppic0](https://cloud.githubusercontent.com/assets/25268970/23716194/4e597436-03fd-11e7-9117-0353362e6ed9.png)

```markdown
5) A new window will appear, look to the right hand side and locate the Controllers folder. Click the arrow 
  next to the folder to expand the folder. Double click on MessageContrller.cs to open it in a new tab. 

6) Next, locate Web.config and double click it to open it in another new tab.
```
![botapppic1](https://cloud.githubusercontent.com/assets/25268970/23715743/a670f2fe-03fb-11e7-983a-254a44fb971f.png)
```markdown
MessagesController.cs
```
![botapppic2](https://cloud.githubusercontent.com/assets/25268970/23719750/968403b8-040a-11e7-99e0-5557f629d6ae.png)

```markdown
The MessagesController.cs is the core functionality of the Bot Template. In this case the code takes the 
message text for the user, then creates a reply message using the CreateReplyMessage function. You can 
modify this template to add more functions.
```
```markdown
Web.config
```
![botapppic3](https://cloud.githubusercontent.com/assets/25268970/23720193/0b416cbc-040c-11e7-9e9a-4d9d5d0d4bb6.png)

```markdown
* Note the highlighted. There are 3 values that can be filled in 
  (botID, MicrosoftAppID, and MicrosoftAppPassword)
  
  The botID reflects what I called my project; Smart bot
  MicrosoftAppID and MicrosoftAppPassword must be created while you are registering your bot.
  
  However, if you are only running your bot locally then this information can be left blank.
  
  7) Register your bot; locate this tab at the top of the window.
```

![botapppic4](https://cloud.githubusercontent.com/assets/25268970/23720923/3512bee0-040e-11e7-863a-b7c7f50f958e.png)

```markdown
8) Fill it out the registration form
I filled the following sections with information: Name, Bot handle, and Description.

Name > Smart bot
Bot handle > 'must be unique identifier e.g. Smart_bot_12345 or GSU_Smart_bot'
Description > About your bot, its functionality, where your code was adapted from, etc...

9) Select Create Microsoft App ID and password; Copy this information into Web.config in their 
  designated place holders. Then save the document.
  
10) Download the Bot Framework Channel Emulator from 
  https://docs.botframework.com/en-us/tools/bot-framework-emulator/

11) Download ngrok from https://ngrok.com/download
* Note: this download will allow you to connect your bot pass your firewall to the internet. 
  After dowloading, unzip and click the file. A command prompt will open, 
  type in ngrok. exe http 80. Another note, make sure that you are in the same directory where 
  the ngrok file is located.
```

![botapppic5](https://cloud.githubusercontent.com/assets/25268970/23722373/1bd7b75a-0413-11e7-8e47-27c55a57619b.png)

```
12) Go back to your Microsoft Visual Studio 2017, click on the tab that indicates your bot name. 
  Click File in the upper left-hand corner. Then click, View in Browser. Or another quick option is 
  Ctrl-Shift-W.
  
  * Note: A new tab will open in your browser. You will need 2 pieces of information from this tab.
    1) locathost: ####
    2) https://your_bots_hostname/api/messages
```
![botapppic6](https://cloud.githubusercontent.com/assets/25268970/23722626/193617b6-0414-11e7-9623-080c61e23654.png)

```
13) Now open your Bot Framework-Emulator. Take the password that your generated for you application 
  in addition to the 2 pieces of information that was retrieved from Step 12 (local address and 
  MicrosoftAppID); and apply this information to the designated fields in the emulator. 
  Select Connect.
```
![botapppic7](https://cloud.githubusercontent.com/assets/25268970/23731343/fb16d10e-043a-11e7-8542-43eee5c9b511.png)

```
14) Finally, test if your application works. Type Hello or any number of characters. The return should 
  be the number of elements that has been executed.
  
  * Note: The count includes spaces.

