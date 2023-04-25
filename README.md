<h1 align="center"> API Test Automation Framework Based on Postman and Newman </h1>

<p style="font-size: 1.2rem; font-weight: bold;">
  This framework is made up mostly of the following tools
</p>

```
1. Node.js: A back-end JavaScript runtime environment.
2. Postman-Collection: Software testing tool used for API testing.
2. Newman: A command-line Collection Runner for Postman.
4. newman-reporter-htmlextra: Newman HTML reports generator.
```

<p style="font-size: 1.2rem; font-weight: bold;"> Framework Structure </p>

##
The structure of this framework consists mainly of the following folders/files

1. dataFile.json: Contains the test data scenarios based on which the tests run. Therefore hereinafter we will call it data file.
2. postman_collection.json: Contains the test logic extracted from the postman collection. therefore hereinafter we will call it collection file.
3. package.json: Contains dependencies and instructions about how to run the tests, which can be modified as needed.
4. newman: In this folder will be saved the HTML reports generated after the test run.
##

<p style="font-size: 1.2rem; font-weight: bold;"> How to run the tests from this project </p>

1. As prerequisite, download and install [NodeJS](https://nodejs.org/en/download)
2. Open a terminal console and `make sure you are in the root path of the project`, and run the command below to install dependencies.
   - `npm i`
   - Wait until all dependencies are installed

3. To run the tests without the HTML report, run
   - `npm t`

4. To run the tests along with the HTML report, run
   - `npm run test:report`
>_Notes_:
>* Steps 3 and 4 don't depend on each other. Just select what suits you best.
>* You can change how these commands work by going to the package.json file and update the script section as needed.

5. If your run step 4, you can see the generated report in the newman folder, which you can open with any web browser.

<p style="font-size: 1.2rem; font-weight: bold;"> How to run the tests from postman </p>

1. Take the collection file and import it into postman as a collection.
2. Click on the 3 dots to the right of the collection file, and select 'Run collection'
3. In 'Choose how to run your collection' select 'Run manually'
4. Click on 'Select File' in the Data section and select the data file in this project.
5. Click on "Run_<data file>"
6. Look at the results in the run panel and evaluate according the expected result of your setup.

<p style="font-size: 1.2rem; font-weight: bold;"> How to maintain the tests </p>

1. The data file you can update directly in this project using your IDE.
2. The collection file you should open int from postman by importing it as a collection.
   - Make the required/desired changes in postman and save them.
   - Export the collection and place the updated version within this project replacing the old version.

>Note: Once you are very familiar with the tests in Postman and JSON format handling, you can update the collection file directly in this project using your IDE. Although it is not recommended due to the high risk of possible errors.