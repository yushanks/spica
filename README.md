# docker Nginx Puma
## :memo:使い方

### Step 1: 
docker-composeで複数のコンテナを起動します。

`docker-compose up -d`


docker-composeでどのコンテナが起動しているかを確認します。

`docker-compose ps `

`docker-compose exec app rake db:migrate:status`

`docker-compose exec db  mysql -u user_name -p -D mysql`




