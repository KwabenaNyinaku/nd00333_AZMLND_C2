## SCRIPT FOR SCREENCAST
To begin with this project, I uploaded the bank marketing dataset from my local files and configured a new cluster called kwabs233. 
After which, I created an automl experiment and run using classification and selected the label column "y".
The best model was then deployed using the azure container instance. I then activated application insights,
by specifying the deployed model name and running the script logs.py. THe swagger.json was then retrieved using
the "wget" and the swagger URL in the terminal for the swagger folder. The deployed model was then consumed using swagger, by running
the bash swagger.sh command and running the serve.py script in the swagger folder containing swagger.json. 
I then interacted with the swagger instance, running with the documentation for the HTTP API of the model.
The contents were also on display after which the endpoints.py script was run, showing that it runs against the 
API producing JSON output from the model. Benchmark.sh was then run to display the benchmark report. 
In the Azure SDK, the computer cluster and dataset are created, and the dataset was described and displayed.
I then run the notebook given, filling in the required variables to create, publish and consume the pipeline.
Some errors were encountered along the way which has been resolved. The notebook shows that an environment and 
pipeline was created and a run showing the metrics and run details in the notebook. After completion, it 
is then published and run from the REST endpoint using the pipeline_run.publish_pipeline() code. We authenticate
again to retrieve the auth_header so the endpoint can be used. The REST URL from the endpoint is attained and 
an HTTP POST request to the endpoint is built. The RunDetails then shows the status and other information 
regarding the pipeline. The pipeline section shows the created pipeline, and after the bank marketing
dataset with the AutoML module. The pipeline endpoint Bankmarketing Train is displayed and a published pipeline 
overview shows a REST endpoint and status of ACTIVE.

