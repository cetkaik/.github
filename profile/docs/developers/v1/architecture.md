# 【V1】アプリ構成図

## 全体構成

### online cetkaik アプリ
  - onlineでcetkaikを遊ぶためのアプリ
  - 以下の２アプリからなる
    - frontend
    - backend 
  - DBなどは採用しておらず、必要な履歴はアプリが保持している程度。

### 周辺アプリ

- [cetkaik_platform](https://sozysozbot.github.io/cetkaik_platform/show_history.html?history=%7B%E4%B8%80%E4%BD%8D%E8%89%B2%3A%E9%BB%92%7D%0A%7B%E5%A7%8B%E6%99%82%3A2022-09-08T07%3A19%3A07.162Z%7D%0A%7B%E7%B5%82%E6%99%82%3A2022-09-08T07%3A20%3A13.412Z%7D%0AMAU%E5%BC%93MAIMY%E6%A9%8B%E4%B8%80%09ME%E5%BC%93MIMU%E6%A9%8B%E4%BA%94%0AZO%E7%9A%87%5BZY%5DZAIZAU%09MU%E5%BC%93MYZY%E6%A9%8B%E4%B8%80%E6%AD%A4%E7%84%A1%0AZAI%E8%88%B9ZIZA%E6%A9%8B%E4%B8%89%E6%89%8B%E8%B5%A4%E7%8E%8B%0A%0A%E6%88%96%E7%82%BA%E7%8E%8B%0A%E5%86%8D%E8%A1%8C%0A%0ATE%E8%99%8EZA%E7%84%A1%E6%92%83%E8%A3%81%E6%89%8B%E9%BB%92%E8%88%B9%09MY%E5%BC%93MU%E7%84%A1%E6%92%83%E8%A3%81%E6%89%8B%E9%BB%92%E5%BC%93%0AZAU%E7%9A%87XAU%5BZAI%5DTY%09MU%E5%BC%93MI%E7%84%A1%E6%92%83%E8%A3%81%E6%89%8B%E8%B5%A4%E5%85%B5%0A%0A%E6%88%96%E7%82%BA%E9%A6%AC%E5%BC%93%E5%85%B5%E5%8A%A0%E7%8E%8B%0A%E5%86%8D%E8%A1%8C%0A%0AZI%E8%88%B9ZIA%E7%84%A1%E6%92%83%E8%A3%81%E6%89%8B%E9%BB%92%E7%8E%8B%0A%0A%E6%88%96%E7%82%BA%E7%8E%8B%E8%80%8C%E6%89%8B%E4%BA%8C%E5%8D%81%0A%E7%B5%82%E5%AD%A3%09%E6%98%A5%E7%B5%82%0A%0A%0A%E6%98%9F%E4%B8%80%E5%91%A8)
  - 棋譜を表示するためのアプリ

## Frontend

### 概要

Production / Staging の２環境があり、環境識別情報を付加した上で同一のbackendと通信する。
GitHub Pagesでホストされる。


### デプロイ方法

master push を triggerに [deploy workflow](https://github.com/jurliyuuri/cerke_online_alpha/blob/master/.github/workflows/deploy.yml)が走り、github_pagesブランチが更新される。、 GitHub Pages機能でにデプロイされる。

TODO: 当該repositoryのdocsに書く

###　環境

| 環境 | リポジトリ | URL |
| --- | ---       | --- |
| production  | https://github.com/jurliyuuri/cerke_online_alpha | http://jurliyuuri.com/cerke_online_alpha/entrance.html　|
| staging | https://github.com/sozysozbot/cerke_online_alpha_staging | https://sozysozbot.github.io/cerke_online_alpha_staging/entrance.html　|

## BackEnd

### 概要

cerkeのbackend をさばくサーバー。

fly.io でホストされる。

### デプロイ方法

TODO. 記述

TODO. 当該リポジトリの docs に書く

### 環境

fly.io 上に　マスターコードがあり、適宜以下のリモートリポジトリにも同期されている（！）

- API endpoint:
    - https://little-water-8645.fly.dev
    - GET すると github の方のrepositoryにredirectされるようになっている。
- repository
    - fly.io 上
    - https://gitlab.com/jekto.vatimeliju/cerke_online_backend
    - https://github.com/cetkaik/cerke_online_backend 

## cetkaik_platform

### デプロイ方法

当該リポジトリのdocsに記載。


### 環境

| リポジトリ | URL |
| --- | --- |
| https://github.com/sozysozbot/cetkaik_platform | https://sozysozbot.github.io/cetkaik_platform/ |
