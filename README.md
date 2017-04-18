# duplicate-WHM-account
Duplicate account in WHM using SSH

**1.** Login to SSH  
**2.** Type: ```/scripts/pkgacct username``` (where username is the username of the account you wish to duplicate)  
**3.** In WHM -> Account Functions -> Modify Account, change the domain name and username of the account to which you need to duplicate. Change these to the NEW duplicate site you want.  
**4.** Restore your original site.  
**5.** Type: ```/scripts/restorepkg username``` (username is the original username of the account)  
  
You will now have two duplicate accounts. Any scripts using databases in the new site will need to have their database connections updated (e.g. if a wordpress site in wp-config.php) to use the new account name prefix for the database and username.
