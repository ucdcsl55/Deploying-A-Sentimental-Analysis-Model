# Deploying-A-Sentimental-Analysis-Model

## Setting up a Notebook Instance

The deployment project is intended to be done using Amazon's SageMaker platform. In particular, it is assumed that we have a working notebook instance in which can clone the deployment repository.

Here are the steps....

### Step 1. Go to AWS SageMaker

First, start by logging in to the AWS console, opening the SageMaker dashboard, and clicking on Create notebook instance.

![AmazonSage](https://github.com/ucdcsl55/Deploying-A-Sentimental-Analysis-Model/blob/main/images/AmazonSageMaker.png?raw=true)

AWS SageMaker → Notebook instances service
Step 2. Create a notebook instance

The Create notebook instance wizard will come up, asking you the following information:

    Notebook instance settings - In this section, you may choose the notebook instance name of your choice. By default, a ml.t2.medium type is available. But, we will use ml.p2.xlarge for training a model and ml.m4.xlarge for deployment. These instances may not be available to all users by default. If you haven't requested ml.p2.xlarge so far, go to the AWS Support Center to raise a Service limit increase request.

        Note that your notebook may have a different name than the one displayed here.

Create notebook instance → Notebook instance settings

    Permissions and encryption - Next, under IAM role field select Create a new role.

Create notebook instance → Permissions and encryption. Create a new IAM role

    Create an IAM role - You should get a pop-up dialog box, where you have to select None radio-button under S3 buckets you specify field, as is shown in the image below.

        Note that the IAM role name that appears may be different than the one displayed here.

Create an IAM role dialog box

Create an IAM role dialog box

Success, creating a new IAM role

    Network - optional - Choose the No VPC option.

Create notebook instance → Network settings. Choose No VPC

    Git repositories - Here you will clone the https://github.com/udacity/sagemaker-deployment.git repository to the current notebook instance only.

Create notebook instance → Git repositories setting

    You're done! Click on Create notebook instance button.

Your notebook instance is now set up and ready to be used! Once the Notebook instance has loaded, you will see a screen similar to the following snapshot.

A successfully created notebook instance (Status: InService). You can access your notebook using the Open Jupyter Action.
