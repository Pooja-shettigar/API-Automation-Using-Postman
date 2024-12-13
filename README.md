**Project Description:**

Aimed to automate REST and SOAP api calls using Postman applications and report generation using Newman tool


**Project Setups:**

Postman download -> https://www.postman.com/downloads/ 

Newman Installation -> https://learning.postman.com/docs/collections/using-newman-cli/installing-running-newman/ 


**Project Details:**

Project 1 -> Automation of REST api using Postman, https://gorest.co.in/

Project2 -> Automation of SOAP api using Postman, http://dneonline.com/calculator.asmx

**Postman functionalities used:**
1. Global, Environment and Collection level variables
2. Inbuilt postman randonly generated data
3. Assertions
4. Test scripts 

**Type of testing used:**
1. Positive testing od APIs
2. Negative testing of APIs
3. API Chaining
4. Data driven testing
5. Interoperability testing
6. Fuzz testing

**Project Structures:**

API Collections -> https://github.com/Pooja-shettigar/API-Automation-using-Postman/tree/master/API%20Collections

Testdata -> https://github.com/Pooja-shettigar/API-Automation-using-Postman/tree/master/Testdata

Testreports -> https://github.com/Pooja-shettigar/API-Automation-using-Postman/tree/master/Testreports


**Commands too run the collections and generate test reports:**
1. Execute entire collection
newman run "{Filepath}/API Collections/API Automation Using POSTMAN - SOAP.json"  -r htmlextra

2. Execute specific folder in the collection
newman run "{Filepath}/API Collections/API Automation Using POSTMAN - SOAP.json" --folder "{{Filepath}/API Collections/POSITIVE TESTING}" -r htmlextra

3. Execute collection with test data file
newman run "{Filepath}/API Collections/API Automation Using POSTMAN - REST - Data Driven.json" -d "{Filepath}/Testdata/Create User Testdata.csv" -r htmlextra

4. Execute collection with environment variables
newman run -e "{Filepath}/API Collections/Dev-Env.postman_environment.json" "{Filepath}/API Collections/API Automation Using POSTMAN - REST - Data Driven.json" -r htmlextra

5. To generate customised title in the report
newman run "{Filepath}/API Collections/API Automation Using POSTMAN - SOAP.json"  -r htmlextra --reporter-htmlextra-title "{Write Project Tilte}"




