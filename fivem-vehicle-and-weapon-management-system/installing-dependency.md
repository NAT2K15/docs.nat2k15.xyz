---
description: >-
  The vehicle and weapon system relies on a single dependencies: oxmysql. below
  is our guide on installing oxmysql and setting up a sql server on windows.
---

# Installing Dependency

## Oxmysql (Windows Version)

***

<details>

<summary>Installing SQL server</summary>

## _Installing XAMPP:_

#### Step 1: Download and Install XAMPP

1. **Visit the Official XAMPP Website**: Go to [Apache Friends](https://www.apachefriends.org/download.html) and download the XAMPP installer for Windows.&#x20;
2. **Run the Installer**: Launch the downloaded installer. You might need to approve the UAC prompt and disable any antivirus temporarily if it blocks the installation.
3. **Select Components**: During installation, ensure that **Apache**, **MySQL**, and **PHP** are selected. You can deselect other components unless you know you'll need them.
4. **Choose Installation Directory**: You can install XAMPP in the default directory (`C:\xampp`) or choose another location. Click Next and proceed with the installation.
5. **Complete Installation**: Follow the remaining prompts and finish the installation.

**Step 2: Start Apache and MySQL**

1. **Launch XAMPP Control Panel in Administrator**: After installation, open the XAMPP Control Panel. You can find it in the Start Menu or where you installed XAMPP.
2. **Installing services:** When XAMPP opens up click the ❌ button on the left side of Apache and MySQL and install the services.

<img src="https://i.imgur.com/3WElWOb.png" alt="" data-size="original">

3. **Start Apache and MySQL**: Click the 'Start' buttons next to Apache and MySQL. This will run your local server and database server.

**Step 3: Creating The Database**

1. **Open phpMyAdmin: Open phpMyAdmin using the `Admin` Button on Apache.**

<img src="../.gitbook/assets/image (1) (1).png" alt="" data-size="original">

2. **Creating a database:** Upon opening phpMyAdmin click new on the top left then type for database name `fivem` (all lowercase) then click create.

<img src="../.gitbook/assets/image (2) (1).png" alt="" data-size="original">

Congratulations, you now know how to create a fivem database. Move on to the next page to continue the installation.

</details>

<details>

<summary>Creating an SQL string</summary>

Creating your connection string:

1. **Visit the MySQL String Generator Website:** [Here](https://brouznouf.github.io/fivem-mysql-async/)
2. Click `Next` twice until you are on `3: Configure the FXServer`.

<img src="../.gitbook/assets/image (5) (1).png" alt="" data-size="original">

3. **After you are on the 3rd page, scroll down until you see this:**

<img src="../.gitbook/assets/image (6) (1).png" alt="" data-size="original">

4. **The following information will be required for your connection string to work:** (Some other things you can add will be: **acquireTimeout** and **connectTimeout** - These will make the string take longer before connecting / pushing an error.)

* User
* database
* host
* password

<img src="https://i.imgur.com/I2hE9QE.png" alt="Password only required if you created with a password" data-size="original">

5. **After filling out the info regarding your database and you should see a section called `FXServer Configuration`**
6. **Copy the line shown below from the website and paste it into your server.cfg and restart your server**

<img src="../.gitbook/assets/image (8) (1).png" alt="" data-size="original">



## Ensuring oxmysql or mysql-async

Whether you use [oxmysql ](https://github.com/overextended/oxmysql)or [mysql-async](https://github.com/brouznouf/fivem-mysql-async) the way you ensure the it matters.

1. Put the following lines of code into your server.cfg below all the default resources required by FiveM.
2. **When downloading the files from github always select the releases version on the right side.**

<img src="../.gitbook/assets/image (6).png" alt="" data-size="original">

```lua
set mysql_connection_string "host=localhost;user=root;database=fivem"
ensure oxmysql -- Only if using oxmysql
```





Congratulations, you connected your database to your FiveM Server!

</details>
