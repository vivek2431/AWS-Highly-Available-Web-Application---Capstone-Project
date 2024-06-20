
## AWS RDS and EC2 Integration

This repository contains scripts to set up an AWS RDS instance, connect to it from an EC2 instance, insert dummy data, and fetch it using an Apache server.
## Prerequisites

- AWS EC2 instance
- AWS RDS instance
- MySQL client on EC2
- Apache server on EC2

### Script 1: RDS connection from EC2

```bash
#!/bin/bash
# Update and install MySQL client
sudo apt update
sudo apt-get install mysql-client -y
```

# Verify MySQL client installation
```mysql --version```

# Connect to RDS instance (replace with your actual endpoint, username, and password)
```mysql -h mydatabase.c5wym6zs3no9.us-east-1.rds.amazonaws.com -P 3306 -u admin -p```
# Enter password: admin123

### Script 2: RDS dummy data insertion
```
#!/bin/bash
# MySQL connection details
host="mydatabase.c5wym6zs3no9.us-east-1.rds.amazonaws.com"
username="admin"
password="admin123"
database="mydatabase"
```
# SQL query to create table
`create_table_query="CREATE TABLE IF NOT EXISTS Family (id INT PRIMARY KEY, name VARCHAR(50));"`

# SQL query to insert dummy data
`insert_data_query="INSERT INTO Family (id, name) VALUES (1, 'Saurabh'), (2, 'Nishant'), (3, 'Rohit'), (4, 'Azruddin');"`

# Connect to MySQL and execute queries
```mysql -h $host -u $username -p$password -D $database -e "$create_table_query" && \
mysql -h $host -u $username -p$password -D $database -e "$insert_data_query"

echo "Table created with dummy data."
```
### Apache server fetches data from RDS
```
#!/bin/bash
# Database configuration
host="mydatabase.c5wym6zs3no9.us-east-1.rds.amazonaws.com"
username="admin"
password="admin123"
database="mydatabase"
table="Family"
```
# Install required packages
```
sudo apt update
sudo apt install -y apache2 php libapache2-mod-php php-mysql

# Create a PHP script to fetch data from the database
sudo tee /var/www/html/index.php >/dev/null <<EOF
<?php
\$conn = new mysqli("$host", "$username", "$password", "$database");
if (\$conn->connect_error) {
    die("Connection failed: " . \$conn->connect_error);
}
\$sql = "SELECT * FROM $table";
\$result = \$conn->query(\$sql);
if (\$result->num_rows > 0) {
    echo "<table><tr><th>ID</th><th>Name</th></tr>";
    while(\$row = \$result->fetch_assoc()) {
        echo "<tr><td>" . \$row["id"] . "</td><td>" . \$row["name"] . "</td></tr>";
    }
    echo "</table>";
} else {
    echo "0 results";
}
\$conn->close();
?>
EOF
```
# Configure Apache to serve PHP files
`sudo sed -i "s/index.html/index.php/g" /etc/apache2/mods-enabled/dir.conf`

# Restart Apache
`sudo systemctl restart apache2`

# Display public IP
`echo "Web application is now accessible at: http://$(curl -s ifconfig.me)"`

### Usage
Connect to your EC2 instance.
- Run Script 1 to install the MySQL client and connect to your RDS instance.
- Run Script 2 to create a table and insert dummy data into your RDS instance.
- Run Script 3 to set up an Apache server, create a PHP script to fetch data from your RDS instance, and display the public IP of your 
  EC2 instance.
