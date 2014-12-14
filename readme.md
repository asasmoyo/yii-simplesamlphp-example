Yii Simplesamlphp Example
-------------------------

This is an example of [Yii Simplesamlphp](https://github.com/asasmoyo/yii-simplesamlphp).

### Installation
	
	You need to follow this steps to install:

	- You need a running Simplesamlphp configured as Identity Provider.

	- Setup apache virtualhost:

		'''bash
		<VirtualHost *:80>
		    ServerName example.com

		    DocumentRoot YOUR_PATH_TO/simplesamlphp-example/app
		    <Directory PATH_TO/simplesamlphp-example/app>
		        Require all granted
		        AllowOverride all
		    </Directory>

		    Alias /simplesaml YOUR_PATH_TO/simplesamlphp-example/simplesamlphp-sp/www
		    <Directory YOUR_PATH_TO/simplesamlphp-example/simplesamlphp-sp/www>
		        Require all granted
		        AllowOverride all
		    </Directory>
		</VirtualHost>
		'''