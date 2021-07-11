# h1としてのタイトル

## h2としてのタイトル

### h3としてのタイトル

#### h4の大きさ

何も指定なしに書いた地の文

##### h5の大きさ

###### h6の大きさ

囲った箇所を**強調する**ことができる  
囲った箇所を~~打ち消す~~ことができる  
囲った箇所を*斜体に*できる

html使えば文字色を指定できる  
<font color="Red">テキスト</font>  
Lintはとても怒ってくるが。

マークアップに空行は反映されない。  
唐突に水平線を入れてみる。↓
***

## 箇条書きは-でも*でもいいらしい

* 箇条書き１
* 箇条書き２
  * 箇条書き2-1
  * 箇条書き2-2

1. 数字つき箇条書き１
2. 数字つき箇条書き２
    * 2-1
    * 2-2

***

## 引用のような書き方

>誰々は
>こう言っていた。ここまでは改行はされていない。  
>これで改行される。改行するには文末に （半角空白スペース）を２つ。もしくは

１行空白行をつける。
>引用を  
>>ネストにすることもできる
***


## 画像を貼り付けたい場合はこれ

Format: ![Alt Text](url)  
![サンプル画像](https://qiita-image-store.s3.amazonaws.com/0/126861/90386757-fd96-8ba6-3477-485669713c55.png)  
htmlのimgタグでも指定できる。  
<img width="200" alt="qiita-square" src="https://qiita-image-store.s3.amazonaws.com/0/126861/90386757-fd96-8ba6-3477-485669713c55.png">  
でも、めちゃLintは怒ってくる。
***


## リンクを貼りたい場合はこれ

[GitHub](http://github.com)

***

## バックスラッシュエスケープは通常通り有効

\*literal asterisks\*

## インライン表示

例えば`print('sample')`のように書くのかな？

***

## コード挿入

```python
def sample_func(sample):
    for item in sample:
        print(item)
```

***

## 表はこれで作るらしい。ガチ編集しづらい

First Header | Second Header
------------ | -------------
Content cell 1 | Content cell 2
Content column 1 | Content column 2


***

## タスク的な書き方ができる

* [x] 完了したこと
* [ ] 完了してないやつ

***

## マーメイドの機能

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```

```mermaid
graph TD;
    %% から始まる箇所はコメント
    Start-->Pull(Git Repo から Pull)
    Pull-->Build{ビルド実施}
    Build-->Noerror(エラーなし)
    Build-->Error(エラー)
    Noerror-->Deploy(デプロイ実施)
    Error--失敗したので修正-->Pull
    Deploy-->End;
```

```mermaid
graph LR
    Left-->Right-->other
    Right-->another
```

```mermaid
sequenceDiagram
   participant Alice
   participant Bob
   Alice->>John: Hello John, how are you?
   loop Healthcheck
       John->>John: Fight against hypochondria
   end
   Note right of John: Rational thoughts <br/>prevail!
   John-->>Alice: Great!
   John->>Bob: How about you?
   Bob-->>John: Jolly good!
```

```mermaid
sequenceDiagram
    A->B:AとBを実線
    A-->B:AとBを点線 
    A->>B:AからBへ実線矢印
    B-->>A:BからAへ点線矢印
    A -x B:AからBへ×付きの実線矢印
    B --x A:BからAへ×付きの点線矢印
    B->>B:ループ
```

```mermaid
graph LR;
   A-.->B;
   A-->C;
   B-.->D;
   C-->D;
```

```mermaid
gantt
title Adding GANTT diagram to mermaid
dateFormat  YYYY-MM-DD
section A section
Completed task            :done,    des1, 2019-12-10,2019-12-11
Active task               :active,  des2, 2019-12-11, 14d
Future task               :         des3, after des2, 1d
```
