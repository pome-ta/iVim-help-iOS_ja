[https://github.com/pome-ta/iVimHelpDocsTranslationSandBox](https://github.com/pome-ta/iVimHelpDocsTranslationSandBox)

# 📝 2022/09/24

## `Docs` 抜き出し

`:h ios` など、iVim 用のhelp を抜き出してみる

### 手順

#### 受け取る用のディレクトリを作成

- iVim でterminal を起動
  - `Documents` が多分root になってる
- 適当な名前で作成 `mkdir hoge`

#### help を開いてディレクトリ位置を確認

- `:h ios` とかでiVim 用のhelp を開く
- help のバッファ上で`:echo expand("%:p")` で、格納ディレクトリを確認
  - `echo` をどこかに挿入でもいいけど、気軽にみつけられなかった
  - 今回は、スクショをしてスクショ上からテキストコピー(iOS16)
    - `O` が`0` になっていたり、勝手に改行されたりするから調整
- ディレクトリパスをコピー

#### `:terminal` で該当ディレクトリへ移動

- 一階層上の`doc/` やもう一つ上の`runtime` へ
- `doc/` ディレクトリをコピーして、`Documents` へ貼り付け
  - `cp -r doc/ ~hoge`
  - ちょっと待つ

## キーボードセッティング

``` .txt
Customize ~

If the default buttons or keys on the extended keyboard don't meet your own
needs, you can customize them through command |:isetekbd|.

```

カスタマイズ

拡張キーボードのデフォルトのボタンやキーが自分のニーズに合わない場合は、コマンド｜:isetekbd｜でカスタマイズできます。
コマンド |:isetekbd| でカスタマイズすることができます。
