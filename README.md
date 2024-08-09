# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

### `AUTOMATION OF THE PROJECT (DEPLOYING APP TO AWS ECS)`

1. Create AWS free tier account.
2. Search for ECS (Elastic Container Service) and ECR (Elastic Container Registry).
3. Go to ECS and Create new cluster (fragate cluster known as serverless).
4. Now create a new task definition for your fragate cluster and define the resources to be used by the cluster.
5. Now create a service under your cluster add your deployment configuration (ECR Name and ECR URL).
6. Now push your code and Dockerfile to the GitHub Repository.
7. Create a AWS workflow in the actions tab.
8. Add necessary secrets for the further use like aws_secret_key, aws_secret_access_key, aws_region, etc.
9. Now update the workflow file with the relevant steps.

 ### `STEPS IN THE CI/CD PIPELINE`
 1.
