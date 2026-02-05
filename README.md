# Postman API Automation Integration with GitHub Actions #
This repository is a demonstration for POC for integrating Postman tests with GitHub actions. The tests are written in Postman and they are executed on the VM with the help of newman and newman-reporter-htmlextra.
GitHub actions will trigger the project exceution on every push to the main branch. Ypu can also execute the project manually using workflow_dispatch. The project runs on scheduled time with the help of CRON job.

The HTML report is archieved and kept in the artifact section for the team to download. ALong with that they can view the report directly from the GitHub Page: https://shivajibajpai.github.io/Phoenix-InWarranty-Flow/
The latest report is mailed to the team members using the GMAIL SMTP.

## Tech Stack
1. Postman
2. Node.JS
3. Newman
4. newman-reporter-htmlextra
5. GitHub Actions
6. GMail SMTP
7. GitHub Pages
8. AWS EC-2 for self hosted GitHUb runner
9. CSV For Data Driven testing
    
## GitHub Pages ##
You can directly view the latest report of the Postman test at the GitHub page link: https://shivajibajpai.github.io/Phoenix-InWarranty-Flow/

## How to run the project? ##
You can run the project on your local system. For that:
1. Clone the project on local system: https://github.com/ShivajiBajpai/Phoenix-InWarranty-Flow.git
2. Install NodeJS and NPM: https://nodejs.org/en/download
3. Install Newman using: npm install -g newman
4. Install Newman-reporter-htmlextra using: npm install -g newman-reporter-htmlextra
5. Run the newman command:
                           newman run 'In-warranty flow collection Copy 2.postman_collection.json' \
                           -e 'QA.postman_environment.json' \
                           -d 'testdata.csv' \
                           -r cli,htmlextra \
                           --reporter-htmlextra-export ./newman/index.html

## HTML Report ##
The report will be created in the newman folder

