# dockerを用いてのLaravel環境構築を練習

## 起動
```
# GitHubからリポジトリをクローン
git clone <URL>

# コンポーザー起動
cd docker-laravel-handson
docker-compose up -d --build

# Laravelインストール
docker-compose exec app bash
composer install

# .env 環境変数ファイルを作成
cp .env.example .env

# アプリケーションキーを生成
php artisan key:generate

# マイグレーションを実行
php artisan migrate

# アクセス確認
http://127.0.0.1:10080

# アクセス確認後、コンテナを停止して終了
exit
docker-compose down
```

## 参考
- [【超入門】20分でLaravel開発環境を爆速構築するDockerハンズオン](https://qiita.com/ucan-lab/items/56c9dc3cf2e6762672f4)
