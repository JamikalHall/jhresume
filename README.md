# Jamikal Hall Resume

 This is my rendition of the Cloud Resume Challenge. I wanted to build in AWS despite having the AZ-900 because
 I like AWS, wanted to test myself and AWS has a very generous free tier that I could take advantage of
 for this challege. I am creating more of a personal portfolio rather than a resume, however the idea is still the same.
 These are the general steps I will be taking, with some slight changes.

 Below are the challenges in order.

1. Your resume needs to have the AWS Cloud Practitioner certification on it.

2. Your resume needs to be written in HTML.

3. Your resume needs to be styled with CSS.

4. Your HTML resume should be deployed online as an Amazon S3 static website.

5. The S3 website URL should use HTTPS for security. You will need to use Amazon CloudFront to help with this.

6. Point a custom DNS domain name to the CloudFront distribution, so your resume can be accessed at something like my-c00l-resume-website.com. You can use Amazon Route 53 or any other DNS provider for this.

7. Your resume webpage should include a visitor counter that displays how many people have accessed the site. You will need to write a bit of Javascript to make this happen.

8. The visitor counter will need to retrieve and update its count in a database somewhere. (DynamoDB)

9. Do not communicate directly with DynamoDB from your Javascript code. Instead, you will need to create an API that accepts requests from your web app and communicates with the database. I suggest using AWS’s API Gateway and Lambda services for this.

10. You will need to write a bit of code in the Lambda function; you could use more Javascript, but it would be better for our purposes to explore Python.

11. You should also include some tests for your Python code.

12. You should not be configuring your API resources – the DynamoDB table, the API Gateway, the Lambda function – manually, by clicking around in the AWS console. For this I will be using Terraform.

13. You do not want to be updating either your back-end API or your front-end website by making calls from your laptop, though. You want them to update automatically whenever you make a change to the code.

14. Set up GitHub Actions such that when you push an update to your Terraform template or Python code, your Python tests get run. If the tests pass, the Terraform app should get packaged and deployed to AWS.

15. Create a second GitHub repository for your website code. Create GitHub Actions such that when you push new website code, the S3 bucket automatically gets updated.