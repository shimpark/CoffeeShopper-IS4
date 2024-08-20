# CoffeeShopper-IS4
A project integrating ASP.NET Identity with IdentityServer 4

NOTE: please check out the different branches based on the 4 stages of this tutorial

https://www.youtube.com/watch?v=SXJ377G5bOg

======================================

References: https://www.youtube.com/watch?v=SXJ377G5bOg&list=PL1EYnCfHLswwOz77bgfFbFqRnY3bXYHp3&index=1

		https://www.youtube.com/watch?v=rNqgxAqGZJ8&list=PL1EYnCfHLswwOz77bgfFbFqRnY3bXYHp3&index=2
  
		https://github.com/iulianoana/CoffeeShopper-IS4/tree/Part4-Secure_the_Client_app
  
		https://codewithjulian.com/


1) To create a new database before first use:
	- Create a database called CoffeeShopperDb
	- Edit API/appsettings.json and set the DB connection string
	- Edit SERVER/appsettings.json and set the DB connection string
	- In Package Manager Console:
		- Set API as startup project
			- Project: DataAccess PM> Update-Database 
		- Set Server as startup project
			- Project: Server PM> Update-Database -Context PersistedGrantDbContext
			- Project: Server PM> Update-Database -Context ConfigurationDbContext
			- Project: Server PM> Update-Database -Context AspNetIdentityDbContext
	- Seed the database with some initial clients and users
		- Project: Server PM> dotnet run Server/bin/Debug/net6.0/Server /seed --project Server
		- Project: Server PM> Click the red stop button

2) After updates to database, set multiple projects to start.
	- API, Server, Client, DataAccess

3) Run the code
