# OPERATIONALIZING ML FOR BANKING DATASET

Azure was used to configure a cloud-based machine learning model using the bank marketing dataset. The main goal is to predict if a client will accept to subscribe to the bank's term deposit. The best model is attained using automl, deployed and the model endpoints consumed. Also the python sdk is used to create, publish and consume a pipeline.

## Architectural Diagram

![Screenshot (61)](https://user-images.githubusercontent.com/48255327/159686354-4f97b3a4-928b-4715-9ce0-947a367ed4cd.png)
Authentication is enabled which is very important as it improves security and allows for continuos flow. After an automl is run to derive the best model for the classification problem and later deployed using azure container instance(AcI). During the logging process, both logs are retrieved and application insights are enabled. With its unique scoring uri and key, the model endpoints are consumed using the interaction with the trained model occurs. Lastly a pipeline is created with the same dataset in the Azure SDk to be published and consumed.

## STRUCTURE
1.Authentication
2.Automated ML Experiment
3.Deploy the best model
4.Enable logging
5.Swagger Documentation
6.Consume model endpoints
7.Create and publish a pipeline
8.Documentation (Screencast)
9.Standout Suggestions
