# ready2use-2.3-3.4.1
conn1.okondratov.pl.

mkdir -p /opt/cmdbuild/cmdbuild-db

mkdir -p /opt/cmdbuild/cmdbuild-tomcat

mkdir -p /opt/cmdbuild/nginx_conf

mkdir -p /opt/cmdbuild/letsencrypt_certs

mkdir -p /opt/cmdbuild/certbot_acme_challenge

docker volume rm cmdbuild-db

docker volume rm cmdbuild-tomcat

docker volume rm nginx_conf

docker volume rm letsencrypt_certs

docker volume rm certbot_acme_challenge

docker volume create --opt type=none --opt o=bind --opt device=/opt/cmdbuild/cmdbuild-db cmdbuild-db

docker volume create --opt type=none --opt o=bind --opt device=/opt/cmdbuild/cmdbuild-tomcat cmdbuild-tomcat

docker volume create --opt type=none --opt o=bind --opt device=/opt/cmdbuild/nginx_conf nginx_conf

docker volume create --opt type=none --opt o=bind --opt device=/opt/cmdbuild/letsencrypt_certs letsencrypt_certs

docker volume create --opt type=none --opt o=bind --opt device=/opt/cmdbuild/certbot_acme_challenge certbot_acme_challenge