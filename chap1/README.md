# Chapter1 PythonからRustへ準備体操
## 1. なぜRustが必要なのか


## 2. PythonとRustでは何が違う？


## 3. Rustと開発環境をインストールしよう
> [!NOTE]
> Macで環境構築をする場合の手順をまとめる。

### Rustのインストール
ターミナルでコマンドを実行するだけ
```shell
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
``` 
コマンド実行後にインストールメニューが表示されるので、そこで `1` と `Enter` キーを押すとインストールが実行される。
もしくは、パッケージマネージャーがインストールされている場合は以下のコマンドでもインストールできる。ここでは Homebrew を使った。
```shell
brew install rust
```

インストール済みのRustを最新版にアップデートするには、以下のコマンドを実行するだけでよい。
```shell
rustup update stable
```
> [!TIP]
> Rustをインストールすると `rustup` コマンドが使えると書いてあったが、私の環境では使えなかったので、別途インストールした。[参考](https://qiita.com/notakaos/items/9f3ee8a3f3a0caf39f7b) 
> 
> 実行したコマンド
> ```shell
> brew install rustup-init
> rustup-init
> ```

### VS Codeのインストール
インストールの手順自体は省略する。Rustの拡張機能を入れておく。

### サンプルコードを作ってみる
`hello.rs` を作成して、これを実行してみる。
```shell
# コンパイル
% cd (プログラムを保存したディレクトリのパス)
% rustc hello.rs

# 実行
% ./hello
```


## 4. 初めてのRust


## 5. RustとPythonでFizzBuzz問題を解く


## 6. RustとPythonで九九の表を作る


## 7. 変数定義とフィボナッチ数列


## 8. 変数型とコイン組み合わせの計算


## 9. 関数定義とシーザー暗号


## 10. 配列と100個の素数を計算

