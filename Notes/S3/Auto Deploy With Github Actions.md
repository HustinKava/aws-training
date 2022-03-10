IAM -> policies -> new -> json

```
{
	"Version": "2012-10-17",
	"Statement": [
    	    {
              "Sid": "AllowS3SyncCommand",
        	  "Effect": "Allow",
        	  "Action": [
                  "s3:GetObject",
                  "s3:Listbucket",
                  "s3:PutObject",
                  "s3:DeleteObject",
              ],
        	  "Resource": [
		      "arn:aws:s3:::{bucket_name}",
                  "arn:aws:s3:::{bucket_name}/*"
              ]
    	    }
	]
}
```

next -> review ->

name: deploy-hustin-portfolio

create policy

usergroups -> create new

name: deploy-hustin-portfolio

scroll down and select the policy we just created -> create group 

users -> add users -> 

user name: hustin-portfolio

select access key - programmatic access

permissions -> select the new user group created 

create user

copy access key and secret access key

Back in github go to your repo settings -> secrets -> actions -> new repo secret

Name: AWS_ACCESS_KEY_ID

Name: AWS_SECRET_ACCESS_KEY

In your react app create this structure on the root:

.github/workflows/workflow.yml

Add your template and push up

In github hit actions and view the deployment