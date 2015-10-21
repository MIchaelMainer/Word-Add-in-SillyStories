# Silly stories Word add-in sample: load files and use content controls

This Word add-in will show you how to:

1. Load a list of docx files from a service and populate a drop down box control with the file names as options.
2. Load a docx file from the service and insert it into the Word document.
3. Load the content control collection and create input boxes based on the content controls.
4. Update the text value of the content control collection based on the values in the input boxes.
5. Use Office UI Fabric to create a seamless Word user experience.

> Note: A giggle is a side effect of running this sample.

## Prerequisites

To use the Silly stories Word add-in sample, the following are required.

* [node.js](https://nodejs.org) to serve up the docx files.
* [npm](https://www.npmjs.com/) to install the dependencies.
* Word 2016, or any client that supports the Word Javascript API. This sample does a requirement check to see if it is running in a supported host.

## Configure the add-in and Word

1. Install project dependencies with Node's package manager (npm) by running ```npm install``` in the project's root directory on the command line.
2. Start the development server by running ```node server.js``` in the project's root directory. The add-in will be running at 127.0.0.1:8080.
3. Create a network share, or [share a folder to the network](https://technet.microsoft.com/en-us/library/cc770880.aspx) and place the [word-add-in-sillystories.xml](word-add-in-sillystories.xml) manifest file in it. 

You've deployed your add-in at this point. Now you need to let Word know where to find the add-in.

1. Launch Word and open a document.
2. Choose the **File** tab, and then choose **Options**.
3. Choose **Trust Center**, and then choose the **Trust Center Settings** button.
4. Choose **Trusted Add-ins Catalogs**.
5. In the **Catalog Url** box, enter the network path to the folder share that contains word-add-in-sillystories.xml and then choose **Add Catalog**.
6. Select the **Show in Menu** check box, and then choose **OK**.
7. A message is displayed to inform you that your settings will be applied the next time you start Office. Close and restart Word. 

## Run the add-in

1. Open a Word document. 
2. On the **Insert** tab in Word 2016, choose **My Add-ins**. 
3. Select the **Shared folder** tab.
4. Choose **Silly stories add-in**, and then select **Insert**.
5. The add-in will load in a task pane. See figure 1 to see how it will look when it gets loaded.
6. Select a story,  to have boilerplate text entered into the Word document.

__Figure 1. The Silly stories add-in loaded in Word__

![Picture of the Word application with the Silly stories add-in loaded](./readme-images/sillystoriesUI.PNG)

## Questions and comments

We'd love to get your feedback about the Silly stories Word add-in sample. You can send your questions and suggestions to us in the [Issues](https://github.com/OfficeDev/Word-Add-in-SIllyStories/issues) section of this repository.

Questions about add-in development in general should be posted to [Stack Overflow](http://stackoverflow.com/questions/tagged/Office365+API). Make sure that your questions or comments are tagged with [office-js], [word], and [API].

## Learn more

Here are more resources to help you create Word Javascript API based add-ins:

* [Office Add-ins platform overview](https://msdn.microsoft.com/EN-US/library/office/jj220082.aspx)
* [Word add-ins](https://github.com/OfficeDev/office-js-docs/blob/master/word/word-add-ins.md)
* [Word add-ins programming overview](https://github.com/OfficeDev/office-js-docs/blob/master/word/word-add-ins-programming-guide.md)
* [Snippet Explorer for Word](http://officesnippetexplorer.azurewebsites.net/#/snippets/word)
* [Word add-ins JavaScript API Reference](https://github.com/OfficeDev/office-js-docs/tree/master/word/word-add-ins-javascript-reference)

## Copyright
Copyright (c) 2015 Microsoft. All rights reserved.