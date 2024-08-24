---
description: >-
  Creating a local server environment on your Windows machine with XAMPP and
  setting up a database for FiveM  involves a few steps. This guide will show
  you how to do it in no time!
---

# 🛢️MySQL Installation

***

#### Step 1: Update and Upgrade your linux machine

```bash
sudo update
sudo upgrade -y
```

This will take a little bit so give it sometime keep your SSH connection open while running this process.

#### Step 2: Installing mysql-server

```bash
sudo apt install mysql-server -y
```

#### Step 3: Connecting to mysql

Run the following command to get into the MySQL server in SSH&#x20;

```bash
sudo mysql
```

#### Step 4: Assigning a password to the root account

Change `password` with the password you want the root account for this demo we used: `COOL`You can generate a secure password by visiting this website [CLICK ME](https://www.lastpass.com/features/password-generator#generatorTool)

```sql
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'COOL';
```

```sql
FLUSH PRIVILEGES;
```

```bash
EXIT; 
```

#### Step 5: Logging back into your MySQL server after changing the password

```
sudo mysql -u root -p
```

Now enter your new password in this case it would be `COOL`

#### Step 6: Creating the FiveM database

```sql
CREATE DATABASE fivem;
```

#### Step 7: Exit

```sql
EXIT;
```

😊 Congratulations, you created your first database in a linux server.&#x20;
