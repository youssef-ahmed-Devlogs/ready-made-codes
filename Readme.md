
<h2>Install latest version of git</h2>
<a href="https://askubuntu.com/questions/568591/how-do-i-install-the-latest-version-of-git-with-apt">Read More</a>

<h2>Web Development Setup on Linux Ubuntu</h2>
<a href="https://www.youtube.com/watch?v=nQVvtC_V1ZQ&ab_channel=TheCodeholic">Watch Video</a>


<p>


sudo apt-get install apache2 <br>
sudo apt-get install php libapache2-mod-php <br>

To restart apache2:- <br>

sudo service apache2 restart <br>

Inside [/var/www/html] change user permissions:- <br>

sudo chown {username}:{username} -R ./ <br>

sudo gedit /etc/apache2/envvars <br>

Then change this values to your username:- <br>

export APACHE_RUN_USER={username} <br>
export APACHE_RUN_GROUP={username} <br>


sudo gedit /etc/apache2/mods-available/dir.conf

Then change this order of files:- <br>

<strong>DirectoryIndex index.html index.cgi index.pl index.php index.xhtml index.htm</strong> <br>

<strong>TO</strong> <br>

<strong>DirectoryIndex  index.cgi index.pl index.php index.html index.xhtml index.htm</strong> <br>


Install MySQL:- <br>

sudo apt-get install mysql-server <br>

Check MySQL status:- <br>

sudo service mysql status <br>

Install phpmyadmin:- <br>

sudo apt-get install phpmyadmin <br>

Errors while login to phpmyadmin:- <br>

*Cannot log in to the MySQL server* <br>
*mysqli::real_connect(): (HY000/1698): Access denied for user 'root'@'localhost'*
<br>
The solution:- <br>

sudo mysql<br>
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '123456';




</p>

<a href="https://www.thedataops.org/how-to-upgrade-php-version-from-8-1-to-8-2-in-ubuntu/">Upgrade To PHP 8.2</a>

<hr/>


<h2>** To Install Nodejs Any Version **</h2>

           
        <h4>
        curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash - &&\
        sudo apt-get install -y nodejs
        </h4>
    

<a href="https://github.com/nodesource/distributions/blob/master/README.md#using-ubuntu-3">Read More...</a>


<hr/>

<h2>** To Generate SSH KEY **</h2>
<h4>ssh-keygen -t rsa -b 4096 -C "your_email@example.com"</h4>
<a href="https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent">
Read More...
</a>

<hr/>

<h2>** To Open Xampp **</h2>
<h4>sudo '/opt/lampp/manager-linux-x64.run'</h4>

<hr/>

<h2>** To Give Permission **</h2>

<h4>vscode always ask for permission to save ( sudo chown -R $USER:$USER . )</h4>
<a href="https://stackoverflow.com/questions/51004206/vscode-always-ask-for-permission-to-save">vscode always ask for permission to save</a>
<h4>sudo chmod 777 ./Foldername</h4>
<h4>chmod -R 775 /var/www</h4>
<hr/>

<h2>** Regex Email Validation **</h2>
<a href="https://stackoverflow.com/questions/46155/whats-the-best-way-to-validate-an-email-address-in-javascript">
Read More...
</a>

<h2>** change file permisions to read and write **</h2>
<h4>sudo chmod +x filename</h4>

<hr/>


<h2>** set php path **</h2>
<h4>sudo ln -s /opt/lampp/bin/php-8.0.17 /usr/bin/php</h4>

<hr/>

<h2>** set composer path **</h2>
<h4>sudo mv composer.phar /usr/local/bin/composer</h4>

<hr/>


<h2>** Make a virtual domain **</h2>
<h4>sudo nano /etc/hosts</h4>
<h4>open [ /opt/lampp/etc/httpd.conf ] with text editor, and remove hash[ # ] from [ #Include etc/extra/httpd-vhosts.conf ]</h4>
<h4>open [ /opt/lampp/etc/extra/httpd-vhosts.conf ] with text editor</h4>
<h4>

    <VirtualHost *:80>
        DocumentRoot "/opt/lampp/htdocs"
        ServerName localhost
    </VirtualHost>

    <VirtualHost *:80>
        DocumentRoot "/opt/lampp/htdocs/eCommerce/public"
        ServerName eCommerce.com
    </VirtualHost>

</h4>
<h4>
    sudo /opt/lampp/xampp restart
    
    or
    
    sudo /opt/lampp/xampp stop
    sudo /opt/lampp/xampp start
    
    [ issue ]
    netstat: command not found
    
    [ solve ]
    sudo apt install net-tools
</h4>

<hr/>


<h2>** Laravel issue permition on linux **</h2>
<h4>

    [ issue ]
    The stream or file "/opt/lampp/htdocs/eCommerce/storage/logs/laravel.log" could not be opened in append mode: Failed to open stream: Permission   
    denied The exception occurred while attempting to log: The stream or file "/opt/lampp/htdocs/e................bla bla bla</div>
    
    [ solve ]
    sudo chmod -R ugo+rw storage/ bootstrap/cache/
    
</h4>

<hr/>

