FROM mediawiki:1.38.5

RUN git clone --depth 1 https://github.com/wikimedia/mediawiki-extensions-LDAPProvider.git /var/www/html/extensions/LDAPProvider

RUN git clone --depth 1 --branch REL1_37 https://github.com/wikimedia/mediawiki-extensions-PluggableAuth.git /var/www/html/extensions/PluggableAuth

RUN git clone --depth 1 https://github.com/wikimedia/mediawiki-extensions-LDAPAuthentication2.git /var/www/html/extensions/LDAPAuthentication2

RUN git clone --depth 1 https://github.com/wikimedia/mediawiki-extensions-LDAPAuthorization.git /var/www/html/extensions/LDAPAuthorization

RUN git clone --depth 1 https://github.com/wikimedia/mediawiki-extensions-LDAPUserInfo.git /var/www/html/extensions/LDAPUserInfo

RUN git clone --depth 1 https://github.com/wikimedia/mediawiki-extensions-LDAPGroups.git /var/www/html/extensions/LDAPGroups

RUN \ 
apt-get update && \
apt-get install libldap2-dev -y && \
rm -rf /var/lib/apt/lists/* && \
docker-php-ext-configure ldap --with-libdir=lib/x86_64-linux-gnu/ && \
docker-php-ext-install ldap

#RUN touch /var/www/html/debug.log && chown www-data:www-data /var/www/html/debug.log
