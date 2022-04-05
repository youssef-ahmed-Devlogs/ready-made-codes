<h2>** To Install Nodejs Any Version **</h2>
<ol>
    <li>
        <h4>curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -</h4>
    </li>
    <li>
        <h4>sudo apt-get install -y nodejs</h4>
    </li>
</ol>
<a href="https://github.com/nodesource/distributions/blob/master/README.md">Read More...</a>

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
    <div>
        The stream or file "/opt/lampp/htdocs/eCommerce/storage/logs/laravel.log" could not be opened in append mode: Failed to open stream: Permission       </div>
    <div>denied The exception occurred while attempting to log: The stream or file "/opt/lampp/htdocs/e................bla bla bla</div>
    
    [ solve ]
    sudo chmod -R ugo+rw storage/ bootstrap/cache/
    
</h4>

<hr/>
    
    


