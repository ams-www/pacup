# pacup aptリポジトリ

このリポジトリは `pacup` コマンドのAPTパッケージを配布する。

## 使い方

1. 公開鍵を追加する。次にリポジトリを登録する。

```sh
wget -O- https://ams-www.github.io/pacup/mykey.gpg | sudo gpg --dearmor -o /usr/share/keyrings/pacup-archive-keyring.gpg
```

```sh
echo "deb [signed-by=/usr/share/keyrings/pacup-archive-keyring.gpg] https://ams-www.github.io/pacup stable main" | sudo tee /etc/apt/sources.list.d/pacup.list
```

2. パッケージリストを更新する。次にpacupをインストールする。

```sh
sudo apt update
sudo apt install pacup
```

---

## サポート環境

Ubuntu 20.04以降に対応する。次にDebian 11以降にも対応する。

---

## 公開鍵

公開鍵`mykey.gpg`をこのリポジトリで配布する。次にAPTのセットアップ時に使う。

---

## よくある質問

Q. aptで署名エラーが出る。  
A. 公開鍵の追加コマンドをもう一度実行する。

Q. どのディストリで動く？  
A. Ubuntu 20.04以降とDebian 11以降で動作確認済み。

---

## ライセンス

GPL-3.0で公開する。

---

## 問い合わせ

Issueから連絡する。次に質問や要望があれば気軽にどうぞ。
