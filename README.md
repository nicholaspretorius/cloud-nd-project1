### Udacity Cloud Developer Nanodegree: Project 1

The code for this project was provided by Udacity, with minor alterations made by myself. 

The static website files are hosted in AWS S3 and distributed by AWS CloudFront. Since I did not want to manually upload files any time something changed, I setup a CodePipeline connected to a GitHub repository. 

This means that any time any code is committed into the master branch, CodePipeline will deploy the files into the S3 bucket - thus eliminating any need for manually copying files over. 

According to the rubric, I changed some items such as the title, the background image and some of the content. 

AWS Services Used:

* S3 (Simple Storage Service)
* CloudFront (Content Delivery Network)
* CodePipeline (Continuous Delivery)
* GitHub (Code Repository)
