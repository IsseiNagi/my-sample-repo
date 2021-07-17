# my-sample-repo
test message for Git
another chages for merge test
another changes for merge in remote 2021-06-18 10:23:33

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
適用されるブラウザと適用されないブラウザがある。

マークアップに空行は１行しか反映されない。  

改行するには文末に （半角空白スペース）を２つ。  
もしくは

１行空白行をつける。  

水平線は↓
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

>誰々はこう言っていた。  
>改行するには、通常通り改行指定を入れる。  
>引用を  
>>ネストにすることもできる
***


## 画像を貼り付けたい場合はこれ

Format: ![Alt Text](url)  
![サンプル画像](https://qiita-image-store.s3.amazonaws.com/0/126861/90386757-fd96-8ba6-3477-485669713c55.png)  
htmlのimgタグでも指定できる。  
<img width="200" alt="qiita-square" src="https://qiita-image-store.s3.amazonaws.com/0/126861/90386757-fd96-8ba6-3477-485669713c55.png">  
適用されるブラウザと適用されないブラウザがある。
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

適用されるブラウザと適用されないブラウザがある。

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

```mermaid
erDiagram

user ||--o{ post : owns
post ||--o{ updoot : has
user }|--o{ updoot : does

user {
  number id
  string username
  string email
  string password
}

post {
  number id
  string title
  string text
  number points
  number voteStatus
}

updoot {
  number userId
  number postId
  number value
}
```

```mermaid
journey
    title My working day
    section Go to work
      Make tea: 5: Me
      Go upstairs: 3: Me
      Do work: 1: Me, Cat
    section Go home
      Go downstairs: 5: Me
      Sit down: 5: Me
```


```mermaid
classDiagram
Class01 <|-- AveryLongClass : Cool
Class03 *-- Class04
Class05 o-- Class06
Class07 .. Class08
Class09 --> C2 : Where am i?
Class09 --* C3
Class09 --|> Class07
Class07 : equals()
Class07 : Object[] elementData
Class01 : size()
Class01 : int chimp
Class01 : int gorilla
Class08 <--> C2: Cool label
```

```mermaid
erDiagram

Trouble_records ||--|{ Logs : belongs_to_trouble_records
Cases ||--o{ Trouble_records : has_many_cases
Categories ||--o{ Trouble_records : has_many_categories
Statuses ||--o{ Trouble_records : has_many_statuses

Trouble_records {
  AutoField record_id
  ForeignKey case_id
  ForeignKey category_id
  ForeignKey status_id
  CharField title
  TextField contents
  IntegerField priority
  DateTimeField created_at
  CharField editor
  CharField assignees
  CharField reporter
  IntegerField reporter_phone
  EmailField reporter_mail
}

Logs {
  AutoField log_id
  ForeignKey record_id
  DateTimeField changed_at
  TextField chages
}

Cases {
  AutoField case_id
  TextField case_name
}

Categories {
  AutoField category_id
  TextField category_name
}

Statuses {
  AutoField status_id
  TextField status_name
}
```
