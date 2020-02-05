### Udacity Cloud Developer Nanodegree: Project 1

The code for this project was provided by Udacity, with minor alterations made by myself. 

1. CloudFront URL: [http://d1t8lxwhdmt6wa.cloudfront.net/index.html](http://d1t8lxwhdmt6wa.cloudfront.net/index.html)
2. S3 URL: [https://udacity-cloud-nd-project1.s3.us-east-1.amazonaws.com/index.html](https://udacity-cloud-nd-project1.s3.us-east-1.amazonaws.com/index.html)

#### Caching 

*Please note that CloudFront is caching the `index.html` file. As a result, as of writing, you cannot see the latest version of the `index.html` file on the CloudFront URL. You can see the latest version of `index.html` on the second, S3 URL I provided above. I did run an "Invalidation" on the CloudFront distribution, but since I last checked (10:23 AM, CloudFront was still serving the cached page - likely the invalidation takes some time to flush through the network.)*

#### Description

The static website files are hosted in AWS S3 and distributed by AWS CloudFront as per the project [rubric](https://review.udacity.com/#!/rubrics/2573/view). 

According to the section titled "Suggestions to Make Your Project Stand Out!", I changed some items on the page such as the title, the background image and some of the content.


#### CodePipeline

Additionally, since I did not want to manually upload files any time the code changed, I setup a CodePipeline connected to a GitHub repository. 

This means that any time any code is committed into the master branch, CodePipeline will deploy the files into the S3 bucket - thus eliminating any need for manually copying files over. 

AWS Services Used:

* S3 (Simple Storage Service)
* CloudFront (Content Delivery Network)
* CodePipeline (Continuous Delivery)
* GitHub (Code Repository)

#### AWS Screenshots

##### S3 Bucket

S3 Bucket Files:

![S3 Bucket](/img/project/s3-bucket.png)

S3 Bucket Hosting:

![S3 Bucket](/img/project/s3-bucket-hosting.png)

S3 Bucket Policy

![S3 Bucket](/img/project/s3-bucket-policy.png)

##### CloudFront Distribution

![CloudFront Distribution](/img/project/cloudfront-dist.png)


##### CodePipeline

![CodePipeline](/img/project/codepipeline.png)
![CodePipeline Stages](/img/project/codepipeline-stages.png)