#pubkeys
clone
`git clone https://github.com/yasuken1990/pubkeys.git` OR `git clone git@github.com:yasuken1990/pubkeys.git`

addkeys
`cd pubkeys && sh addkey.sh`

example apache
DocumentRoot is public_keys
`
<VirtualHost *:80>
    DocumentRoot /[path]/public_keys
    ServerName pubkeys.yasuken1990.com
    <Directory "/[path]/public_keys">
        Options Indexes FollowSymLinks
        AllowOverride all
        Order allow,deny
        Allow from all
    </Directory>
</VirtualHost>
`
