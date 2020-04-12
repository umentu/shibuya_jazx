# Shibuya JAZZ


## 環境構築

brewは各自で

### anyenv

```
brew install anyenv
echo 'eval "$(anyenv init -)"' >> ~/.bash_profile
exec $SHELL -l
```

### nodenv

```
anyenv install nodenv
exec $SHELL -l
```

### Node.js 12.10.0をインストール

```
nodenv install 12.10.0
```

**nodenv: default-packages file not found** が出た場合

一旦アンインストールして設定してサイドインストール

```
nodenv uninstall 12.10.0
mkdir -p "$(nodenv root)/plugins"
git clone https://github.com/nodenv/nodenv-default-packages.git "$(nodenv root)/plugins/nodenv-default-packages"
echo yarn >> $(nodenv root)/default-packages
nodenv install 12.10.0
```

12.10.0をデフォルトに。一応Pythonをsystem標準に。
```
pyenv global system
nodenv  global 12.10.0
node -v
# 12.10.0が出たら成功
```


```
cd $PROJECT_DIR/lp
# 関連ライブラリINSTALL
yarn
```

## 起動

```
yarn dev
```

localhost:3000にアクセス

## ファイル
とりあえず使うのは

- pages
    - メイン
- compornents
    - メインで使う部品を作る
- assets
    - js/css/imagesを設置
- static
    - js/css/imagesを設置


assetsとstaticの違いはまぁおいおい
