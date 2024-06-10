# docker_traefik_example2

## 概要
* 前回  
  https://github.com/Tobotobo/docker_traefik_example1  
* 今回  
  traefik とリバースプロキシーの対象( nginx )を別の compose ファイルに分ける

## 詳細

### 起動

* my_network を作成
  ```
  ./create_my_network.sh
  ```
* traefik フォルダ内で `docker compose up -d`
* nginx フォルダ内で `docker compose up -d`
* http://web.docker.localhost にアクセス
* nginx の welcome ページが表示されることを確認

### 破棄

* nginx フォルダ内で `docker compose down`
* traefik フォルダ内で `docker compose down`
* my_network を削除
  ```
  ./remove_my_network.sh
  ```