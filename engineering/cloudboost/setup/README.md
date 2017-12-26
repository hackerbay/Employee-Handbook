# Setting up CloudBoost

- Install latest versions of NodeJS, NPM, MongoDB, Redis, Docker before starting and make sure all these services are running.
- Fork and then clone the following repos.
   - https://github.com/CloudBoost/cloudboost
   - https://bitbucket.org/cloudboost/accounts-ui
   - https://bitbucket.org/cloudboost/dashboard-ui
   - https://bitbucket.org/cloudboost/user-service
   - https://bitbucket.org/cloudboost/tables-ui
   - https://github.com/CloudBoost/JavaScriptSDK
- Install dependencies for each repo by `npm install`
- Add these env vars in your terminal (Linux) or use Environment Variables dialog (Windows). To see the env vars. Please click [here](https://hackerbaycompany.slack.com/files/U2JE4HBUK/F3LACUE4T/Environment_Variables)
- Run all repo servers `node server`
- Once the servers are running. Check the console of cloudboost & user-service repo. It should display Secure Key and Cluster Key on the console. Please make sure these keys match. If these keys don't match then delete `_GLOBAL` database on your MongoDB server and restart all the servers again.
- Run and pass all the test cases provided within the JavaScriptSDK repo.
  - To run tests, open config.js inside JavaScriptSDK/test folder, replace the SecureKey with the secure key that was displayed on the console in the last step. Run tests by running npm test in JavaScriptSDK repo.
  - Make sure all the tests pass. If they don't. Contact the CTO.
- Make sure you do this every single time you want to push changes to GitHub / Bitbucket. 
