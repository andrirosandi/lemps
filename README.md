## 
# GITHUB andrirosandi/lemps
# LEMP + SSL Docker setup
##

## how to use

0. change working directory to lemps folder
1. edit ./nginx/conf.d/default.conf
- ubah nama domain sesuai dengan keinginan
2. update docker-compose.yaml sesuai kebutuhan
3. run: docker compose create 
4. run: docker compose start
5. run: docker-compose run --rm certbot certonly --webroot --webroot-path /var/www/certbot/ --dry-run -d [domain-name]
6. jika berhasil maka jalankan kembali poin 5 tanpa option --dry-run
7. edit kembali ./nginx/conf.d/default.conf
- hilangkan komentar pada section yang ke 2 agar ssl dapat berjalan
8. smile :)

# note: 
1. untuk melakukan renew ssl cert, run: docker-compose run --rm certbot renew