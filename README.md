# Azure Deployment Demo
### This project is forked from https://github.com/krishnaik06/AzureDeployment.
#### I have added more comments and have updated the below Readme to make the files more readable & the overall process more understandable.

In this demonstration, we show how we can deploy a ML model using Azure using a Flask WebAPI.

We have already built an AQI predictor for the city of Jaipur and in this demo, we simply demonstrate the steps to deploy the same on Azure.

To start with, we already have our pre-built model, which we have saved as randomForestRegressor.pkl, and is uploaded to our respective GitHub profile from where Azure will pull the same for web app build and deployment. Along with this, we also need to provide the Flask app.py file, for invoking a html based web-page for user interaction-fetch model .pkl file-and use the .pkl file for prediction using the inputs provided on the web-page by the user.

In Azure Portal:
	1. we choose 'Create a Resource'
	2. Choose 'Web App'
	3. Choose the subscription & resource group-either existing/new
	4. Provide the resource name-runtime stack (we chose Python 3.7, as our model was built using Python 3.7)-SKU and size (we chose Free F1, as it is free)
	5. Click 'Review & Create'
	6. Click 'Create'
	7. Once the deployment is completed-choose 'Go to resource' to view the deployment details
	8. Then under Deployment options, click on 'Deployment Center'-choose GitHub for deployment as we have already saved all our code there
	9. For 1st time users, we need to provide authorization to Azure for connecting to GitHub, and then once authorized, we need to fill in the details. Choose the relevant repository that we want to use & choose 'Finish'
	10. Inside the GitHub repository, we have provided the html files for building the webpage while the webapp link is available under the Overview section-URL
	
The web-app is hosted at:
https://aqiazuredemo.azurewebsites.net	