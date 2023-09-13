Followed Steps:

1 - Setup Git repository:

**Fork the Github repository**
1. Logged into my Github account & navigated to the "aws-elastic-beanstalk-express-js-sample" repository.

<p align="center">
  <img src="https://github.com/arorae1/aws-elastic-beanstalk-express-js-sample/assets/119739576/834f1116-048a-4a90-a300-fa0ff0bb122f" width="800">
</p>
2. Locate the white "Fork" button situated in the top right corner of the screen. Click on it. Following this, a small window will appear, prompting you to specify where you'd like to create the fork. Select "Create a fork." After a brief moment, your web browser will show a duplicate of the repository within your account, accessible under the "Repositories" section.

<p align="center">
  <img src="https://github.com/arorae1/aws-elastic-beanstalk-express-js-sample/assets/119739576/0fd9866b-6701-4408-b82d-16dcbda4eee4" width="400">
</p>

**Push a change to your repo**
1. Navigate to the "aws-elastic-beanstalk-express-js-sample" repository & select the green "Code" button positioned near the top of the page.
2. To clone the repository using HTTPS, confirm that the header reads "Clone with HTTPS." If it doesn't, click on the "Use HTTPS" link.

<p align="center">
  <img src="https://github.com/arorae1/aws-elastic-beanstalk-express-js-sample/assets/119739576/8fc4c4b1-64c7-47cb-9678-6587f0b9dc3c" width="200">
</1p>

3.In your terminal or Git Bash, input the following command, ensure to substitute "YOUR-USERNAME" with your GitHub username. Upon executing this command, your terminal will display a message beginning with "Cloning into." This action will create a new directory containing a copy of the files from the GitHub repository.
#git clone https://github.com/YOUR-USERNAME/aws-elastic-beanstalk-express-js-sample

<p align="center">
  <img src="https://github.com/arorae1/aws-elastic-beanstalk-express-js-sample/assets/119739576/60fd6ac5-03f0-42c1-8810-269457d11a39" width="800">
</p>

4. Within the newly created folder, there will be a file named "app.js." Open "app.js" using your preferred code editor. Modify the content on line 5 to something other than "Hello World!" and save the file.

<p align="center">
  <img src="https://github.com/arorae1/aws-elastic-beanstalk-express-js-sample/assets/119739576/bbad7cb1-926c-434c-992b-d21b23721b18" width="200">
</p>

5. Navigate to the folder named "aws-elastic-beanstalk-express-js-sample/" and commit the changes using the following commands:
#git add app.js
#git commit -m "Change message"
<p align="center">
  <img src="https://github.com/arorae1/aws-elastic-beanstalk-express-js-sample/assets/119739576/37b7e4da-9826-431c-94e8-3f3962c107fc" width="200">
</p>

6. Push the local changes to the remote repository hosted on GitHub using this command.
#git push

<p align="center">
  <img src="https://github.com/arorae1/aws-elastic-beanstalk-express-js-sample/assets/119739576/8e74f670-612b-4dce-a399-0ef4c26a7471" width="200">
</p>

#Verify the changes
1. In your browser window, open GitHub.
2. In the left navigation panel, under Repositories, select the one named aws-elastic-beanstalk-express-js-sample.
3. Choose the app.js file. The contents of the file, including our change, should be displayed.
<p align="center">
  <img src="https://github.com/arorae1/aws-elastic-beanstalk-express-js-sample/assets/119739576/91b1a732-1e95-4006-8c01-d5a821f0b4f5" width="200">
</p>

2 -  Deployed Web App on Elastic Beanstalk

1. Open a new browser tab and access the AWS Elastic Beanstalk console. Click on the "Create Application" button.
<p align="center">
  <img src="https://github.com/arorae1/aws-elastic-beanstalk-express-js-sample/assets/119739576/4312f96a-d801-4643-9f4c-dd3bc5d0adba" width="200">
</p>

2. Under the "Configure environment" section, choose "Web server environment."
3. In the text field labeled "Application name," enter "DevOpsGettingStarted"
4. In the "Platform" dropdown menu under the "Platform" section, select "Node.js." The "Platform branch" and "Platform version" fields will automatically populate with default selections.
5. Confirm that the radio button next to "Sample application" under the "Application code" section is selected.
6. Ensure that the radio button next to "Single instance (free tier eligible)" under the "Presets" section is selected.Click "Next" to proceed.

<p align="center">
  <img src="https://d1.awsstatic.com/Getting%20Started/tutorials/ci-cd-tutorial-2.1.58bb539e9311b0db00207baf7c2af566a5974ae8.png" width="500">
</p>

7. On the "Configure service access" screen, select "Use an existing service role for Service Role." if not listed create one aws-elasticbeanstalk-ec2-role.

<p align="center">
  <img src="https://github.com/arorae1/aws-elastic-beanstalk-express-js-sample/assets/119739576/78aab2a8-5f8e-4761-a454-5e034df74882" width="500">
</p>
 
8. In the "EC2 instance profile" dropdown list, the options may vary depending on your previous environment creations:
a. If "aws-elasticbeanstalk-ec2-role" appears in the dropdown list, select it.
b. If another value is displayed, and it's the default EC2 instance profile for your environments, choose it.
c. If the dropdown list is empty, follow the procedure to "Create IAM Role for EC2 instance profile," and once you've created it, return to this step. You should now see the newly created IAM Role in the dropdown list, so select it.

<p align="center">
  <img src="https://github.com/arorae1/aws-elastic-beanstalk-express-js-sample/assets/119739576/ee5503d4-6382-4042-bb2c-3c91719627f3" width="500">
  <img src="https://github.com/arorae1/aws-elastic-beanstalk-express-js-sample/assets/119739576/7a903353-d25a-48ce-aa2f-d21abea4f2aa" width="500">
</p>

8. Click "Skip to Review" on the "Configure service access" page to use the default values and skip optional steps.

The "Review" page will display a summary of your selections.

10. Click "Submit" to initiate the creation of your new environment.

While waiting for the deployment, you will observe:

A screen displaying status messages for your environment.
After a few minutes, a green banner with a checkmark will appear at the top of the environment screen.
Once you see the banner, you have successfully created an AWS Elastic Beanstalk application and deployed it to an environment.

**Test sample web app**
i. Select the link provided under the name of your environment.
ii. After the test is completed, a new browser tab should open, congratulating you on your successful deployment!

3 - Create Build Project

1. Open a new browser tab and access the AWS CodeBuild console. Select "Create project" button.
2. In the "Project name" field, input "Build-DevOpsGettingStarted." From the "Source provider" dropdown menu, select "GitHub."
Ensure that the "Connect using OAuth" radio button is selected.
3. Click the white "Connect to GitHub" button. A new browser tab will open, requesting AWS CodeBuild's access to your GitHub repository.Click the green "Authorize aws-codesuite" button. Enter your GitHub password. Click the orange "Confirm" button.
4. Select the "Repository in my GitHub account" option.
5. In the search field, enter "aws-elastic-beanstalk-express-js-sample."
6. Confirm that "Managed Image" is selected.
7. Choose "Amazon Linux 2" from the "Operating system" dropdown menu.
8. From the "Runtime(s)" dropdown menu, select "Standard."
9. Choose "aws/codebuild/amazonlinux2-x86_64-standard:3.0" from the "Image" dropdown menu.
10. Verify that "Always use the latest image for this runtime version" is selected for "Image version". Confirm that "Linux" is selected for "Environment type."
12. Make sure "New service role" is selected.

Now, create a Buildspec file:

13. Click "Insert build commands."
14. Choose "Switch to editor."
15. Replace the contents of the editor with the following code:

```yaml
version: 0.2
phases:
  build:
    commands:
      - npm i --save
artifacts:
  files:
    - '**/*'
```
16. Click the  "Create build project" button. You should now see a dashboard for your project.

**Testing the CodeBuild project**
1. Click the orange "Start build" button. This will take you to a page to configure the build process.
2. Confirm that the loaded page references the correct GitHub repository.
3. Click the "Start build" button.
4. Wait for the build to complete. While waiting, you'll see a green bar at the top of the page with the message "Build started," the build progress under "Build log," and after a few minutes, a green checkmark with a "Succeeded" message confirming the successful build.

4 - Create Continuous Delivery Pipeline

**Create a New Pipeline:**
1. Open a browser window and access the AWS CodePipeline console. Click the  "Create pipeline" button to start setting up the pipeline.
2. In the "Pipeline name" field, enter "Pipeline-DevOpsGettingStarted."
3. Ensure that "New service role" is selected.
4. Click the "Next" button to proceed.

**Configure Source Stage:**
1. Select "GitHub version 1" from the "Source provider" dropdown menu.
2. Click the white "Connect to GitHub" button. A new browser tab will open, requesting AWS CodePipeline's access to your GitHub repository.
3. Click the "Authorize aws-codesuite" button. You will see a green box with the message "You have successfully configured the action with the provider."
4. From the "Repository" dropdown, choose the repository you created in Module 1.
5. Select "main" from the branch dropdown menu.
6. Confirm that "GitHub webhooks" is selected.
7. Click the orange "Next" button to proceed.

**Configure Build Stage:**
1. From the "Build provider" dropdown menu, select "AWS CodeBuild."
2. Under "Region," verify that the "US West (Oregon) Region" is selected.
3. Select "Build-DevOpsGettingStarted" under "Project name."
4. Click the orange "Next" button.

**Configure Deploy Stage:**
1. Choose "AWS Elastic Beanstalk" from the "Deploy provider" dropdown menu.
2. Under "Region," confirm that the "US West (Oregon) Region" is selected.
3. In the "Application name" field, select the app named "DevOpsGettingStarted" that you created in Module 2.
4. Choose "DevOpsGettingStarted-env" from the "Environment name" textbox.
5. Click the "Next" button. You will now be presented with a page where you can review the pipeline configuration.
6. Click the "Create pipeline" button to finalize the pipeline setup.

**Execute the Pipeline:**
As you watch the pipeline execution, you will see a page with a green bar at the top. This page displays all the steps defined for the pipeline, and after a few minutes, each step will change from blue to green.
Once the "Deploy" stage switches to green and displays "Succeeded," click on "AWS Elastic Beanstalk." This will open a new tab listing your AWS Elastic Beanstalk environments.
Select the URL in the "Devopsgettingstarted-env" row. You should now see a webpage with a white background and the text you included in your GitHub commit from Module 1.

5 - Finalize Pipeline and Test

**Add a Review Stage to the Pipeline:**
1. Open the AWS CodePipeline console.
2. Locate the pipeline you created in Module 4, named "Pipeline-DevOpsGettingStarted," and select it.
3. Click the "Edit" button near the top of the page.
4. Click the "Add stage" button positioned between the "Build" and "Deploy" stages.
5. In the "Stage name" field, enter "Review". Click the  "Add stage" button.
6. Inside the "Review" stage, click the "Add action group" button.
7. Under "Action name," enter "Manual_Review." From the "Action provider" dropdown, select "Manual approval." Confirm that the optional fields are left blank.
8. Click the orange "Done" button.
9. Click the orange "Save" button at the top of the page.
10. Confirm the changes by clicking the orange "Save" button again.

Now, push a new commit to your repository:

11. In your preferred code editor, open the "app.js" file from Module 1. Modify the message in Line 5. Save the file.
12. Open your Git client.  Navigate to the folder created in Module 1. 
13. Commit the change using the following commands:

  #git add app.js
  #git commit -m "Full pipeline test"
  
14. Push the local changes to the remote repository hosted on GitHub:
  #git push
  
**Manually approve the pipeline**

1. Go to the AWS CodePipeline console.
2. Select the pipeline named "Pipeline-DevOpsGettingStarted." You will notice that the "Source" and "Build" stages switch from blue to green.
3. When the "Review" stage switches to blue, click the white "Review" button.
4. Write an approval comment in the "Comments" textbox.
5. Click the orange "Approve" button.
6. Wait for the "Review" and "Deploy" stages to turn green.
7. Select the AWS Elastic Beanstalk link in the "Deploy" stage. This will open a new tab listing your Elastic Beanstalk environments.
8. Click the URL in the "Devopsgettingstarted-env" row. You should now see a webpage with a white background and the updated text from your most recent GitHub commit.

Congratulations! You now have a fully functional continuous delivery pipeline hosted on AWS, including a manual review stage for deployment approval.


NOTE : Detailed steps can be found here: https://aws.amazon.com/getting-started/hands-on/create-continuous-delivery-pipeline/?ref=gsrchandson
