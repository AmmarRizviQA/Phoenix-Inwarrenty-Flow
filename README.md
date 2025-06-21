# Postman API Automation Integration with Github Actions #

This repository is a demostration for POC for integrating postman tests with github actions. The Tests are written in postman and they are executed on
the Virtual Machine with the help of newman and newman-reporter-htmlextra.Github Actions will triger the project execution on every push to the main branch. You can also execute the project manually using workflow_dispatch. The projects runs on a scheduled time with the help of the cron job.

The HTML report is archieved and kept in the artifact section for the teamto download it. Along with that they can view the report directly from the github page :https://github.com/AmmarRizviQA/Phoenix-Inwarrenty-Flow/ . 
The latest report is mailed to the team member using GMAIL SMIP.

## TEch Stack ##
1. Postman
2. Nodejs 22v
3. Newman
4. Newman-reporter-Htmlextra
5. GIthub Actions
6. Gmail SMIP
7. Github pages
8. CSV for Data Driven Testing
9. AWS-EC2 instance for self hosted github runner.


## Github Pages ##
You can directly view the latest test report of the Postman test at the GIthub page Link: https://github.com/AmmarRizviQA/Phoenix-Inwarrenty-Flow

## How to run the Project ##
You can run the project on your local system for that:
1. Clone the Project on Local System: https://github.com/AmmarRizviQA/Phoenix-Inwarrenty-Flow.git
2. Install nodejs and NPM from: https://nodejs.org/en/download
3. Install newman using npm: npm install -g newman
4. Install Newman-reporter-htmlextra: install -g newman-reporter-htmlextra
5. Run the newman command:
           newman run 'Inwarranty-flow Collection.postman_collection.json' \
          -e QA.postman_environment.json \
          -d testdata.csv \
          -r cli,htmlextra

## HTML Report ##
The Report will be created in the newman folder

## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing and Edge Case Testing
3. Token Testing
4. Data Driven Testing with csv
5. Schema Validation
6. Secrets Management with Github Secrets.



