# docker Nginx Puma
## :memo:使い方

### Step 1: 

適当な作業ディレクトリを用意します。

`mkdir spica`
中に入って、git cloneし

`cd spica`
`git clone ***`

docker-composeでビルドして

`docker-compose build`
docker-composeで複数のコンテナを起動します。

`docker-compose up -d`

docker-composeでどのコンテナが起動しているかを確認します。

`docker-compose ps `

`docker-compose exec app rails db:migrate:status`

DBに接続する場合

`docker-compose exec db  mysql -u user_name -p -D mysql`

毎回、docker-composeホニャララと打つのは疲れると思うので、aliasを設定するといいと思います


私の場合、使用シェルがzshなので~/.zshrcに記述、※使用シェルがbashなら~/.bash_profile。

設定方法

`alias dcrails=‘docker-compose exec app rails`

これをすると、ローカルで普通にrails触っている感覚で

`dcrais generate *** `

って打てば、あまり違和感ないかな


