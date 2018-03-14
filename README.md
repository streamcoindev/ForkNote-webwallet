# ForkNote-webwallet
If using this please provide credits to me
Word before hand this is kind of raw code if you encounter any bugs or whatsoever or security flaws within wallet code (not the login system) feel free to contact me at thecryptowriter@gmail.com.
SO how to get started? You need have a working forknote coin and walletd needs to be running.
For this i used https://github.com/therecluse26/PHP-Login#postinstall this is the login system i used since its maintained and bugs are being fixed everyday. so you can set that up or use any login system whatsoever.
After you setup PHP-Login we are going to edit the database:

Login to your system or phpmyadmin select the database and memebers table.
Next we are going to add a column address for the coins address just execute this query ALTER TABLE members ADD address varchar(97)  
dont forget to change members to prefix_members if you used a prefix during the installation of php login.

Next up is editing the pages to add wallet functionallity.
First is to edit the registration page so it creates an address and adds it to the user database.

Open up yourwebsite/login/ajax/createuser.php with your favourite text editor and add the registration page code you can find on this github right below line 38 

so right below this :
echo '<div class="alert alert-success"><button type="button" class="close" data-dismiss="alert" aria-hidden="true">&times;</button>'. $conf['signup_thanks'] .'</div><div id="returnVal" style="di.....

Dont forget to fill in the database credentials.

Next up is the index page: The index page will contain a balance checker and will show the address of the user.
So go ahead and open up yourwebsite/index.php with a text editor and add the code from index page code on this repository right underneath 
if (isset($_SESSION['username'])){

Once again dont forget to edit the database credentials.
So now lets move on to the last page this page will need to be made so create the following file yourwebsite/withdraw.php 
I created 2 pages for this in this repository 1 with only the wallet code and 1 that you only have to copy and paste into the withdraw.php 




