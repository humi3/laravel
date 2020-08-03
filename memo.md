# laravel メモ

## ルーティングに関して
デフォルトだと以下のフォルダー内のソース  
`routes`  

webの場合 `routes/web.php`  
変えられるかは不明

3年前の記事だが以下参照  
[Laravelのルーティング書き方まとめ](https://qiita.com/michiomochi@github/items/de19c560bc1dc19d698c)

ルーティンの確認については以下  
`php artisan route:list`

memo
```
php artisan route:cache
コマンドを実行するとルーティングのキャッシュが作成され
php artisan route:clear
でもキャッシュをクリアすることができます。
```

## アクション作成時コマンド
`php artisan make:controller action-name`  
actionを作成する場合は、上記のコマンド  
ルーティングに関しては以下のような記述になる。

```php
Route::get('/sample', 'SampleController@index');
```

## DB migration
コマンド  
`php artisan migrate`

ディレクトリー  
`database/migrations`

マイグレーションファイルの作成
`php artisan make:migration create_posts_table --create=table-name`

## DB
### モックデータ作成

`php artisan make:seeder table-name-Seeder`

`/database/seeds`フォルダー直下に上記のソースが作成される。

以下のコマンドで適応  
`php artisan db:seed --class=table-name-Seeder`