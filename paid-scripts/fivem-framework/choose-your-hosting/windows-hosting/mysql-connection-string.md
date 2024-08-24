---
description: >-
  Creating your database is 1 thing, but connecting your database to your server
  is another, below are a few steps on how to connect your fivem server to your
  mysql database.
---

# 🛢️MySQL Connection String

***

Creating your connection string:

1. **Visit the MySQL String Generator Website:** [Here](https://brouznouf.github.io/fivem-mysql-async/)
2. Click `Next` twice until you are on `3: Configure the FXServer`.

<figure><img src="../../../../.gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>

3. **After you are on the 3rd page, scroll down until you see this:**

<figure><img src="../../../../.gitbook/assets/image (6) (1).png" alt=""><figcaption></figcaption></figure>

4. **The following information will be required for your connection string to work:** (Some other things you can add will be: **acquireTimeout** and **connectTimeout** - These will make the string take longer before connecting / pushing an error.)

* User
* database
* host
* password

<figure><img src="https://i.imgur.com/I2hE9QE.png" alt=""><figcaption><p>Password only required if you created with a password</p></figcaption></figure>

5. **After filling out the info regarding your database and you should see a section called `FXServer Configuration`**
6. **Copy the line shown below from the website and paste it into your server.cfg and restart your server**

<figure><img src="../../../../.gitbook/assets/image (8) (1).png" alt=""><figcaption></figcaption></figure>



## Ensuring oxmysql or mysql-async

Whether you use [oxmysql ](https://github.com/overextended/oxmysql)or [mysql-async](https://github.com/brouznouf/fivem-mysql-async) the way you ensure the it matters.

1. Put the following lines of code into your server.cfg below all the default resources required by FiveM.

```lua
set mysql_connection_string "host=localhost;user=root;database=fivem"
ensure mysql-async -- Only if using mysql-async
ensure oxmysql -- Only if using oxmysql
```





Congratulations, you connected your database to your FiveM Server!
