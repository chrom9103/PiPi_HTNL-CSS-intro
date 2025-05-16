# PiPi_HTML/CSS-intro

HTML/CSS講習会では、実際にWebページを作成することを通してWeb開発の基礎となるHTMLとCSSについて学びます。さらに、JavaScriptを使用して動的なWebページの作成方法や基本的なプログラミングの概念についても触れます。  

## 0.はじめに

### 0.1. 事前設定

### 0.2. 環境整備

### 0.3. Webサイトの仕組み

#### HTMLとは？

#### CSSとは？


## 1. 雛形の作成
HTMLの基本的な使い方を確認しながら、Todoリストを表示するアプリのひな形を作成します。
<details><summary>本日終了時のイメージ</summary>

本日の目標は次のような基本的な文字、画像の表示を行うことです。
<!-- 写真を添付 -->
</details>

### 1.1. Hello World!
最初に「Hello, World!」という文字を表示する簡単なWebページを作成します。以下のコードをエディタに入力し、ブラウザで表示してみましょう！

```html
<!DOCTYPE html>
<html>

<head>
</head>

<body>
    <h1>Hello, World!</h1>
</body>

</html>
```

1. `<!DOCTYPE html>`: HTML5であることを宣言します。
2. `<html>`: HTML文書のルート要素です。
3. `<head>`: メタ情報（文字コードやタイトルなど）を記述します。
4. `<body>`: 実際にブラウザに表示される内容を記述します。

このコードをVS Codeの右下部にある`Go Live`をクリックするとWebページが作成され「Hello, World!」という文字が表示されます。

### 1.2. 見出しと段落（`<h>,<p>`）
画面に「Todo List - Demo」という見出しと「HTML/CSSの基礎用法の演習用」というサブタイトルを書きましょう！
次のような表示を書いていきます。
<!-- ここにイメージを追加 -->

#### 1.2.1. 見出し（`<h1>~<h6>`）
見出しは`<h1>`から`<h6>`までの6段階のレベルがあり、`<h1>`が最も重要で大きな見出し、`<h6>`が最も小さな見出しです。

```html
<h1>これは見出し1です</h1>
<h2>これは見出し2です</h2>
<h3>これは見出し3です</h3>
```
> [!NOTE]
> これ以降、扱うHTMLタグは`<body>`タグ内に記述してください。  
> `<body>`タグはHTML文書の中で実際にブラウザに表示される内容を記述するための領域です。見出しや段落、その後に紹介する画像やリンクなどのブラウザに表示する要素はすべて`<body>`タグ内に配置してください。
> `見出し`のサンプルコードを配置すると次のようになります。
> ```html
> <!DOCTYPE html>
> <html>
> 
> <head>
> </head>
> 
> <body>
>    <h1>これは見出し1です</h1>
>    <h2>これは見出し2です</h2>
>    <h3>これは見出し3です</h3>
> </body>
> 
> </html>
> ```

#### 1.2.2. 段落（`<p>`）
段落は`<p>`タグを使用してテキストをグループ化します。段落は通常、1つのまとまった文章を表します。

```html
<p>これは段落1です。</p>
<p>これは段落2です。</p>
```

#### 実装例
現在、ブラウザ上に次の写真のような画面が表示されていますか？
<!-- 画像を追加 -->

### 1.3. リンク（`<a>`）
画面にHTML/CSS講習会の資料(`https://github.com/chrom9103/PiPi_HTNL-CSS-intro`)へ遷移するリンクを貼りましょう！
リンクは`<a>`タグを使用して作成します。リンク先のURLを`href`属性に指定します。

```html
<a href="https://www.example.com">こちらをクリック</a>
```

上記のコードをブラウザで表示すると、「こちらをクリック」というテキストがリンクとして表示され、クリックすると指定したURL（ https://www.example.com ）に移動します。

#### 実際の例
以下はリンクを使用した例です：

```html
<p>詳細は<a href="https://x.com/piedpiper_agu">X(旧Twitter)</a>をご確認ください。</p>
```

このコードをブラウザで表示すると、「X(旧Twitter)」というリンクが表示され、クリックすると指定したURLに移動します。

> [!TIP]
> リンク先を新しいタブで開きたい場合は、`target="_blank"`属性を追加します：
> ```html
> <a href="https://www.example.com" target="_blank">新しいタブで開く</a>
> ```

### 


### 1.4. 画像（`<img>`）

画像をWebページに表示するには、`<img>`タグを使用します。画像のソース（ファイルパスまたはURL）を`src`属性に指定し、代替テキストを`alt`属性に記述します。

```html
<img src="https://www.example.com/image.jpg" alt="サンプル画像">
```

上記のコードをブラウザで表示すると、指定した画像が表示されます。`alt`属性は画像が表示されない場合に代わりに表示されるテキストで、アクセシビリティの向上にも役立ちます。

#### 実際の例
実際にwebページに画像を表示していきましょう！！  
このリポジトリ内に画像ファイルがおいてあります。(`assets\TodoImg.png`)  
この画像を以下のように表示されるようにしてください。
<!-- 画像を挿入 -->

> [!TIP]
> 画像のサイズを調整したい場合は、`width`や`height`属性を使用します：
> ```html
> <img src="assets\TodoImg.png" alt="サンプル画像" width="200" height="100">
> ```
> または、CSSを使用してスタイルを指定することもできます：
> ```html
> <img src="assets\TodoImg.png" alt="サンプル画像" style="width: 200px; height: 100px;">
> ```

#### 画像のリンク化
<details><summary>詳細を表示</summary>

画像をクリックすると別のページに移動するようにするには、`<a>`タグで画像を囲みます：

```html
<a href="https://www.example.com/">
    <img src="assets\TodoImg.png" alt="サンプル画像">
</a>
```

このコードをブラウザで表示すると、画像がリンクとして機能します。
</details>

#### 実装例
現在、ブラウザ上に次の写真のような画面が表示されていますか？
<!-- 画像を追加 -->

### 1.5. フォーム（`<input>`）

フォームの入力要素を使用して、ユーザーからデータを取得する方法を学びます。以下の例では、テキスト入力フィールドを作成します。

```html
<input id="username" type="text" placeholder="ユーザー名を入力してください">
```

- `<input>`: ユーザーがデータを入力するためのフィールドです。
  - `id`: 入力フィールドを識別するための属性です。
  - `type`: 入力フィールドにどのような型を受け付けるのか指定します。
  - `placeholder`: 入力フィールド内に表示される初期テキストを指定します。

> [!TIP]
> 他の入力タイプも試してみましょう：
> ```html
> <input type="date" placeholder="日付を選択">
> <input type="file" placeholder="ファイルを選択">
> <input type="radio" placeholder="ラジオボタン">
> ```

### 1.6. ボタン（`<button>`）

ボタンは、ユーザーがクリックして特定のアクションを実行するための要素です。

```html
<button>クリックしてください</button>
```

このコードをブラウザで表示すると、「クリックしてください」というボタンが表示されます。

#### ボタンの属性
ボタンにはさまざまな属性を設定できます。HTML/CSS講習会では以下の属性を使用します。

- `onclick`: ボタンがクリックされたときに実行されるJavaScriptコードを指定します。

```html
<button onclick="alert('ボタンがクリックされました！')">アラートを表示</button>
```

このコードをブラウザで表示すると、名前を入力するフィールドと「送信」ボタンが表示されます。

#### 実装例
現在、ブラウザ上に次の写真のような画面が表示されていますか？
<!-- 画像を追加 -->

## 2. 表の作成

### 2.1. 表（`<table>`）
HTMLの`<table>`要素は、データを行と列で構成された表形式で表示するために使用されます。表は、以下のような構造で記述されます：

- `<table>`: 表全体を囲む要素。
- `<tr>`: 表の行を定義する要素。
- `<th>`: 表のヘッダーセルを定義する要素（通常は太字で中央揃え）。
- `<td>`: 表のデータセルを定義する要素。

#### 例
以下は、簡単な表の例です：

```html
<table>
    <tr>
        <th>名前</th>
        <th>年齢</th>
        <th>職業</th>
    </tr>
    <tr>
        <td>山田太郎</td>
        <td>30</td>
        <td>エンジニア</td>
    </tr>
    <tr>
        <td>鈴木花子</td>
        <td>25</td>
        <td>デザイナー</td>
    </tr>
</table>
```

### 2.2. ボタンと関数
`<button>`タブの`onclick`属性を使用することにより、ボタンがクリックされたら表が表示されるようにしましょう！

### 2.2.1. イベントハンドリング
イベントハンドリングとは、ユーザーが行う操作（クリック、キー入力、マウス移動など）やシステムからの通知（タイマーの終了、データの読み込み完了など）に応じて、特定の処理を実行する仕組みを指します。この章ではボタンがクリックされたときに表を表示します。  
ボタンがクリックされたときに`AddPressed()`という関数を呼び出しましょう！

```html
<button id="addButton" onclick="AddPressed()">Add Task</button>
```

これで関数が呼び出されるはずですが、その処理を定義していないので書いていきましょう。  
関数(function)のような`Javascript`のコードは`<script>`タグに記述していきます。

```html
<script>
    function AddPressed(){
        text = `<tr>\n` + 
               `<td class="taskElement">タスク0</td>\n` + 
               `<td><button onclick="deleteTask()">Delete</button></td>\n` + 
               `</tr>\n`　+ 
               `<tr>\n` + 
               `<td class="taskElement">タスク1</td>\n` + 
               `<td><button onclick="deleteTask()">Delete</button></td>\n` + 
               `</tr>\n`
               `<tr>\n` + 
               `<td class="taskElement">タスク2</td>\n` + 
               `<td><button onclick="deleteTask()">Delete</button></td>\n` + 
               `</tr>`;
        document.getElementById('result').innerHTML = text;
    }
</script>
```
関数の動作
1. `text`変数の生成
    - テーブルの行(`<tr>`)を複数生成するHTML文字列を作成しています。
    - 各行には以下の要素が含まれます
        - `<td class="taskElement">`: タスク名を表示するセル。例: "タスク0", "タスク1", "タスク2"。
        - `<button onclick="deleteTask()">Delete</button>`: 各タスクを削除するためのボタン。クリックするとdeleteTask()関数が呼び出されるようになっています（ただし、この関数はまだ定義されていません）。
2. `document.getElementById('result').innerHTML = text;`
    - HTML内の`class="result"`を持つ要素を取得し、その中身を変数`text`で上書きします。

`document.getElementById('result')`を使用していますが、HTML内に`class="result"`を持つ要素が存在しないので表が画面に表示されません。以下の要素をHTMLに追加しましょう。

```html
<table class="result">
    <!-- Tasks will be added here -->
</table>
```


### 2.2.2. DOM操作

### 2.3. 色と背景

### 2.4. ボックスモデル

### 2.5. レイアウト

### 2.6. フレックスボックス

### 2.7. グリッドレイアウト

### 2.8. メディアクエリ


## 3. JavaScript

### 3.1. イベントハンドリング

### 3.2. DOM操作

### 3.3. フォーム


## 4. 演習問題