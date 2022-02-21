Services -> Databases -> RDS -> Create Database -> MySQL -> Choose the free tier option under Templates -> Create database.

Multi AZ is not available using free tier.

To enable multi AZ:

In the database overview select modify -> select multi az -> scheduling of modifications, select apply immediately -> click modify DB instance

If you check your database it will have a status of "modifying"

Go to your database -> replication -> it will show you where the "standby" database will be created. 