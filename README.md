# docker-laravel
Laravel development environment

# 手順
コンテナ起動（バックグラウンド）  
`docker-compose up -d`

起動を確認  
`docker ps`

http://localhost:8000 にアクセスし画面確認

appコンテナに入る  
`docker-compose exec app bash`

Laravelのプロジェクト作成  
`composer create-project --prefer-dist laravel/laravel <プロジェクト名>`

web/default.confを編集  
```
server {
    listen 80;
    root /var/www/html/<プロジェクト名>/public;
```

コンテナ再起動    
`docker-compose down`  
`docker-compose up -d`

http://localhost:8000 にアクセスし画面確認
