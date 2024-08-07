---
marp: true
# class: invert
---

# Git講習会

### SEKI Hibiki

---
## 座学編

- Gitとは
- Gitの仕組み

## 実習編
未定

---

# Gitとは

---
## バージョン管理
![bg right:50% w:70%](images/version_db.png)

- セーブポイントのようなもの
- 変更の記録を管理 
  - 時間とともに記録
  - 必要な時点に戻れる

- 例)問題が起きた時
  - 問題の発生前まで戻る
  - 変更を見て原因を調査する

---

## Git
![bg right:38% w:80%](images/git.png)


- https://git-scm.com/
- バージョン管理システムの一つ
  - 他にもSubversion, Mercurialなどがある
- ファイル変更の履歴を保存・管理
  - **いつ、誰が、何を変更したか**
- GitHub / GitLab は**履歴共有**のためのサービス

---

## 変更履歴をどう共有するか？
管理方法は大きく以下の三つに分類できる

- ローカル管理
- 集中管理
- 分散管理

---

## ローカルバージョン管理
![bg right:50% w:100%](images/local.png)
**メリット**
- ローカルにバージョン情報を保存する

**デメリット**
- 他人と共有がしにくい

---

## 集中バージョン管理
![bg right:49% w:100%](images/centralized.png)
**メリット**
- 共有サーバーに保存する
- 複数人で共有できる

**デメリット**
- 同時に作業すると巻き戻ることも
- サーバーが落ちたり壊れると被害が大きい

---

## 分散バージョン管理
![bg right:40% w:100%](images/distributed.png)
- ローカルにもバージョン情報を保存
  - 他人を待たずに作業可能
  - サーバーが落ちてもローカルから復元可能


---


# Gitの仕組み


---


## Repository 

**Gitがバージョン管理を行う単位**
- ディレクトリ + Version Database (.git/)で構成
- リポジトリ内のファイルの変更履歴を保存

### Remote Repository
- 共有サーバー上にある Repository

### Local Repository
- 自分の手元にある Repository

---

## 
![bg center w:100%](images/repository.png)


---

## Commit
- 「バージョン」の Git 内での呼び名
  - セーブポイントを作るイメージ
  - 一意なIDを持つ
- Gitは Commit を基準として状態を移動する
  - Commit したときの状態が保存される
  - Commit されていない時点には移れない
    - Commit の間の編集中の状態とか
- HEAD:自分が今いる Commit (基本的には最新コミット)

---

## Push / Pull
- Remote と Local のバージョン履歴を同期する
- **Push** : Local → Remote
    - Push すると Remote も Local と同じ状態になる
    - **他の人からも変更がわかるようになる**
- **Pull** : Remote → Local
    - Remote の変更を Local に持ってくる
    - **他の人の変更が自分の手元に反映される**

---

## Branch
- Commit の繋がり
  - Repository 内に複数作成可能
  - ブランチごとに分けてバージョン管理ができる
    - →複数の機能の開発を分離して保存できる

- **main**(master) Branch：本流

## Merge
- 他の Branch にある変更を取り込む

---

## ![bg center w:100%](images/branch.png)

---
## 他にも
- Rebase: Branch の履歴を整理する
- Stash: 作業中の変更を一時保存する
- Tag: 特定の Commit に名前をつける
- Cherry-pick: 特定の Commit を取り込む
- Checkout: 特定の Commit に移動する
- Submodule: 他のリポジトリを取り込む
- ...

気になる人は調べてみてください

---


この講習会の資料はすべて Git で管理されています
- https://github.com/hijiki51/git-lecture