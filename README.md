# laravelのセットアップ環境

## 環境
必要なもの  
* dokcer
* docker-compose
* VScode
  * Remote Containers

## 起動方法
* VScode上で`＞＜`をクリック
* クローンしたフォルダを選択

## projectの作成
* 起動した状態で以下のコマンド  
`composer create-project --prefer-dist laravel/laravel <project-name>`

## project作成後
docker-compose.ymlの以下の部分に関して作成したprojectのフォルダ名を加える。  
イメージはリビルドしてください。

変更前
```
../:/var/www
```
変更後
```
../<project-name>:/var/www
```

## 反省点
参考にしたものが古かったためか、PHPのバージョンで引っかかった。  
今回は参考にしたものの7.2のまま作業した。  
phpのDockerfileを変更し、バージョンを上げることでprojectの作成時のコマンドも`laravel new <project-name>`で作成できると思われる。