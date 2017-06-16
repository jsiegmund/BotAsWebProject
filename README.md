# FunctionsAsWebProject
Example of a Bot Service instance in a web app project for Azure Functions use

## Prerequisites 

Install the Azure Functions CLI, either through [Visual Studio Tools for Azure Functions](https://aka.ms/functionsvstools) or the Azure Functions CLI from npm [azure\-functions\-cli](https://www.npmjs.com/package/azure-functions-cli). 

## Local debugging in Visual Studio 

Since the project is a Web App, by default F5 will launch IIS Express. With a few simple changes to the project settings, you can run the Azure Functions CLI and attach a debugger: 

- Right-click **FunctionsAsWebProject** and open **Properties**. 
- In the **Web** tab, choose **Start External Program**
- For the program path, enter the path to `func.exe` for the Azure Functions CLI. 

  - If you've installed the [Visual Studio Tools for Azure Functions](https://aka.ms/functionsvstools), the path will look something like `C:\Users\USERNAME\AppData\Local\Azure.Functions.Cli\1.0.0-beta.93\func.exe`
  - If you've installed the Azure Functions CLI through NPM, the path will be something like `C:\Users\USERNAME\AppData\Roaming\npm\node_modules\azure-functions-cli\bin\func.exe`
- For **Command line arguments** set `host start`
- For Working directory, specify the root of the project `CoderCardsWebsite` on your machine.

![Start external program settings](http://blog.repsaj.nl/wp-content/uploads/2017/06/botasweb.png)
