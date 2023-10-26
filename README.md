# Steps to Deploy an Meteor.js on Red Hat OpenShift

The [Developer Sandbox for Red Hat OpenShift](https://developers.redhat.com/developer-sandbox) is a free-to-use OpenShift instance for you to experiment with OpenShift for your use cases.The development of dynamic and responsive web applications has evolved into a fundamental requirement. Node.js and Meteor.js stand out as formidable technologies capable of crafting these applications with finesse. Our workflow involves the creation and deployment of applications directly from GitHub onto an OpenShift sandbox environment.

Follow these steps to start your sandbox instance and deploy your Meteor.js app:

1.  Create a Red Hat Sandbox account using [https://developers.redhat.com/developer-sandbox](https://developers.redhat.com/developer-sandbox)
    
2.  Once you have the account and are signed in, On the left side menu, click on **+Add**.
    
3.  Select **Import from Git**.
    
4.  Specify your Git repo URL. For the sake of this tutorial, we use [https://github.com/redhat-developer-demos/meteor.js-openshift-example.git](https://github.com/redhat-developer-demos/meteor.js-openshift-example.git). But, you can choose any Meteor.js repo.
    
5.  Add a **Containerfile** to your repo. The Containerfile helps developers to specify the environment needed for running your applications. In case, you do not have a Containerfile on your project, you can add add one to your repo by referring to [https://github.com/redhat-developer-demos/meteor.js-openshift-example/blob/main/Dockerfile](https://github.com/redhat-developer-demos/meteor.js-openshift-example/blob/main/Dockerfile)
    
6.  OpenShift will detect the Containerfile from the git repository. In case the Containerfile is in a subdirectory, you need to provide the path of Containerfile.
[ NOTE: If the containerfile/Dockerfile is not detected, click Import Edit Strategy. Select as Dockerfile, define the path as Containerfile. ]

7.  Choose a Resource Type field, please choose either Deployment or Serverless Deployment (default option) depending on your preference.
    
8.  Select Target Port under Advanced options to define the port **3000** that will receive the container's traffic.

9.  As this is a resource-consuming container/pod, we should define the resource limit for this. Select the **Build configuration** and then click on **Resource limit** and set the **CPU** to 4 cores and **Memory** to 5Gi.
    
10.  Click on **Create**.
    
11.  You will now be directed to the Topology view, and the application will commence deployment. Please allow some time for the build & deployment process to complete. While it is in progress, you will have the opportunity to monitor the logs.
    
12.  Once it’s done deploying, you can click on the **↗** OpenURL icon to see the webpage of your Meteor.js application running on OpenShift.
    

In this tutorial, you learned how to deploy a Meteor.js application on Red Hat OpenShift. Red Hat OpenShift has powerful features that make it easy to manage and scale your Meteor.js application in production.
