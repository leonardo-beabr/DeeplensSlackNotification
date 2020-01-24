<h2>Deeplens Slack Notifications</h2>

Notify in a slack channel when someone enter in the office


<h2>Setup</h2>
<h3>Slack</h3>
<ul>
    <li>Go to https://api.slack.com/apps to create a new app;</li>
    <li>Click in "Create New App", type the name of the App and select a workspace;</li>
    <li>In "Add features and functionality" turn on the "Enable Events" and add a bot user in Subscribe to bot events. Select "app_mention" and "messages.im";</li>
    <li>Install the App in your workspace, then copy the "Bot User OAuth Token"</li>
</ul>

<h3>Deeplens</h3>
<ul>
    <li>Create a S3 Bucket;</li>
    <li>Create a new project in the Deeplens page using the template "Face dectection";</li>
    <li>Copy and paste the code of the file face-detection.py in the function "deeplens-face-detection;</li>
    <li>Replace add the name of the bucket in the variable "bucket_name"</li>
    <li>Update the function to the latest version. Set the timeout with 600 seconds and click save.</li>
</ul>

<h3>Lambda Function</h3>
<ul>
    <li>Create a new role for AWS Lambda Function with the policies AmazonRekognitionFullAccess, AmazonDynamoDBFullAccess, AmazonS3FullAccess and AWSLambdaExecute in IAM console;</li>
    <li>Download the file recognition.zip;</li>
    <li>Create a new function with Python 3.6;</li>
    <li>Select the option "Upload a .zip file" and chose the file recognition;</li>
    <li>Change the values of the variables bucket, slack_token and slack_channel;</li>
    <li>Save the function.</li>
</ul>
<ul>

</ul>


<h2>Architecture</h2>

[Architecture](https://challengepost-s3-challengepost.netdna-ssl.com/photos/production/software_photos/000/602/534/datas/gallery.jpg)

<h2>Refences</h3>

[Doorman](https://github.com/svdgraaf/doorman)

[Track the number of coffees consumed using AWS DeepLens](https://aws.amazon.com/pt/blogs/machine-learning/track-the-number-of-coffees-consumed-using-aws-deeplens/)


