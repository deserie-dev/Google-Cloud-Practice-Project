# LAB: Google Cloud Fundamentals: Getting Started With App Engine

## Objectives:

In this lab you will learn how to perform the following tasks: 

- Initialize App Engine.

- Preview an App Engine application running locally in Cloud Shell.

- Deploy an App Engine application, so that others can reach it.

## Steps:

1. Initialize your App Engine app with your project and choose its region.
```
gcloud app create --project=$DEVSHELL_PROJECT_ID
```

2. Clone the source code repository for a sample application in the hello_world directory.
```
git clone [YOUR_APP]
```

3. Navigate to the source directory.
```
cd [YOUR_APPs_SOUURCE_DIRECTORY]
```

4. Download and update the packages list.
```
sudo apt-get update
```

5. Set up a virtual environment in which you will run your application.
```
sudo apt-get install virtualenv
```

6. Activate the virtual environment.
```
source venv/bin/activate
```

7. Navigate to your project directory and install dependencies.
```
pip install  -r requirements.txt
```

8. Run the application.
```
python main.py
```

9. To deploy your application to the App Engine Standard environment navigate to the source directory.
```
cd ~/python-docs-samples/appengine/standard_python3/hello_world
```

10. Deploy your app.
```
gcloud app deploy
```

11. Launch your browser to view the app at http://YOUR_PROJECT_ID.appspot.com
```
gcloud app browse
```