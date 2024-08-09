### `DOCKERFILE`

Consists of two stages following optimize docker image with multistage build:
1. Build the React App (using Node LTS, app runs on port 3000 by default)
2. Create the production image (to serve with nginx as reverse proxy exposed to port 80)


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

 1. Checkout Source (Checking the changes in the Master Branch)
 2. Configure AWS Credentials (Checking AWS credentials and Login to the AWS)
 3. Login to Amazon ECR 
 4. Fetch Previous Task Definition ARN (fetching the previous successful build ARN for the rollback functionality)
 5. Build, tag and Push image to Amazon ECR (Build the application and push it to the ECR with the Latest tag)
 6. Fill in the new image ID in the Amazon ECS task definition
 7. Deploy Amazon ECS task definition (Deploying to the ECS)
 8. Run Integration Tests
 9. Rollback if Test fails
 10. Post Login to Amazon ECR and Completion of the pipeline
