# 神奈川大学宇宙エレベータープロジェクトHP共同管理用リポジトリ
====

このリポジトリは宇宙エレベータープロジェクトのホームページを部員が共同で管理・編集・更新するために使用するもの。

## Description


## Demo
↓以下で確認出来る。  
<http://space-ev.kanagawa-u.ac.jp/project/KUSEP/index.html>



## Requirement
このHP作成において使用したライブラリとプラグインとしては、
* jquery-3.4.1.min.js
* prmenu-master
* slick-1.8.1  
がある。
prmenu-masterはヘッダー部分のメニューに使用している。header.html内で使用している。
slick-1.8.1はindex.html内のスライドショーに使用。ここは弄りやすいと思われる。

## Usage
#### 記事を追加したい時
activities/YYYY/  
に移動(YYYYは投稿したい記事の西暦)  
YYYY_MM_DD  
の名前の'フォルダ'を作成(YYYY_MM_DDは投稿したい記事の日付, 2024年6月9日の場合 例: 2024_06_09)  
YYYY_MM_DD内に  
YYYY_MM_DD.html  
のフォルダと同じ名前のhtml'ファイル'を作成  
同じディレクトリ(YYYY_MM_DD 内)にその記事に必要な画像ファイルを全て入れる(なるべく圧縮して)
YYYY_MM_DD.html に/KUSEP-HP/にある common-article.htmlのコードを完全に全てコピペする  
そのコード内にコメントアウトしてある通りに内容を変更、追加する  
具体的な記事のhtmlファイルが完成したら次はその上のディレクトリにある年度活動報告一覧に記事サムネイルを追加する 
   
activities/YYYY/YYYY.html  
を編集する(YYYYは上に同じ年度, 例だと: activities/2024/2024.html)  
編集するのは< article >の入ってる< li >  
まず既存の< li >をコピーして上の  
< ul style="list-style: none;">  
    < li>  
この二つの間にペーストする  
ペーストした中の< a href=".html">の".html"の部分を"YYYY_MM_DD/YYYY_MM_DD.html"  
に置き換える  
< figure>< img src=""> ~~ < !--記事のサムネイル画像 正方形が望ましい--> のsrc=""の""の中にYYYY_MM_DD/の中に最初に入れた画像の中でサムネイルにしたい画像の相対パスを記述する。 src="YYYY_MM_DD/画像の名前.jpg"とかになってるはず。  
次の次の行の datetime="YYYY-MM-DD">YYYY年MM月DD日 の部分のYMDも同じように記事の日時を入力する。  
< h3>< /h3> の間に記事タイトルを入力(置き換え)する。  
< p class="text_excerpt">記事の簡単な説明< /p>  '記事の簡単な説明'の部分に必要に応じて記事の簡単な説明文を入力する。
下に残っていると思われる不要な< li>をコメントアウトする。  
index.htmlを最後に編集する。お知らせor新着情報の中の< li>に記事を更新した旨を他と書式を合わせてリンク付きで記載する。
以上、お疲れ様でした。  

#### 機体を追加したい時
上に同じ


## Install


## Contribution

## Licence

## Document
部室のルーター鯖のどこかに入ってる機体情報や記録画像を元に更新して下さい。

## Deploy

## Test
内部でjavascript中から同じディレクトリのhtmlファイルを呼び出しているが、Chromeなどでのデバッグの際はセキュリティの点で勝手にローカルファイルの参照を禁止されてしまう。そのためローカルのディレクトリに関してのウェブサーバーをデバッグ用に立ち上げてそれを見に行く用にしないと上手くデバッグ出来ない。Visual Studio Codeの拡張機能に"Live Server"と言うのがあり、これで手軽に出来るので各自活用して欲しい。(2022/2/9)




## Author

[youyeh-gaoqiao](https://github.com/youyeh-gaoqiao)