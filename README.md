# flask-webapp-demo
WebApp using Python Flask

## Database  
Create db-name file `db-name` in root directory with db connection name retrived from aws rds

```bash
# Check db connection
mysql -u root -h <db-host> pythonlogin -p
show tables;

# Create db table
CREATE DATABASE IF NOT EXISTS `pythonlogin` DEFAULT CHARACTER SET utf8 COLLATE utf8_general_ci;
USE `pythonlogin`;

CREATE TABLE IF NOT EXISTS `accounts` (
	`id` int(11) NOT NULL AUTO_INCREMENT,
  	`username` varchar(50) NOT NULL,
  	`password` varchar(255) NOT NULL,
  	`email` varchar(100) NOT NULL,
    PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=2 DEFAULT CHARSET=utf8;

# Insert table data
INSERT INTO `accounts` (`id`, `username`, `password`, `email`) VALUES (1, 'test', 'test', 'test@test.com');
```

## ENV Setup  
```bash
sudo apt install -y python python3-pip python3-venv
sudo pip3 install -y flask
sudo pip3 install -y flask-mysqldb
```

# Credit  
Complete credit goes to David Adams at [codeshack.io](https://codeshack.io/login-system-python-flask-mysql/)   
This project is copied here with due permission and used for demo purpose only.
