
# FakestoreAPI Automation

The FakestoreAPI Automation project is an efficient solution built to automate the testing of the FakestoreAPI, a popular online e-commerce API. Leveraging a powerful combination of Postman, JavaScript, Newman Reporting and Jenkins this project brings automation, scalability, and reliability to the API testing process.

## Run Locally in Postman
- Clone the Project
```bash
git clone https://github.com/MubeenAhmadShaikh/FakestoreAPI-Automation-Postman.git
```
- Import the global workspace json file 'workspace.postman_global.json'
- Import the collection in Postman you want to run [Products | User | Cart]
 - Download the csv data files [products_data.csv | user_data.csv | cart_data.csv]
 - Select the products collection and click on Run select the products_data.csv file and preview it once
 - Run the collection
 - Results will displayed with all the tests

## Run Locally using Newman
Dependencies

`Newman` `Nodejs` `newman-reporter-htmlextra`

- Clone the Project
```bash
git clone https://github.com/MubeenAhmadShaikh/FakestoreAPI-Automation-Postman.git
```
- Go to the project directory

```bash
cd FakestoreAPIAutomation
```
- Go to specific collection directory
```bash
cd products_collection
```
- Run the collection using following command
```bash
newman run Products.postman_collection.json -d products_data.csv -g workspace.postman_globals.json
```
- For reports add the following 
```bash
newman run Products.postman_collection.json -d products_data.csv -g workspace.postman_globals.json -r htmlxtra
```

## Run Locally in Jenkins
Dependencies

`Java` `Jenkins.war` 

- Clone the project

```bash
git clone https://github.com/MubeenAhmadShaikh/FakestoreAPI-Automation-Postman.git
```

- Go to the project directory

```bash
cd FakestoreAPIAutomation
```

- Start the Jenkins server
```bash
java -jar jenkins.war
```
- Access the jenkins server on localhost using your port_number
```bash
http://localhost:port_number/
```
- Create a new job and give the project name FakestoreAPI
- Configure the job scroll to Build step and click on add build step
- Select `Execute shell` for MacOS and `Execute windows bash command` for windows
- Add following commands
```bash
cd C:\working_directory\FakeStoreAPIAutomation\cart_collection
newman run Cart.postman_collection.json -d cart_data.csv -g workspace.postman_globals.json -r htmlextra
```
- Click on Build now to run the collection 

#

Arguments of commands

| Parameter | Option     | Description                |
| :-------- |:-----------| :------------------------- |
| `newman run` | `required` | Newman command to run the tests from CLI |
| `-d` | `optional` | For providing the data files |
| `-g` | `optional` | For providing the global env json file|
| `-r` | `optional` | For providing the reports |
| `htmlextra` | `optional` | To generate the reports|

## Features

- GET, POST, PUT, PATCH, DELETE APIs Tested 
- API Test Automation
- RestAPIs Testing
- HTML Reporting
- Schema Validation
- Response data Validation
- Data driven tests 
- End-to-end tests 


## Developed using

- Postman
- JavaScript
- Newman
- Jenkins

## 🛠 Skills

`JavaScript` `Automation Testing` `API Testing` `Postman API Testing` `RESTapi` `Jenkins` `Newman` `Newman Html reports` 

