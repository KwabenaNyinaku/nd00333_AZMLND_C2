   # OPERATIONALIZING MACHINE LEARNING FOR BANKING DATASET

Azure was used to configure a cloud-based machine learning model using the bank marketing dataset. The main goal is to predict if a client will accept to subscribe to the bank's term deposit. The best model is attained using automl, deployed and the model endpoints consumed. Also the python sdk is used to create, publish and consume a pipeline.

## Architectural Diagram

![Screenshot (61)](https://user-images.githubusercontent.com/48255327/159686354-4f97b3a4-928b-4715-9ce0-947a367ed4cd.png)
Authentication is enabled which is very important as it improves security and allows for continuos flow. After an automl is run to derive the best model for the classification problem and later deployed using azure container instance(AcI). During the logging process, both logs are retrieved and application insights are enabled. With its unique scoring uri and key, the model endpoints are consumed using the interaction with the trained model occurs. Lastly a pipeline is created with the same dataset in the Azure SDk to be published and consumed.

## STRUCTURE
### 1.Authentication
### 2.Automated ML Experiment
### 3.Deploy the best model
### 4.Enable logging
### 5.Swagger Documentation
### 6.Consume model endpoints
### 7.Create and publish a pipeline
### 8.Documentation (Screencast)
### 9.Standout Suggestions


## Authentication
Security is enabled, and a service principle has been created and allowed access to the workspace.
![Screenshot (30)](https://user-images.githubusercontent.com/48255327/159693112-60360588-c86d-4383-867c-c100f49f27cc.png)
The screenshot shows az ml workspace share command:
![Screenshot (32)](https://user-images.githubusercontent.com/48255327/159693185-514bfac9-007b-4a36-badf-b17eda950879.png)

## Automated ML Experiment
An automl experiment is run using the uploaded Bankmarketing dataset. Explain best model is checked for the classification problem.

Screenshot of Registered Datasets:
![Screenshot (29)](https://user-images.githubusercontent.com/48255327/159694544-34d29fe9-4347-4cea-824f-28b590237fef.png)

Screenshot of Completed Experiment:
![Screenshot (33)](https://user-images.githubusercontent.com/48255327/159694878-d9b8a866-7989-4580-bb66-39f47d10ac86.png)

Screenshots of best model:
![Screenshot (35)](https://user-images.githubusercontent.com/48255327/159695508-65d93ff5-4232-4847-b8c8-535a63928b35.png)
![Screenshot (36)](https://user-images.githubusercontent.com/48255327/159696269-b113ffb4-9233-49b1-bdb2-f9efad1055d9.png)

## Deploy the best model
Completion of the experiment derived the best model which was deployed using the Azure Container instance and enabling authentication. Deploying the Best Model will allow to interact with the HTTP API servie and interact with the model by sending data over POST requests.

## Enable logging
After the best model was deployed, application insights was enabled and the logs were retrieved by running the logs.py python file with the updated model name.
Screenshot of application insights enabled:
![Screenshot (38)](https://user-images.githubusercontent.com/48255327/159697660-cf7b4ce1-4135-4782-a330-8d6afa185679.png)
Screenshot of logs:
![Screenshot (37)](https://user-images.githubusercontent.com/48255327/159698174-0508bb0d-49ad-43bf-aa3d-2b24ee9282ea.png)

## Swagger Documentation
The deployed model was then consumed using swagger. The deployed model's swagger json file is copied and used during to access the documentation.
Screenshots showing that swagger runs on localhost with the HTTP API methods and responses for the model:
![Screenshot (39)](https://user-images.githubusercontent.com/48255327/159699413-cd09df0d-55e7-438c-8da8-fb793f100d88.png)
![Screenshot (40)](https://user-images.githubusercontent.com/48255327/159699443-3608a0d7-7adc-4d58-a55e-e6c8fdeb6adc.png)
![Screenshot (41)](https://user-images.githubusercontent.com/48255327/159699456-011cdba5-edf7-41e6-8397-aefb455d03c2.png)
![Screenshot (42)](https://user-images.githubusercontent.com/48255327/159699483-a20e0ae2-a461-42d3-9ff2-4bf1a41ecb62.png)

## Consume model endpoints
The scoring_uri and the key are updated in the endpoints.py script to match the key for your service and the URI that was generated after deployment. Running the script will allow interaction with deployed model.
Screenshot showing that the endpoint.py script runs against the API producing the JSON output from the model:
![Screenshot (43)](https://user-images.githubusercontent.com/48255327/159700502-19df6742-db9b-40c7-b4df-05e1486bc800.png)
Screenshot showing that Apache Benchmark runs against the HTTP API using authentication keys to retrieve performance results:
![Screenshot (44)](https://user-images.githubusercontent.com/48255327/159700538-221e29d8-aa50-46e9-b784-2e55c235fb83.png)

## Create and publish a pipeline
During this process a pipeline was created, published and consumed with the help of the azure sdk. The bankmarketing dataset was used and after running a pipeline endpoint was created and in the later part of the code, the pipeline was published showing a REST endpoint and a status of active.
Screenshot showing the pipeline was created:
![Screenshot (48)](https://user-images.githubusercontent.com/48255327/159702611-ae70ab84-4e20-4987-b660-d8d222407ab6.png)
Screenshot showing pipeline endpoint:
![Screenshot (60)](https://user-images.githubusercontent.com/48255327/159703038-644ca2c2-e182-429e-a768-6fea4be79a86.png)
Screenshot showing the Bankmarketing dataset with the AutoML module:
![Screenshot (62)](https://user-images.githubusercontent.com/48255327/159704289-063f8a76-047e-4cc9-894e-896412d01176.png)
Screenshot "Published Pipeline overview" showing a REST endpoint and a status of ACTIVE:
![Screenshot (63)](https://user-images.githubusercontent.com/48255327/159704537-fb551a60-612b-4795-83ae-96935971e829.png)
Screenshots showing the "Use RunDetails Widget" step runs:
![Screenshot (59)](https://user-images.githubusercontent.com/48255327/159704875-1a67e11e-724c-4cd5-89a2-49376b682a54.png)
![Screenshot (58)](https://user-images.githubusercontent.com/48255327/159704942-53ee2650-a4cf-46c0-ad61-ddcbcea73598.png)
Screenshot showing run:
![Screenshot (53)](https://user-images.githubusercontent.com/48255327/159705286-8c678ab1-d50e-4363-87fa-f14daec1e906.png)

## Documentation (Screencast)
Screencast can be found ([here](https://youtu.be/m_rG0q5dr90) ). 

## Standout Suggestions
