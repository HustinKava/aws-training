Amazon Simple Storage Service

This is an object based storage system
The "objects" are your files

The bucket name must be globally unique

The object must contain the following:

- Key (name of the objects)
- Version ID
- Value (actual data) 
- Metadata
- Access control information

You can also connect your EC2 instances using the internet gateway to the S3 bucket (see "Using roles EC2.md")

![](./Images/S3BucketDiagram.PNG)

Creating an S3 bucket:

Services -> storage -> S3 -> Create bucket (s3-WhateverNameYouWant) -> next -> enable versioning -> next -> create bucket