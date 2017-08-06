# 語意元素

> 聊聊：在沒有語意元素之前

* New tags：新的標籤，像是 `<header>`、`<section>` 等
* Application tags：也是新的標籤，像是 `<meter>`、`<progress>` 等
* Microdata：加入語意的資料讓搜尋引擎等網站可以正確顯示

```html
<section itemscope itemtype="http://example.org/animals#cat">
 <h1 itemprop="name">Hedral</h1>
 <p itemprop="desc">Hedral is a male american domestic
 shorthair, with a fluffy black fur with white paws and belly.</p>
 <img itemprop="img" src="hedral.jpeg" alt="" title="Hedral, age 18 months">
</section>
```

* Form type：`<form>` 可以加入的 type 便多了，包含 email 和 tel 等屬性，瀏覽器會協助進行資料格式的驗證
* 有特殊意義的元素，由名稱可以了解到它與其他內容的差異。
* 語意元素全部都是 block elements


![](./assets/layout.gif)

| 名稱            |        描述     |
| :------------- | :-------------  |
| article        | 通常擁有自己的標題 |
|                | `<article>` 中，還可以在包含 `<article>` |
|                | 表示網頁中一段完整的文件，或可單獨使用的文件 |
| aside          | 適合放置廣告       |
| details        | 定義使用者可顯示或隱藏之額外詳細資料 |
| figcaption     | 描述圖片的標題     |
| figure         | 用來包含影像及其說明，以便將圖及說明一連結在一起。 |
| section        | 內容區塊，有點類似POST的，而此標籤可再包覆header與footer。|
|                | 可以將一段文章，分成好幾個 `<section>` |
| header         | 版頭，可甩來包覆logo。|
|                | 可以加入 table     |
|                | 可以加入搜尋表單    |
|                | 可以加入 `<nav>`   |
| footer         | 一個網頁中，可以有多個 `<footer>` |
|                | 適合用來表示版權資訊 |
|                | 適用用來表示相關的文章連結資訊 |
|                | 版尾用來放置一些版權宣告、 隱私條件 、合作提案...等訊息。|
| main           | 一個 `<main>` 在一個網頁裡面只能出現 一次 |
|                | `<main>` 不能被放到 `<article>`、 `<aside>`、 `<footer>`、 `<header>` 、 `<nav>`  裡面。 |
| mark           | 文字中要突顯的部分   |
| nav            | 導覽列 |
| summary        | 定義 `<details>` 元素之可見標題 |
| time           | 適合用來表示時間     |

### figure

```html
<figure>
  <img src="img_pulpit.jpg" alt="The Pulpit Rock" width="304" height="228">
  <figcaption>Fig.1 - A view of the pulpit rock in Norway.</figcaption>
</figure>
```

* [demo](http://www.w3schools.com/TAgs/tryit.asp?filename=tryhtml5_figcaption)

http://www.w3schools.com/TAgs/tag_figure.asp
http://www.w3schools.com/TAgs/tag_figcaption.asp

### 延伸閱讀

* http://www.w3schools.com/html/html5_semantic_elements.asp
* [[HTML5]main用法 - IL Night](http://49night.azurewebsites.net/html5-main%E7%94%A8%E6%B3%95/)