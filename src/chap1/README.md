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
> [!TIP]
> Rustの拡張機能を入れると、`rust-analyzer` という拡張機能も一緒にインストールされるが、`rust-analyzer failed to discover workspace` というエラーが出てしまう。
> 通常、Rustのプロジェクトには `Cargo.toml` がルートディレクトリに配置されているはずだが、今回はなかった。
> 作成したフォルダをRustのプロジェクトとして扱うために、`Cargo init` を実行した（新規にプロジェクトを作成する場合は `Cargo new <name>` で、既存のディレクトリをRustのプロジェクトとしたい場合は `Cargo init` を実行する）。
[参考](https://zenn.dev/razokulover/scraps/17844b5b5c7147)

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
### 画面に文字を表示する
* PythonとRustの標準出力の違いを比較してみる。
    ```python
    print("Hello, World!")
    ```
    ```rust
    fn main() {
        println!("Hello, World!");
    }
    ```

> [!NOTE]
> [書式] 画面出力
> ```rust
> println!("出力内容");
> ```
> https://doc.rust-lang.org/std/macro.println.html

* Rustは必ず `main` 関数を記述する必要がある。この `main` 関数をエントリーポイントといい、プログラムを実行すると最初にこの関数が実行される。

> [!TIP]
> `println!` の `!` はRustのマクロを使っていることを示している。

### 数値に文字列を埋め込んで表示しよう
> [!NOTE]
> [書式] 値を書式に埋め込んで表示
> ```rust
> println!("...文字列...{}...", 値);
> ```


## 5. RustとPythonでFizzBuzz問題を解く


## 6. RustとPythonで九九の表を作る


## 7. 変数定義とフィボナッチ数列


## 8. 変数型とコイン組み合わせの計算


## 9. 関数定義とシーザー暗号


## 10. 配列と100個の素数を計算

