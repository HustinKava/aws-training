EC2: virtual server on the cloud (Linux or Windows)

Amazon S3: s3 is a storage system

calculator.aws (cost estimate website)

If you do not have IAM set up you have to login with your root user email

IAM: Identity and access manager

Root account has the ultimate power and aws recommends that you do not use it for everyday usage, you should create your own user accounts

IAM user: person or a service (create an account for each user, or you can use it for service meaning the service uses the credentials of the account for access)
You can apply an IAM policy to a user, group or role
This sets up the permissions for them.

Roles are a little more complex but something that can be used for delegations. For example you can have a service that obtains a role with the permissions required to access EC2.

You can create an access key (.env variable) that you can put into your javascript project and make an API call to aws using the .env variable.
Another way is just by using a GUI through aws using a password and then you get access to the management console.
There is another way using a server signing certificate 

Security, Identity, & Compliance -> IAM -> dashboard -> edit account alias (if you want to change the account id to something more dev friendly) 

user groups -> create group -> AdministratorAccess -> create group
The permissions are set up as a json object

{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": "*",
            "Resource": "*" (* basically means any action on any resource is granted)
        }
    ]
}

Creating a user:

users -> add users -> (here is where we can choose to give the access token or give a GUI password)

After you have picked the user type, you set the permissions. It is not advised to directly attach or copy a policy to the user.
Add the user to a group.
You can then add tags associated with the user (email ect)

click on review -> create user

The user can then sign in using this link:

https://hkava.signin.aws.amazon.com/console

One thing you cannot do in any other account aside from the root account is access billing information.

