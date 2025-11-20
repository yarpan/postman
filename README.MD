Running the Postman collection on GitHub Actions using newman and newman-reporter-htmlextra

# Running Postman Tests in GitHub Actions

This workflow runs a Postman collection using **Newman** and generates an HTML report via **newman-reporter-htmlextra**. It installs dependencies, executes the collection, and uploads the resulting **newman/report.html** as a downloadable artifact for each push or pull request.

## Local Execution
Run the collection locally using:  
  
```
npx newman run collections/NASA-APOD.postman_collection.json -r htmlextra
```
### Or using script in "package.json" file
```
npm run test
```
 
After execution, open **newman/report.html** in your browser to view the full interactive report.

## CI/CD Workflow Summary
GitHub Actions runs the same command and stores the report in the workflow artifacts, providing:
- Detailed request/response logs  
- Test pass/fail status  
- Execution metrics  
- Visual HTML reporting  

