Databases -> select your database -> actions -> create read replica (you can even make a standby for your read replica database) -> you can choose the AZ (availability zone) -> you need to give it an identifier (naming the database, for example testdatabase-ro) -> create read replica

The read only database will have a different end point that you will connect to your application.