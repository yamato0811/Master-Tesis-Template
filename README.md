# 02MasterThesis
Template for Mater Thesis

## Files

    Font/                  このテンプレートで使用するフォント（再頒布）
    Macro/                 digicon-lab 独自のマクロ
    library.bib            digicon-lab 独自サンプル; BibTeX ファイル
    face.eps               iit 公式サンプル; 画像
    sample.eps             iit 公式サンプル; 画像
    .gitignore             as is; そのまま自分のドキュメント管理にも利用できる。
    README.md              このファイル
    digicon-iit-en.sty     英文用スタイルファイル
    digicon-iit-jp.sty     和文用スタイルファイル
    00_Introduction.tex    digicon-lab 独自サンプル; 分割された TeX ファイル（ MasterThesis.tex にインクルードされる。）
    MasterThesis.tex       digicon-lab 独自サンプル; メインとなる TeX ファイル

## Setup - ローカルで利用する場合

このレポジトリを適当なディレクトリに `clone` する。

```bash
~/repos$ git clone git@github.com:digicon-lab/02MasterThesis.git
```

`Macro` へシンボリックリンクを張る。

Windows, TeX Live の場合:

```cmd
> mklink /D C:\texlive\texmf-local\tex\latex\local\DigiconMacro C:\path\to\repos\02MasterThesis\Macro
```

`Font` にあるフォントをシステムにインストールする。

Windows の場合:

```
すべてのフォントファイルについて、右クリックして「インストール」を実行する。
```

必要と思われるファイルを、自分の作成する文書を保管するディレクトリにコピーする。

例:

* library.bib
* face.eps
* sample.eps
* .gitignore
* README.md
* digicon-iit-en.sty
* digicon-iit-jp.sty
* 00_Introduction.tex
* MasterThesis.tex

`MasterThesis.tex` の7行目にあるコメントを解除し、8行目をコメントアウトする。

```tex
	\usepackage[local, libertine, yuwin, final]{DigiconPreamble}	% Setting for Local
%	\usepackage[sharelatex, final]{Macro/DigiconPreamble}		% Setting for ShareLaTeX
```

次のコマンドを実行して、このサンプルが正常にタイプセットできることを確認する。

```bash
$ xelatex MasterThesis.tex
```

