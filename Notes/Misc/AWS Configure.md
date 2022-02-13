In order to access your S3 bucket you need to have your aws config set up in the terminal.

Go to IAM -> users -> create access key if you have not already

In the terminal run:

```
aws configure
```

Enter your Access Key ID, Secret access key, default region (us-east-1 for me), output format (I chose json but you can pick table too)