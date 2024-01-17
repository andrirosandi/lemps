# GITHUB andrirosandi/lemps
LEMP + SSL Docker setup

## how to use
1. change working directory to ```lemps``` folder
2. change ```[domain-name]``` into your domain name in ```./nginx/conf.d/default.conf```
3. update ```docker-compose.yaml``` with your preferences
4. run: ```docker compose create```
5. run: ```docker compose start```
6. run: ```docker-compose run --rm certbot certonly --webroot --webroot-path /var/www/certbot/ --dry-run -d [domain-name]```
7. if point 6 is success then try again without the option ```--dry-run```
8. open ```./nginx/conf.d/default.conf``` then remove the comment tag on the second section-SSL
9. smile :)

## note
1. run this command to renew ssl cert, run: ```docker-compose run --rm certbot renew```

## directory
- your php file is in ```./html```
- nginx configuration file is in ```./nginx/conf.d```
