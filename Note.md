---
tital: 全端工程師是目標
---

# 學習規劃 - 前端


| 週 日期 | 項目 | 完成 |
| -------- | -------- | -------- |
| 2025/9/2~3     | 理解觀念/目標 熟悉Figma     | Text     |
| 2025/9/4~6     | 調整figma 練習CSS     | Text     |
| 2025/9/7~17    | 依照figma實作     | Text     |
| 2025/9/18~19   | 練習javascript     | Text     |
| 2025/9/19~22   | 整理筆記     | Text     |



# Figma
目標 :　參考Wix範本，利用Figma設計
[(半)成品](https://www.figma.com/design/MZHKH8DihZ0Xw4rJHYdPUs/My-Websit?node-id=42-1486&t=4iUvg6j9GMFVP4SN-1)

## 目錄
1. [觀念(模板)](##觀念)
2. [常用工具 (Auto Layout、Grid Layout、Component、variables)](##常用工具)
3. [Figma -> Code流程](##Figma轉cdoe)


## 觀念
[FigJam](https://www.youtube.com/watch?v=EuEx8QG-Hsg): 可即時共編、開會使用
[Figma基礎圖文教學](https://frankknow.com/figma-tutorial/) :　

- Section 算是一個工作區域，可以用來裝所有的元素(沒辦法建立 Prototype 原型)。
- Frame 就像是框架，裡面可以加入各種設計區塊，另外在建立 Frame 框架時，Figma 有內建各種裝置（像是桌電、筆電、手機等）尺寸，方便你快速套用。
Section 就是一個框住所有設計的容器，而 Frame 則是實際在進行設計的畫框

[Figma模板](https://www.youtube.com/watch?v=grx15y24rOs) :
Page
- 關於 About ：介紹專案內容包含封面背景介紹 (可以以PPT呈現)
- 交付 Handoff YY.MM.DD
- 設計 Design：設計頁面
- 研究 Research：參考資源 
- 儲藏室 Archive：

## 常用工具
### [**Auto Layout**](https://youtu.be/0at62AAKntA?si=hCpZqxUP0kE2jMQV)
Elements：Text Shape Image等
Components：由Elements組成，bar slid card等
Frame(Container)：裝Elemenets、Components
Gap&Padding填充：各元件在Comtainer中的間距

主要參數：
Layout佈局：Horizontal、Vertical、Warp
間距設置：Gap間隙、Padding邊距
Alignment對齊位置：九宮格
Resizing彈性尺寸：Fixed、Hug(包住內容物)、Fill(填滿外部容器)

### **[Grid Layout](https://youtu.be/pyRfWJg_NdI?si=ZLSXpvUlkwVdZI6d)**
* 一致性：確保不同頁面或元件之間的對齊標準一致。
* 排版規劃：模擬網站的 Grid System（如 Bootstrap 的 12 欄網格）。
* 響應式思維：在設計時就考慮「哪些是主要區塊、哪些是間距」。
* 協作溝通：工程師可以直接參考 Grid 標線，轉換成 CSS grid 或 flex。


### **[Component](https://)**
**設計流程**
1. 建立元件（Component） → 移到 Local Components Page（集中管理）。
2. 在 Design page → 從 Assets 拉出需要的 Instance。
3. Instance 自動繫結到母體元件 → 之後要改樣式只改一次，全部跟著變。

**常用操作**
Add auto layout (auto lyout) ： shift + A
Turn it to Component (component)：ctrl + Alt + K


### [Figma variables](https://youtu.be/1ONxxlJnvdM?si=4kjeL9NN4YhQJlrM)
因為css的關係，決定先將Figma調整的更完整，套用variable也有助於CSS實作。
４種Variables：Color、Number、String、Boolean

Color建議要先建立library再對應Token，Font-size直接使用Library即可

**Variables collection** 建立Library，命名以顏色為主非用途(cherry 50 200 400...)。
標準色票/字體庫，目的為**一致性**。

**Tokens** [create collection]，這次命名依照實際用途(primary bg...)。
功能語境化的變數，目的為**可維護性**、**可擴充性**。
![image](https://hackmd.io/_uploads/rywvxNLclx.png)

影片有提到[design systems](https://www.youtube.com/watch?v=YLo6g58vUm0)去看了一些，總結是跟coding style挺像的(? 由於我想先以時作為主，這次先不深入研究。
- 不一定每個人都需要design sysetems
- 每個團隊/公司有不同的design systems
- 可有利於溝通、展示、減少反覆製作元件的時間 

#### 疑問
Q1. 每個按鈕顏色不同，是否抽token?
A1. 純裝飾不用，有意義(submit、resume等)要


---

## 常用元件
### [**navbar**](https://www.youtube.com/watch?v=bh98SF7OjUk&list=TLPQMDIwOTIwMjW6BkUjxa0ewg&index=3)
1. add Text(list item)
2. Add auto layout ： shift + A
3. Text Style
4. Turn it to  Component，Move to  Component Page，from Assets 新增元件至 Design Page。
(Assets裡面是 **元件副本（Instances）** )
5. from Assets add *nav / list item*，copy，select them，Add auto layout，Component，(可選)Duplicate 「建立副本（複製品）」 ： ctrl + D ， Add Button，Move to Component Page。

### [**button**](https://www.youtube.com/watch?v=KnmxD8LvHmA)
1. 新增Text，auto layout，compontnt，add variant
2. (可選)單獨選取Text，可Apply variable/property

<div style="display:flex; align-items:center; gap:20px;">
  <img src="https://hackmd.io/_uploads/r1xkNON9ll.png" width="500">
  <p>選取文字元件，找到圖示Apply variable/property</p>
</div>

<div style="display:flex; align-items:center; gap:20px;">
  <img src="https://hackmd.io/_uploads/SJrlB_N9xg.png" width="500">
  <p>可選擇文本、開關等變數(但我還不太會用qwq)，建立後可再調整預設狀態、內容</p>
</div>

<div style="display:flex; align-items:center; gap:20px;">
  <img src="https://hackmd.io/_uploads/Hkm0ruNqge.png" width="500">
  <p>元件副本（Instances） 可使用參數調整內容</p>
</div>

主要就是當我們改變Components時，Instances的參數內容可以保留不變。
ex:可能大多數按鈕底色為灰，現在要改變成紅色，但我有個按鈕是藍色不想被改變，此時就可以派上用場。在調整文字內容時也比較方便。

更多內容可能有關 [variable](https://youtu.be/1ONxxlJnvdM?si=4kjeL9NN4YhQJlrM) ，但較進階這邊先跳過，待完成目標後再補學。

[**按鈕prototype影片教學**](https://www.youtube.com/watch?v=__jVKBouojE)可用來複習簡單的prototype用法


**Q1. Auto layout、Frame好難。**
A1：你的理解對的，但 Content 高度建議 Hug 而不是 Fill(code另外處理?)；Gap 必須多包 Frame，這是 Flexbox 限制不是你錯。

**Q2. Component更新，Instance未同步。**
A2：Instance 不同步，多半是連結斷掉（Detach / 複製錯），不是單純移動造成的。解法是 Swap instance。

**Q3. Component時機不會抓**
A3：不要為每個小文字建 Component → 以「區塊是否重複」來決定；必要時抽小元件組合。

---

## Figma轉cdoe
1. 建專案骨架（index.html、components.html、css/tokens.css、css/layout.css、css/components.css。)
2. 填 tokens.css：把 Figma 的 color/typography/spacing/roundness 貼進去。
3. components.html 做 3 個元件（先從高頻開始）：
    * Button（主色 / 次色 / ghost、大小、disabled；hover/active/focus）
    * Card（標題/內文/行高、內距、陰影）
    * Navbar（左 LOGO + 中間連結 + 右 CTA；RWD 切換行為先簡化
4. index.html 組版：
    * 先拉容器與各 section，放入剛做好的元件。
    * 用 layout.css 的 grid/flex 工具排好三段 RWD。
5. 微調：
    * 細節（行高、間距、對齊、斷點時的字級）
    * 無障礙（語義化標籤、alt、焦點樣式）
    * 效能（圖片 WebP、loading="lazy"）

---

# HTML
### 網頁區塊常用名稱
**[Container運用in Figma (YT)](https://www.youtube.com/watch?v=fghWUZfkyew)**

#### 頁面結構範例
Header（頁首/導覽列）
Hero（橫幅 / 首屏大圖）
Intro / About（介紹 / 關於我們）
Features（功能特色）
Services（服務項目）
Portfolio / Showcase（作品集 / 案例展示）
Testimonials（客戶推薦）
Pricing（價格方案）
FAQ（常見問題）
Contact（聯絡我們 / 表單）
Footer（頁尾 / 底部）
| 區塊名稱  | 英文                                | 說明                                                         |
| ----- | --------------------------------- | ---------------------------------------------------------- |
| 公司資訊  | **Company Info / About**          | 公司名稱、簡介、Logo、成立年份。                                         |
| 聯絡資訊  | **Contact Info**                  | 地址、電話、Email、客服連結。                                          |
| 社群連結  | **Social Media Links**            | Facebook、Instagram、LinkedIn、YouTube… 圖示超連結。                |
| 主要導覽  | **Main Navigation / Quick Links** | 重複 Header 的部分選單，幫助用戶快速跳轉。                                  |
| 法律條款  | **Legal / Policy**                | 版權聲明、隱私權政策（Privacy Policy）、使用條款（Terms of Service）、Cookies。 |
| 訂閱表單  | **Newsletter / Subscription**     | Email 訂閱框、CTA 按鈕（例如「訂閱最新消息」）。                              |
| 語言切換  | **Language Switcher**             | 多語言選擇（中文 / 英文 / 日文等）。                                      |
| 合作與認證 | **Partners / Certifications**     | 合作夥伴 Logo、安全認證標章（SSL、PCI DSS、ISO…）。                        |
| 付款方式  | **Payment Methods**               | 信用卡、PayPal、Line Pay、Apple Pay… 圖示。                         |
| 版權資訊  | **Copyright**                     | 「© 2025 YourCompany. All Rights Reserved.」                 |


### 常見裝置寬度（px）
| 裝置類型             | 寬度範圍 (px)        | 長度範圍 (px)        | 備註                                          |
| ---------------- | ---------------- | ---------------- | ------------------------------------------- |
| 📱 手機            | **320 – 480**    | **568 – 896**    | 最小 iPhone SE (320×568) 到大尺寸手機 (414×896)     |
| 📱📲 大螢幕手機 / 小平板 | **414 – 600**    | **736 – 960**    | iPhone Plus / Pixel XL、部分小型平板               |
| 📟 平板            | **600 – 1024**   | **800 – 1366**   | iPad Mini (768×1024) 到 iPad Pro (1024×1366) |
| 💻 小筆電 / 小桌機     | **1024 – 1366**  | **600 – 768**    | 常見低解析度筆電（1366×768）                          |
| 🖥️ 一般桌面螢幕       | **1366 – 1920**  | **768 – 1080**   | 常見桌機 / 筆電 Full HD                           |
| 🖥️ 大型桌面螢幕       | **1920 – 2560+** | **1080 – 1440+** | 2K / 4K 顯示器                                 |

### 基礎範本
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Web Page</title>
    <link rel="stylesheet" href="styles.css">   
    <script src="script.js" defer></script>
</head>
<body>
    <header>
        <h1>Welcome to My Web Page</h1>
    </header>
    <main>
        <p>This is a simple web page with HTML, CSS, and JavaScript.</p>
        <button id="myButton">Click Me!</button>
    </main>
    <footer>
        <p>&copy; 2024 My Web Page</p>
    </footer>
</body>
</html>
```

#### [meta](https://developer.mozilla.org/zh-TW/docs/Learn_web_development/Core/Structuring_content/Webpage_metadata)
- [OG標籤屬性](https://frankknow.com/open-graph-tag/) Open Graph分享置社群時的相關(title description image url)設定。
```html
<meta charset="UTF-8">  <!--這個網頁的編碼-->
<meta name="viewport" content="width=device-width, initial-scale=1.0">  <!--這個網頁要怎麼在行動裝置顯示-->
<meta name="description" content="A simple web page example"> <!--這個網頁的描述，google底下的灰字內容-->
<meta name="keywords" content="HTML, CSS, JavaScript, Web Development"> <!--這個網頁的關鍵字，google底下的灰字內容-->
<meta name="author" content="Eva"> <!--這個網頁的作者-->

<meta property="og:title" content="My Web Page"> <!--這個網頁分享到社群的標題-->
<meta property="og:description" content="A simple web page example"> <!--這個網頁分享到社群的描述-->
<meta property="og:image" content="https://example.com/image.jpg"> <!--這個網頁分享到社群的圖片-->
```

---

# CSS 
## 📑 目錄

1. [CSS觀念](#CSS觀念)
2. [Lyout Container設計概念](#Lyout-Container設計概念)
3. [未來/過去可能出錯的地方](#未來/過去可能出錯的地方)
4. [font、border、shadow、margin、padding](#字體font邊框border陰影shadow邊距margin內邊距padding)
5. [img](#img)
6. [icon](#icon)
7. [overflow、float、display、poitino](#overflow、浮動float、display、定位position)
8. [選擇器](#選擇器)
9. [background(透明)](#background)
10. [偽類pseudo classes](#偽類pseudo-classes)
11. [偽元素 pseudo element](#偽元素-pseudo-element)
12. [Flexbox](#flexbox)
13. [Grid](#grid)
14. [Flex vs. Grid](#flex-vs-grid)
15. [Transform變形、 Animation動畫、Transition過度](#transform變形-animation動畫)
16. [transform](#transform)
17. [Canvas 繪圖](#canvas-繪圖)
18. [RWD](#RWD)
19. [3D](#3D)

---

### [CSS觀念](https://www.youtube.com/watch?v=S6os7SrnzCI&list=PLpZ8gOBZmTy4BTBs5VFAgk-VPcAN2Shci)
Tips：VScode用Live Preview比較好用  


**CSS檔案引入**  
[引入css相關文章](https://medium.com/@small2883/css-%E7%9A%84%E4%B8%89%E7%A8%AE%E5%BC%95%E5%85%A5%E6%96%B9%E5%BC%8F%E6%9C%89%E5%93%AA%E4%BA%9B-58dc7570bb9c)
```
<head>
    <link rel="stylesheet" type="text/css" href="style.css">
</head>
```

```
<style>
    @import url(style.css);
</style>
```

1.link是XHTML標籤，除了加載CSS外，還可以定義RSS等其他事務；@import屬於CSS範疇，只能加載CSS。

2.link引用CSS時，在頁面載入時同時加載；@import需要頁面網頁完全載入以後加載。

3.link是XHTML標籤，無兼容問題；@import是在CSS2.1提出的，低版本的瀏覽器不支持。在IE5以上才能識別

4link支持使用Javascript控制DOM去改變樣式；而@import不支持。

5 .link方式的樣式的權重 高於@import的權重.

---

**三種使用方式**
Inline Styling：同一行
Embedded Styling： ＜style＞
External Stylesheets：style.css

指定id style #

---

### Lyout Container設計概念
一、 Layout(header、section、footer) 
只管位置。
用來劃分版型，不要有外邊距，内邊距有的話用上下(屬於版型，不是用來控制內容物)，不要影響到內層container。
margin = 0;
padding-block: 4rem;


二、Container
控制內容物的最大寬度+排版。
區塊內排版另創一個延續band的class，使用grid，不要使用多個/層container。
```css
/* band 自己的上下留白、背景在 section 上 */
.hero { padding-block: 4rem; background: var(--color-surface); }

/* 版心：每個 band 一次即可 */
.container { width: min(100% - 2rem, var(--container)); margin-inline: auto; }

/* 版內排版用 grid/flex，不要再用 .container */
.hero-grid {
  display: grid;
  gap: var(--space-8);
}
@media (min-width: 900px){
  .hero-grid { grid-template-columns: 1.1fr .9fr; }
}

.button-group { display: flex; gap: var(--space-3); flex-wrap: wrap; }

```

---

### 未來/過去可能出錯的地方
* margin 用px的數字過大可能導致無用。
* display: inline無法設定width、height、overflow等，沒有固定大小
* 預設 body 會有 margin 8px
* 用列表ul il發現視覺上看起來偏右，因為ul預設有padding-left 40px，可以初始化解決(如下)。
```html
#list ul{
  margin: 0;                      /* 移除預設上下外距 */
  padding: 0;                     /* 移除預設左縮排 */
  list-style: disc inside;        /* 圓點放到內容盒內，視覺不再往右推 */
  /* 或者：list-style: none; 自己用 ::before 畫圓點 */
}
```

---

### **字體font、邊框border、陰影shadow、邊距margin、內邊距padding**
**顏色表示**：內建名稱、rgb(225,225,225)、hsl(100,60%,60%)、16進制#FFFFFF

**大小表示方式**：
* px (像素)：直覺，但不會隨瀏覽器縮放。
* em：相對於父元素字體大小，層層相乘。
* rem(root em)👑：相對於根元素大小，不會層層相乘。1rem = 16px。
* vw寬 / vh高 視窗單位：可做流體字體，太大或太小螢幕會失衡，需要搭配 clamp()。背景container可用。
```css
/*常用設置方式*/
font-size: clamp(最小值, 偏好值, 最大值);
```


```css
<style>
    h1 {
        font-family: Arial, sans-serif;  /*標題字體*/
        font-size: 36px;       /*標題字體大小 1em=100%*/
        font-weight: bold;     /*標題粗體 normal 500 800*/
        font-style: italic;   /*標題斜體 normal italic*/
        color: blue;           /*標題顏色*/
        text-align: center;    /*讓inline-block元素置中*/

        border-style: ridge;    /*內文邊框樣式 none solid dashed虛 dotted虛 double groove ridge inset按下 outset未按*/
        border-top: 1px solid red;   /*上邊框 (會覆蓋原本的style)*/

        text-shadow: 2px 2px 5px gray;  /*文字陰影 水平 垂直 模糊 顏色*/
        box-shadow: 2px 2px 5px gray;   /*區塊陰影 水平 垂直 模糊 顏色*/

        margin: 1rem 1rem 2rem 4rem;    /* 標題外距 上右下左 */
        margin: 20px 0px 90px ; /*標題外距 top right/left bottom*/
        margin: 0 auto;         /* 上下 0，左右自動 → 水平置中 */
        
        padding: 0.5rem;    /*內距0.5rem 1rem=16px*/
    }
</style>
```

**字形引入:**
[google font](https://fonts.google.com/)找到要的字體[Get font] > [Get embed code] 依照說明引入字體。
![image](https://hackmd.io/_uploads/Hk8nVnO5lx.png)

**margin注意事項**：
固定用「container + auto」置中，而不是隨便給大 margin
```css
.container {
  max-width: 1200px;
  margin: 0 auto; /* 自動置中 */
  padding: 0 1rem; /* 保持左右留白 */
}
```

元素之間用 gap 而不是 margin（特別是 flex/grid 排版）
```css
.cards {
  display: flex;
  gap: 2rem; /* 取代 margin-right */
}
```

---

### [img](https://developer.mozilla.org```/zh-CN/docs/Web/HTML/Reference/Elements/img)
```
object-fit: cover;
```
| 值            | 行為說明                         |
| ------------ | ---------------------------- |
| `fill`（預設）   | 拉伸圖片，強迫填滿容器（會變形）             |
| `contain`    | 等比例縮放，整張圖片完整顯示，可能有留白         |
| `cover`      | 等比例縮放，填滿容器，多餘部分裁掉            |
| `none`       | 不縮放，維持原始大小                   |
| `scale-down` | `none` 和 `contain` 之間，取較小的效果 |

---

### [icon](https://fontawesome.com/search?ic=free&o=r)
```css
<head>
    <script src="https://kit.fontawesome.com/870689de5b.js" crossorigin="anonymous"></script>
</head>

<body>
    <script src="https://kit.fontawesome.com/870689de5b.js" crossorigin="anonymous"></script>
</body>
```

---

### overflow、浮動float、display、定位position
<div style="display:flex; gap:20px; align-items:flex-start;">
  <div>
    <p style="font-weight:bold">float</p>
    <p>可實現文繞圖，注意用 float: right; 順序會相反 (第三會被排到第一)。</br>float 的效果是讓「inline 或 inline-block 的內容」繞在旁邊，不是 block＜div＞。</p>
  </div>
  <img src="https://hackmd.io/_uploads/S1AIzOIqlx.png" width="200">
</div>

**display**：
inline-block行內區塊 可以設定長寬，inline不行。
flex獨佔一整行


```css
div {
    width: 100px;
    height: 100px;
    border: 1px solid black;
    margin: 10px;
    overflow: hidden;   /*內容超出區塊時的處理方式 visible顯示 hidden隱藏 scroll捲軸 auto自動*/
    float: right;    /*none不浮動 left左浮動 right右浮動 unset取消浮動*/    
    display: inline-block;   /*區塊元素 inline行內元素 inline-block行內區塊元素 block區塊元素 none不顯示*/                        
}
```

**position**
父容器<span style="background-color: #E0E0E0; padding:5px; border-radius: 5px;">position: relative; /*讓絕對定位的子元素參考此元素定位*/ </span>

```css
#item1 {
    position: absolute;  /*絕對定位。可用於卡片右上角的「關閉 X」按鈕*/
    top: 20px;   /*上方20px*/
    left: 100px;  /*左方20px*/
    background-color: lightblue;
}   
#item2 {
    position: fixed;  /*固定定位。可用於返回位頂*/
    bottom: 20px;   /*下方20px*/
    right: 20px;  /*右方20px*/
    background-color: lightgreen;
}
#item3 {
    position: sticky;  /*黏著定位。可用於bar*/
    top: 0;   /*上方0px*/
    background-color: lightcoral;
}
```

---

### 選擇器
* id：同個頁面不能重複出現同名稱，"#idname {}"
* class：可重複，".classname {}"

**多選擇器**
```css
p, li, a {
    color: blue;
    font-size: 20px
}
```

**孫選擇器**
```css
.container > div > p {
    color: red;     /*選擇container底下的div底下的p元素*/
}
```
還有**鄰居、屬性、第n項選擇器**等，但避免過度依賴HTML結構所以較少使用，這邊不詳細紀錄。


**選擇器權重**
inline css > id > class > 元素(div p...) > !important(不要用 難維護)


**相鄰兄弟選擇器**
`+` = 相鄰兄弟選擇器，鎖定「前面緊跟著某元素的那個元素」。
```css
.nav__item {
/*  前面有nav__item的才加一條線(=  第一個以外)    */
  .nav__item + .nav__item {
    border-left: 1px solid #000;
  }
}
```

---

### background
```css
body{
    background-image: url("bg.jpg");  /*背景圖片*/
    background-size: cover;  /*背景圖片覆蓋整個視窗*/
    background-repeat: no-repeat;  /*背景圖片不重複*/
    background-position: center;  /*背景圖片置中*/
}
```

##### 透明底色
```css
background: color-mix(in  srgb, #b11515 10%, transparent);   /* 透明度背景色 數字越小越透 */
backdrop-filter:saturate(180%) blur(8px)    /* 玻璃效果 saturate飽和度 blur背景模糊效果*/
opacity:0.4;    /* 數字越小 越透明(全部透明) */ 
background-color: transparent;   /* 只有背景變透明 */

```

---

###  偽類pseudo classes
應用實例：action連結點擊變色、hover換色等
```css
a:link {
    color: blue;  /*未訪問過的連結顏色*/
}
a:visited {
    color: purple;  /*已訪問過的連結顏色*/
}
a:hover {
    color: orange;  /*滑鼠移到連結上顏色*/
}
a:active {
    color: red;  /*點擊連結時顏色*/
}
li:hover {
    background-color: lightgray;  /*滑鼠移到列表項目上背景顏色*/
}   
li:not(:hover) {
    background-color: white;  /*滑鼠未移到列表項目上背景顏色*/
}
```

---

### 偽元素 pseudo element
應用實例：selection反白換色、before元素前加東西、marker(只換色/大小，形狀於ul使用list-style-type)
```css
#list ul {
    list-style-type: square;  /*列表項目符號樣式*/
    padding: 0px;  /*內距*/
    margin: 0px;  /*外距*/
    list-style: disc inside;        /* 圓點放到內容盒內，視覺不再往右推 */
}
#list li::marker {
    color: red;  /*列表項目符號顏色*/
    font-size: 20px;  /*列表項目符號大小*/
}
#list li::after {
    content: " ✔";  /*列表項目後面加上勾勾*/
}
```
* :after 舊寫法（CSS2 時代），現在還能用。現在的pseudo classes
* ::after 新寫法（CSS3 規範），建議優先使用。現在的pseudo element
* 功能一模一樣，只是語法標準不同。

---

### Flexbox [w3schools](https://www.w3schools.com/css/css3_flexbox.asp)
<!-- Flexbox 快速對照卡（HackMD 可直接貼） -->
<div style="font-family:system-ui,-apple-system,Segoe UI,Roboto,Helvetica,Arial; line-height:1.65;">

  <h2 style="margin:0 0 12px;">Flexbox 快速對照表</h2>

  <table style="width:100%; border-collapse:collapse; border:1px solid #e5e7eb;">
    <thead>
      <tr style="background:#f3f4f6;">
        <th style="-align:left; padding:10px; border-bottom:1px solid #e5e7eb;">屬性</th>
        <th style="text-align:left; padding:10px; border-bottom:1px solid #e5e7eb;">用途說明</th>
        <th style="text-align:left; padding:10px; border-bottom:1px solid #e5e7eb;">常用值</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td style="padding:10px; border-top:1px solid #f1f5f9;"><code>flex-direction</code></td>
        <td style="padding:10px; border-top:1px solid #f1f5f9;">排序方向</td>
        <td style="padding:10px; border-top:1px solid #f1f5f9;"><code>row</code> / <code>row-reverse</code> / <code>column</code> / <code>column-reverse</code></td>
      </tr>
      <tr>
        <td style="padding:10px; border-top:1px solid #f1f5f9;"><code>justify-content</code></td>
        <td style="padding:10px; border-top:1px solid #f1f5f9;">水平對齊（主軸對齊）</td>
        <td style="padding:10px; border-top:1px solid #f1f5f9;"><code>flex-start</code> / <code>center</code> / <code>flex-end</code> / <code>space-between</code> / <code>space-around</code> / <code>space-evenly</code></td>
      </tr>
      <tr>
        <td style="padding:10px; border-top:1px solid #f1f5f9;"><code>flex-wrap</code></td>
        <td style="padding:10px; border-top:1px solid #f1f5f9;">換行</td>
        <td style="padding:10px; border-top:1px solid #f1f5f9;"><code>nowrap</code> / <code>wrap</code> / <code>wrap-reverse</code></td>
      </tr>
      <tr>
        <td style="padding:10px; border-top:1px solid #f1f5f9;"><code>align-items</code></td>
        <td style="padding:10px; border-top:1px solid #f1f5f9;">單行垂直對齊（交叉軸對齊）</td>
        <td style="padding:10px; border-top:1px solid #f1f5f9;"><code>stretch</code> / <code>flex-start</code> / <code>center</code> / <code>flex-end</code> / <code>baseline</code></td>
      </tr>
      <tr>
        <td style="padding:10px; border-top:1px solid #f1f5f9;"><code>align-content</code></td>
        <td style="padding:10px; border-top:1px solid #f1f5f9;">多行垂直對齊（多列時生效）</td>
        <td style="padding:10px; border-top:1px solid #f1f5f9;"><code>stretch</code> / <code>flex-start</code> / <code>center</code> / <code>flex-end</code> / <code>space-between</code> / <code>space-around</code></td>
      </tr>
      <tr>
        <td style="padding:10px; border-top:1px solid #f1f5f9;"><code>align-self</code></td>
        <td style="padding:10px; border-top:1px solid #f1f5f9;">單一子元素的垂直對齊</td>
        <td style="padding:10px; border-top:1px solid #f1f5f9;"><code>auto</code> / <code>stretch</code> / <code>flex-start</code> / <code>center</code> / <code>flex-end</code> / <code>baseline</code></td>
      </tr>
    </tbody>
  </table>

  <!-- 圖片區：自適應並排 -->
  <h3 style="margin:18px 0 10px;">示意圖</h3>
  <div style="display:flex; flex-wrap:wrap; gap:12px;">
    <figure style="margin:0; flex:1 1 280px;">
      <img src="https://hackmd.io/_uploads/Syt7Tfvqgg.png" alt="示意圖1" style="width:100%; border:1px solid #e5e7eb; border-radius:8px;">
    </figure>
    <figure style="margin:0; flex:1 1 280px;">
      <img src="https://hackmd.io/_uploads/Bknr6GD5el.png" alt="示意圖2" style="width:100%; border:1px solid #e5e7eb; border-radius:8px;">
    </figure>
    <figure style="margin:0; flex:1 1 280px;">
      <img src="https://hackmd.io/_uploads/rkC_pfDcee.png" alt="示意圖3" style="width:100%; border:1px solid #e5e7eb; border-radius:8px;">
    </figure>
    <figure style="margin:0; flex:1 1 280px;">
      <img src="https://hackmd.io/_uploads/HkavazP9xe.png" alt="示意圖4" style="width:100%; border:1px solid #e5e7eb; border-radius:8px;">
    </figure>
  </div>

  <!-- 小抄：快速複製的容器範例 -->
  <div style="margin-top:16px; padding:12px; background:#f0f9ff; border:1px solid #bae6fd; border-radius:8px;">
    <strong>範例容器：</strong>
    <pre style="white-space:pre-wrap; margin:8px 0 0;"><code>.box {
  display: flex;
  flex-direction: row;        /* 排序方向 */
  justify-content: center;    /* 水平對齊 */
  align-items: center;        /* 單行垂直對齊 */
  flex-wrap: wrap;            /* 換行 */
}</code></pre>
  </div>
</div>

* flex-grow 依照設定的比例分配剩餘空間(0)
* flex-basis 元素是否進行伸縮(0)
* flex-shrink 當元素>容器寬度會進行壓縮，數字約大 壓縮越多。(要固定寬度，寬度不夠才會壓縮)
```css        
.item {
        width: 100px;
        flex: 1,1,10px;  /*flex-grow   flex-shrink flex-basis*/
        flex-grow: 1;   /*1等寬， 2,3...倍 彈性盒子放大比例*/
        flex-shrink: 1;  /*1會自動縮小彈性盒子縮小比例*/
        flex-basis: 10px;  /*10px(優先序高);0忽略內容寬度;auto一內容大小作為彈性盒子基準寬度*/
      }
```

[**flex練習**](https://flexboxfroggy.com/)
- flex-direction 如果row轉column水平跟垂直會交換。
```
#pond {
  display: flex;
flex-direction: row-reverse;   /*reverse之後排序調換*/
justify-content: flex-end;    /*要用end才會靠左*/
}
```

- oreder: -1;等 通常用於指定單一種類的順位。
```
.yellow {
    order: -1;    /*黃色物品優先序為-1(高)*/
}
```

---

### [grid](https://www.youtube.com/watch?v=EiNiSFIPIQE)
欄寬依內容而定，常用關鍵字：
* `max-content`：欄寬 = 內容不換行時所需寬度（越長越寬）
* `min-content`：欄寬 = 內容能接受的最小寬度（會盡量換行；遇到無法斷行的長字就以它為下限）
* `fit-content(<長度>)`：以內容為主，但不超過指定上限
```css
/* A. 左欄等於內容寬、右欄吃剩下 */
.item{
  display:grid;
  grid-template-columns: max-content minmax(0,1fr);
  column-gap: 1rem;
}
.item__date{ white-space: nowrap; } /* 想確保日期不換行可加 */
```


可能會用到的一些語法
```css
.test-container {
    background-color: lightsalmon;
    display: grid;
    grid-template-columns: 1fr 2fr repeat(2, 1fr); /*第一欄1份，第二欄2份，接下來兩欄各1份*/
    grid-template-rows: 200px repeat(3, 100px); /*第一列200px，接下來三列100px*/
    gap: 10px;  /*格子之間的間距*/
} 

.test-container > span {
    border: 2px solid black;
    width: 100%;  /*讓span佔滿整個格子(gird)*/
    height: 100%; /*讓span佔滿整個格子(gird)*/

    display: flex;  /*讓span裡面的文字置中*/
    justify-content: center; /*必要flex 讓span裡面的文字置中*/
    align-items: center;  /*必要flex 讓span裡面的文字置中*/
}
.item1 { 
  /*grid-column: 1 / 4;   /*從第一欄開始，跨到第四欄結束，也就是跨三欄*/
  /*grid-row: 1 / 2;  /*從第一列開始，到第二列結束，也就是只佔第一列*/
  grid-area: 1 / 1 / 2 / 4; /*row-start col-start row-end col-end*/
  background-color: lightblue; 
}
.item2 {
  grid-column: span 2; /*不論你讀得起點 跨兩欄，若同列的grid不夠 會換行開始*/
  background-color: lightgreen; 
}
```
![image](https://hackmd.io/_uploads/SJY7-aKqeg.png)


排版很好用的樣子(?
```css
.test-container {
    background-color: lightsalmon;
    display: grid;
    grid-template-columns: 1fr 2fr 1fr; /*第一欄1份，第二欄2份，接下來兩欄各1份*/
    grid-template-rows: 100px 300px 100px; 
    grid-template-areas:  /*定義區域名稱 非相鄰名稱不能重複*/
      "header header header"
      "aside1 main aside2"
      "footer footer footer";
} 

.item1 { 
  grid-area: header;
  background-color: lightblue; 
}
.item2 {
  grid-area: aside1;
  background-color: lightgreen; 
}
.item3 { 
  grid-area: main;
  background-color: lightpink; 
} 
.item4 { 
  grid-area: aside2;
  background-color: lightgray; 
}
.item5 { 
  grid-area: footer;
  background-color: lightyellow; 
}
```
![image](https://hackmd.io/_uploads/BJMMQTt9lg.png)


控制grid內的某個元件

```css
.test-container {
  background-color: lightsalmon;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(3, 100px);
  gap : 5px;
} 

.item {
  padding: 5px;
  display: flex;    
  justify-content: center;  /* (必要flex)item內文字 水平置中 */
  align-items: center;      /* (必要flex)item內文字 垂直置中 */
  border: 1px solid #000;
}

.item1 { 
  justify-self: center;    /* (不用flex)item1本身 水平置中 */
  align-self: stretch;     /* (不用flex)item1本身 垂直撐滿 */
  background-color: lightblue; 
}
```

---

### Flex vs. Grid
| 特性   | Flex                  | Grid                        |
| ---- | --------------------- | --------------------------- |
| 維度   | 一維（row 或 column）      | 二維（row + column）            |
| 對齊方式 | 彈性分配空間                | 明確座標、行列控制                   |
| 容易度  | 較直覺，簡單排水平/垂直          | 複雜，但功能更強大                   |
| 常見用途 | Navbar、按鈕列、垂直堆疊、置中    | 整頁框架、複雜佈局、圖片牆               |
| RWD  | 靠 `flex-wrap` 和 `gap` | 靠 `auto-fit / minmax()` 更強大 |

---

### Transform變形、 [Animation動畫](https://developer.mozilla.org/zh-TW/docs/Web/CSS/CSS_animations/Using_CSS_animations)、Transition過度
```html
#box1 {
    transform: translateX(100px) rotateZ(20deg) scale(1.2);  /*平移X100px, Y50px，旋轉20度，放大1.2倍*/
}   
```
```css
#box1 {
    animation: slide-right 1s forwards;  /*動畫名稱 動畫持續時間 動畫結束後保持最後一幀*/
    animation-name: slide-right;  /*動畫名稱*/
    animation-duration: 1s;  /*動畫持續時間*/
}   

@keyframes slide-right {
    from {
        transform: translateX(100px);
    }
    to {
        transform: translateX(50%);
    }     
}
```

#### Transition
`transition: <property> <duration> <timing-function> <delay>;`
| 項目                | 說明      | 範例                                                       |
| ----------------- | ------- | -------------------------------------------------------- |
| `property`        | 要動畫的屬性  | `width`、`height`、`opacity`、`transform`…                  |
| `duration`        | 動畫持續時間  | `0.5s`、`200ms`                                           |
| `timing-function` | 動畫速率曲線  | `linear`、`ease`、`ease-in`、`ease-out`、`cubic-bezier(...)` |
| `delay`           | 延遲多久才開始 | `0s`、`1s`                                                |

```=css


```

#### 控制速率曲線：
* `linear`：等速
* `ease`：慢 → 快 → 慢（預設）
* `ease-in`：慢 → 快
* `ease-out`：快 → 慢
* `ease-in-out`：慢 → 快 → 慢
* `cubic-bezier(x1,y1,x2,y2)`：自訂曲線


#### 動畫練習
按Start幫id=text加.effect class，按Stop移除。
Switch可切換text是否有effect，並會改變按鈕文字。
1. 設定動畫@keyframes
2. 設定動畫class
3. 設定JS邏輯(套用到物件上)
```css
<style>
    .effect {
        animation: blink 1s infinite;  /*動畫名稱 動畫持續時間 無限次數*/
    }
    @keyframes blink {
        0% {opacity: 1;}
        50% {opacity: 0;}
        100% {opacity: 1;}
    }
</style>

<script>
    function start() {
        var text = document.getElementById("text");
        text.classList.add("effect");  /*加入class*/
        // text.classList.remove("effect");  /*移除class*/
        // text.classList.toggle("effect");  /*切換class 有就移除 沒有就加入*/
    }
    function stop() {
        var text = document.getElementById("text");
        text.classList.remove("effect");  /*移除class*/
    }

    function switchh() {
        var text = document.getElementById("text");
        text.classList.toggle("effect");  /*切換class 有就移除 沒有就加入*/
        
        var btn = document.getElementById("switchh");
        if (text.classList.contains("effect")) {
            btn.innerText = "Stop";
        } else {
            btn.innerText = "Start";
        }
    }
</script>


<div id="text">Effect Show</div>
<button onclick="start();">Start</button>
<button onclick="stop();">Stop</button>
<button id="switchh" onclick="switchh();">Switch</button>
```

---


### [transform ](https://www.youtube.com/watch?v=9sR9MmWyhGE&list=PL-g0fdC5RMbpz9X__H5ycq1XcXxhfb5rk&index=2)
```css
.cube > .top {
    width: 240px;
    height: 60px;
    background-color: red;
    transform: skew(-45deg) translate(30px, 0); 
}
.cube > .center {
    width: 240px;
    height: 240px;
    background-color: green;
    display: inline-block;
}

.cube > .right {
    width: 60px;
    height: 240px;
    background-color: blue;
    display: inline-block;
    transform: skew(0, -45deg) translate(0,-30px); /*變形 x軸 y軸*/
}

<div class="cube">
    <div class="top"></div>
    <div class="center"></div><div class="right"></div>
</div>
```
![image](https://hackmd.io/_uploads/BJZYy4rixl.png)

---

### Canvas 繪圖
- 繪製填滿(Fill)、描邊
- 影像處理(顏色反種)
- 影像輸入、輸出 
- 影音播放與控制  

---

### RWD
```css
@media screen and (min-width: 600px) {
    .container {
        flex-direction: row;  /* 只對螢幕套用，列印不受影響。 大於600px時改為水平排列*/
    }
}
```
---
### 3D
`perspective`指定了观察者与 z=0 平面的距离。
```css
perspective: 800px;
```
`transform-style`控制元素的子元素在三維空間 (3D space) 中要如何呈現。
```css
transform-style: flat;    /*设置元素的子元素位于该元素的平面中。*/
transform-style: preserve-3d;     /* 通常父層有perspective 子層搭配這個，指示元素的子元素应位于 3D 空间中。*/
```

#### 常用
```css
 backface-visibility: hidden; /* ✅ 避免背面鏡像 */
```

---

2025/9/18 ~ 2025/9/19
# JavaScript 基礎筆記

#### [**JavaScript基礎影片**](https://www.youtube.com/watch?v=LEwi44cWBu8&t=1950s)

## **📑 目錄**

1. [基礎概念](#1-基礎概念) （引入.js、HTTP、JS vs jQuery、null/undefined、Expression/Statement）
2. [函式與作用域](#2-函式與作用域) （函式宣告、Scope、變數、Callback、匿名函式、IIFE、Hoisting）
3. [資料結構與操作](#3-資料結構與操作) Array、map）
4. [ES6 與變數管理](#4-es6-與變數管理) （var/let/const、Spread Operator、Arrow Function）
5. [迭代與迴圈](#5-迭代與迴圈) （iterator、for in、for of）
6. [API 與網頁物件模型整理](#6-API與網頁物件模型整理) （iterator、for in、for of）


## 1. 基礎概念
##### [DOM](https://ithelp.ithome.com.tw/m/articles/10241371) ：DOM 是一個將 HTML 文件以樹狀的結構來表示的模型，而組合起來的樹狀圖，我們稱之為「DOM Tree」。

### 引入.js
注意放在head可能導致偵測不到body物件。
```html
<script src="script.js"></script>
```

### HTTP 請求
- GET : 網頁開啟
- POST : (保護性)帳號密碼
- DELETE : 刪除物品

### JavaScript & jQuery
- jQuery 是用 JavaScript 組成的函式庫

### null & undefined
- null : 定義為空值  
- undefined : 未定義  

```javascript
parseInt(5/3)    // 1 轉整數
AND: &&
OR: ||
````

```javascript
n ||= 10 // 預設值，如果 n 未被賦值則 = 10
(1 >= 3) ? true : false
```

### Expression 表達式 & Statement 陳述句

* Expression: 會回傳值 (1+1)
* Statement: 不會回傳值 (if-else、switch)

---

## 2. 函式與作用域
### scope 作用域
* function 內要用 var、let、const 才不會影響到 function 外的數值。

### 變數
1. 區域變數 (多用這個)
2. 全域變數
3. 不是變數 => 全域屬性 (window 是根物件)

```javascript
z = 1;
window.z    // 1
```

### Hoisting 變數提升
* `var` 、 *Function Declaration(Statement)* 整個函式會被提升，可以在定義前呼叫
* `let` 、 `const` 、 `class` 也會被「提升」，但是進入 暫時性死區 (TDZ)，宣告前呼叫**會報錯**。


因為 hoisting 所以 `var x;` 會先執行，讓第一個 `console.log(x);` 輸出為 `undefined`。
如果是 let、const 會 Error: "Cannot access 'x'..."。
如果完全未宣告會 Error: "x is not defined"

```javascript
console.log(x);
var x = 10;
console.log(x);

function sayHello() {
    var x = undefined;
    console.log(x);
    x = 20;
    console.log(x);
}

sayHello();
```



### Function Statement(Declaration) (函式宣告式)
特點：會 Hoisting（提升），所以可以在宣告前呼叫。
```javascript
// Statement
functionName1();
function functionName1() {
    console.log("this is Statement(只有statement function可宣告前呼叫，因為變數提升)")
};
```

### Function Expression (函式表達式)
把函式「賦值」給一個變數。
```javascript
var sayHello = function() {
    console.log("Hello Expression");
};

sayHello();  // Hello Expression

```

### Anonymous Function 匿名函式
沒有名字的函式，常用在 callback。
特點：常見於事件監聽、setTimeout、map/filter 等。
```javascript
// 應用於callback funciton
setTimeout(function() {
    console.log("This is anonymous function!");
}, 1000);
```


### Immediately Invoked Function Expression (IIFE，立即執行函式)
1. 不汙染外部
2. 避免 jQuery 因 "\$" 被汙染

```javascript
(function(name) {
    console.log("Hi, " + name + " !");
})("Eva");
```

### Arrow Function（箭頭函式） (ES6)
ES6 新增，語法簡短，且不會綁定自己的 this。
1. 沒有自己的 this
1. 適合 callback、簡短函式
```javascript
const add = (a, b) => a + b;
console.log(add(3, 4)); // 7

setTimeout(() => console.log("Arrow Function!"), 1000);

```




```
// ✅ Function Declaration
sayHello();   // "Hello"
function sayHello() {
    console.log("Hello");
}

// ❌ Function Expression （函式表達式 / 匿名函式）
sayHi();      // TypeError: sayHi is not a function
var sayHi = function() {
    console.log("Hi");
};

```



---

## 3. 資料結構與操作

### Array 陣列

```javascript
var arr = [0,1,2,3,4,5]
console.log(arr)
arr.pop()
console.log("pop刪除最後一項:       " + arr)
arr.push("end")
console.log("push新增在最後一項:    " + arr)
console.log("slice切片(含頭部含尾): " + arr.slice(2,5))
```

### map

```javascript
// Solve 1
var dogs = ['No1','No2','No3','No4'];
var result = dogs.map(function(dog) {
    return dog  + " is good";
}) 
console.log(result)

// Solve 2
function map2(dogs) {
    result =[]
    for (var i=0 ;i < dogs.length; i++) {
        result.push(dogs[i] + " is good")
    }
    return result;
}
map2(dogs)
```

---

## 4. ES6 與變數管理

### var、let、const

* let 不會汙染環境
* var 會汙染環境 (如 if-else, IIFE 等)
* const、let 屬於 ES6
* const 宣告物件時，可以修改物件內容 (其他 type 無法修改)

### 擴展運算子 Spread Operator

```javascript
let arr1 = [1,2,3,4,5];
let arr2 = [6,7,8,9];
let obj1 = {a:1,b:2};
let obj2 = {a:0,c:3};
console.log(Math.min(...arr1));     // 1
console.log({...obj1, ...obj2});    // {a: 0, b: 2, c: 3}
```

### Arrow Function 箭頭函式

箭頭函式不會有作用域隔閡。

```javascript
const function1 = x => x+1;
console.log(function1(1));     // 2

function greet() {
    let replay = `Hi, ${this.preson}`;
    console.log(replay);
}
var obj = {preson: 'Eva'};
console.log(greet.call(obj))    // Hi, Eva

// 一般 function
function fun1() {
    console.log(`output 1: ${this.a}`);     
    setTimeout(function() {     
        console.log(`output 2: ${this.a}`)  // undefined
    } , 1000)
}

// Arrow function
function fun2() {
    console.log(`output 1: ${this.a}`);     
    setTimeout(() =>  {
        console.log(`output 2: ${this.a}`); 
    }, 1000)
}
```

---

## 5. 迭代與迴圈

### iterator

**iterable(可迭代) objects**：Array, String, TypedArray, Map, Set, NodeList

```javascript
var myString = "hello";
var iterator = myString[Symbol.iterator]();

console.log(iterator.next()); 
console.log(iterator.next()); 
console.log(iterator.next()); 
```

### for in & for of

* **for in**：迭代可列舉的屬性
* **for of**：迭代可迭代物件 (ES6)

```javascript
// for in
var object = {a:1, b:2, c:3};
for (var prop in object) {
    console.log(prop, object[prop]);
}

// for of
var myString = "hello"
for (let str of myString) {
    console.log(str);   // h e l l o
}
```

---

## 6. API與網頁物件模型整理

### 🔹 API
- **Application Programming Interface（應用程式介面）**  
- 一組規範或工具，讓不同程式或服務能彼此「溝通」與「交換資料」  
- 可理解為：**程式與網頁之間的溝通橋樑**  
- **Interface（介面）** = 規劃要提供哪些功能  

---

### 🔹 DOM（Document Object Model）
- 將 **HTML / XML 文件** 轉換成 **樹狀結構**  
- 文件中的每個標籤、屬性、文字都變成可被程式存取和修改的「節點」  
- 主要用途：讓 JavaScript 可以動態操作網頁內容  
- 👉 **DOM = 控制網頁內容**  

---

### 🔹 BOM（Browser Object Model）
- 瀏覽器提供的一組物件，用來操作 **瀏覽器本身** 的功能  
- 包含：
  - `navigator`（瀏覽器資訊）  
  - `location`（網址列）  
  - `history`（瀏覽紀錄）  
  - `screen`（螢幕資訊）  
- 👉 **BOM = 控制瀏覽器環境**  

---

### 🔹 window 物件
- 瀏覽器中的 **最上層物件**，所有東西都掛在它底下  
- 相當於瀏覽器的大容器，裡面包含：  
  - **DOM**：網頁文件（`window.document`）  
  - **BOM**：環境資訊（`window.location`、`window.history`、`window.navigator`）  
  - **工具方法**：如 `alert()`、`setTimeout()`、`setInterval()`  
- 常見屬性：  
  - `window.location` → 網址列  
  - `window.history` → 瀏覽紀錄  
  - `window.navigator` → 瀏覽器資訊  

---

### 📌 總結圖示
- **API** = 溝通規範  
- **DOM** = 操作「網頁內容」  
- **BOM** = 操作「瀏覽器環境」  
- **window** = 最大容器，包住 DOM、BOM 與工具方法

---
## 7. DOM 選擇器

### CSS選擇器 (ES5) 
- `document.querySelector("selector")`
👉 回傳第一個符合 CSS 選擇器的元素
```javascript
document.querySelector("#idName");     // 第一個符合 id 的元素
document.querySelector(".className");  // 第一個符合 class 的元素
document.querySelector("div > p");     // 符合 CSS 的巢狀條
```
</br>

- `document.querySelectorAll("selector")`
👉 回傳所有符合的元素，型態是 NodeList (可迭代)
```javascript
let items = document.querySelectorAll("li");
items.forEach(el => console.log(el.textContent));
```

### getElement(s)
- `document.getElementById("id")`
👉 回傳唯一一個元素（找不到則 null）

- `document.getElementsByClassName("className")`
👉 回傳所有符合 class 的元素（HTMLCollection，活的集合；DOM 變動會同步更新）

- `document.getElementsByTagName("tagName")`
👉 回傳所有符合標籤的元素，例如 "div"、"p"

- `document.getElementsByName("name")`
👉 依 HTML name 屬性搜尋，常見於 <input name="...">


| 特性  | `querySelector / querySelectorAll`                            | `getElement(s)By*`              |
| --- | ------------------------------------------------------------- | ------------------------------- |
| 語法  | 使用 **CSS 選擇器**                                                | 使用 **特定屬性 (id/class/tag/name)** |
| 回傳  | `querySelector` = 第一個元素<br>`querySelectorAll` = NodeList (靜態) | HTMLCollection (動態)，有些是單一元素     |
| 靈活性 | ✅ 可以選複雜選擇器（如 `div > p:first-child`）                           | ❌ 只能單一條件                        |
| 效能  | 差異極小，現代瀏覽器幾乎一樣                                                | 差不多                             |
| 推薦度 | **現代開發建議用 querySelector / All**                               | 舊專案或單純抓 id 時可用                  |
###### 已經確定要單一ID的話用getElement會比較快。

---

## 8. DOM監聽器

### 元素屬性 .onclick 
👉 缺點：同一個元素只能綁一次，後者會覆蓋前者。
```javascript
let btn = document.getElementById("myBtn");
btn.onclick = function() {
  console.log("按鈕被點擊了");
};
```

### addEventListener
👉 優點：
- 一個元素可以同時綁定多個事件處理器
- 可搭配 removeEventListener 移除事件
- 支援更多事件選項（例如冒泡 / 捕獲）
```javascript
let btn = document.querySelector("#myBtn");
btn.addEventListener("click", () => {
  console.log("Button clicked!");
});

```

### [常見事件](https://developer.mozilla.org/en-US/docs/Web/API/UI_Events#concepts_and_usage)
* **滑鼠事件**：click(按完後觸發), dblclick(雙擊), mousedown(按下及觸發), mouseenter, mouseleave, mousemove, contextmenu
* **鍵盤事件**：keydown, keyup, keypress
* **表單事件**：submit, input, change, focus, blur
* **視窗事件**：load, resize, scroll, beforeunload


### 事件物件 (Event Object)
```javascript
btn.addEventListener("click", function(event) {
  console.log(event.type);     // click
 console.log(event.target);   // 被點擊的元素
});
```

### [Event Flow 事件流](https://ithelp.ithome.com.tw/articles/10268458)
**Event Bubbling(冒泡)**：
事件觸發由內而外，`<li> -> <ul> -> <div> -> <body> -> <html> -> document`

**Event Capturing(捕捉)**：
事件觸發由外而內，`document -> <html> -> <body> -> <div> -> <ul> -> <li>`


`addEventListener` 和 `removeEventListener` 方法中，可以傳遞第三個參數(布林值)，調整要bubbling還是capturing(預設是bubbling)。
```javascript
element.addEventListener('click', eventHandler) // 未指定，預設為冒泡
element.addEventListener('click', eventHandler, false) // 冒泡
element.addEventListener('click', eventHandler, true) // 捕獲
```

DOM 標準（W3C Event Flow）把事件流分成三個階段：
1. **捕獲階段 (capturing phase)**：由上到下，找出目標。
2. **目標階段 (target phase)**：事件真正發生在目標元素。
3. **冒泡階段 (bubbling phase)**：由下往上，把事件往外傳遞。

### Event Flow 範例
如果同一個元素同時有 capturing 和 bubbling 事件，➡️ 先觸發 capturing，再觸發 bubbling。
1. 捕獲階段 → 由外而內
1. 到目標元素本身
1. 冒泡階段 → 由內而外
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Event Capturing vs Bubbling</title>
</head>
<body>
  <div id="outer" style="border:2px solid blue; padding:20px;">
    Outer Div
    <div id="parent" style="border:2px solid green; padding:20px; margin-top:10px;">
      Parent Div
      <button id="child" style="margin-top:10px;">Click Me</button>
    </div>
  </div>

  <script>
    // Outer 捕獲 / 冒泡
    document.getElementById("outer").addEventListener("click", () => {
      console.log("Outer Capturing");
    }, true);

    document.getElementById("outer").addEventListener("click", () => {
      console.log("Outer Bubbling");
    }, false);

    // Parent 捕獲 / 冒泡
    document.getElementById("parent").addEventListener("click", () => {
      console.log("Parent Capturing");
    }, true);

    document.getElementById("parent").addEventListener("click", () => {
      console.log("Parent Bubbling");
    }, false);

    // Child 捕獲 / 冒泡
    document.getElementById("child").addEventListener("click", () => {
      console.log("Child Capturing");
    }, true);

    document.getElementById("child").addEventListener("click", () => {
      console.log("Child Bubbling");
    }, false);

    // Child target event (目標元素本身)
    document.getElementById("child").addEventListener("click", () => {
      console.log("Child Target Event");
    });
  </script>
</body>
</html>

```
點擊 `button(child)` 輸出:
```
Outer Capturing
Parent Capturing
Child Capturing
Child Target Event
Child Bubbling
Parent Bubbling
Outer Bubbling
```

---

## 9. [Event](https://developer.mozilla.org/zh-TW/docs/Web/API/Event)
當 DOM 事件被觸發時，瀏覽器會自動建立一個 **事件物件 (Event Object)**，並傳遞到監聽函式裡。
它包含了這次事件的所有資訊，例如：事件型別、觸發的元素、滑鼠座標等等。

### Event 常用屬性

`event.type` → 事件型別 (例如 "click")
`event.currentTarget` → 目前正在處理事件的元素（跟 target 不一定相同，特別是冒泡/捕獲時）
`event.target` → 實際觸發事件的元素（永遠是最內層被點擊的）

```javascript
document.getElementById("outer").addEventListener("click", (event) => {
  console.log("target:", event.target);         // 被點擊的實際元素
  console.log("currentTarget:", event.currentTarget); // 綁定監聽的元素
});
```

### `event.target` 常見屬性 / 方法對照表

#### 🎯 基本屬性

| 屬性          | 說明                  | 範例                                     |
| ----------- | ------------------- | -------------------------------------- |
| `id`        | 元素的 id              | `event.target.id // "btn1"`            |
| `className` | 元素的 class（字串格式，舊用法） | `event.target.className // "red big"`  |
| `classList` | 回傳 class 清單，可操作     | `event.target.classList.add("active")` |
| `tagName`   | 標籤名稱（大寫）            | `event.target.tagName // "DIV"`        |
| `nodeName`  | 節點名稱（大寫，類似 tagName） | `event.target.nodeName // "DIV"`       |



#### 🎨 樣式相關

| 屬性 / 方法              | 說明         | 範例                                            |
| -------------------- | ---------- | --------------------------------------------- |
| `style`              | 修改行內樣式     | `event.target.style.backgroundColor = "blue"` |
| `getComputedStyle()` | 取得最終計算後的樣式 | `window.getComputedStyle(event.target).color` |



#### 📑 屬性操作

| 屬性 / 方法                        | 說明    | 範例                                            |
| ------------------------------ | ----- | --------------------------------------------- |
| `getAttribute("attr")`         | 取得屬性值 | `event.target.getAttribute("src")`            |
| `setAttribute("attr","value")` | 設定屬性  | `event.target.setAttribute("title", "Hello")` |
| `removeAttribute("attr")`      | 移除屬性  | `event.target.removeAttribute("disabled")`    |



#### 📦 資料存取

| 屬性            | 說明                  | 範例                                             |
| ------------- | ------------------- | ---------------------------------------------- |
| `innerText`   | 取得 / 設定文字內容（不含隱藏元素） | `event.target.innerText = "Hi"`                |
| `textContent` | 取得 / 設定文字內容（包含隱藏元素） | `event.target.textContent = "Hi"`              |
| `innerHTML`   | 取得 / 設定 HTML 結構     | `event.target.innerHTML = "<b>Hi</b>"`         |
| `dataset`     | 存取 `data-*` 屬性      | `event.target.dataset.id // 假如有 data-id="123"` |



#### 🔄 Class 操作（透過 `classList`）

| 方法                  | 說明           | 範例                                                     |
| ------------------- | ------------ | ------------------------------------------------------ |
| `.add("name")`      | 加入 class     | `event.target.classList.add("active")`                 |
| `.remove("name")`   | 移除 class     | `event.target.classList.remove("active")`              |
| `.toggle("name")`   | 切換 class     | `event.target.classList.toggle("hidden")`              |
| `.contains("name")` | 判斷是否有該 class | `event.target.classList.contains("box") // true/false` |

---

# SASS SCSS

## SCSS SASS 說明
[youtube簡介影片](https://www.youtube.com/watch?v=akDIJa0AP5c&t=2s)
[SASS SCSS語法說明文](https://ithelp.ithome.com.tw/m/articles/10244301) 
**SASS （Indented Sass**）：不寫 { } 、不寫;　不兼容CSS。
**👑SCSS （Sassy CSS）**：一樣要寫{ }、;　兼容CSS。
> SCSS 巢狀只是語法糖，效能取決於你怎麼寫選擇器。

### 1. 巢狀結構 (Nesting)
讓 CSS 的結構和 HTML 結構更接近，提升可讀性。  
適合用在「區塊內的元素關係清楚」的情境，例如一個 Banner 區塊中的 logo、nav。  
⚠️ 注意：不要巢狀太深（建議 2~3 層），否則會讓編譯後的選擇器過度複雜。

```scss
#banner {
  ...

  #logo {   // 等同於 #banner #logo
    ...

    img {   // 等同於 #banner #logo img
      ...
    }
  }

  nav {     // 等同於 #banner nav
    ...
  }
}

.box {
  background: {
    image: url(/img/bg.jpg);
    repeat: repeat;
    position: top;
  }
  font: {
    size: 1rem;     // 等同於 font-size:...
    weight: bold;   // 等同於 font-weight:...
  }
}

a {
  color: red; 
  &:hover {    // 等同於 a:hover
    color: red;
  }

  &.active {   // 等同於 a.active
    color: blue;
  }
}
````

**使用時機**：

* 當 HTML 結構明確、元素之間是「父子或狀態關係」時
* 例如：按鈕 hover 狀態、元件裡的子元素

---

### 2. 變數 (\$)

透過變數管理顏色、字體大小、間距等，可以一次調整，全站同步更新。
適合用在「專案配色、字體規範、間距標準化」。

```scss
$main-color: blue;
$sub-color: gray;

footer {
  background-color: $sub-color; 
  color: $main-color; 
}

p {
  color: $main-color; 
}
```

**使用時機**：

* 主題顏色、按鈕顏色、品牌色
* 字體、間距、邊框等共用樣式

---

### 3. Mixin

`@mixin` 用來定義一段可重用的樣式，並可傳參數。
`@include` 用來呼叫該 mixin。
適合用在「需要彈性變化的樣式」，例如 RWD 媒體查詢、按鈕樣式、陰影、漸層。

```scss
@mixin basic-space($mg, $pd) {
  padding: $mg;
  margin: $pd;
}

.wrap {
  @include basic-space(0, 1rem);
}

.box {
  @include basic-space(1rem, 0.5rem);
}
```

**使用時機**：

* 可重複但參數不同的情境（例如：不同按鈕大小）
* RWD breakpoint（一次定義，全站共用）
* 特效或陰影樣式

---

### 4. 繼承 (@extend)

透過 `%佔位選擇器` 定義一段樣式，使用 `@extend` 可讓多個類別共用。
適合用在「完全相同基底樣式」的情境。
⚠️ 注意：`@extend` 會合併選擇器，若濫用可能產生過長的選擇器鏈。

```scss
%basic-space {
  padding: 1rem;
  margin: 1rem;
}

.wrap {
  @extend %basic-space;
  background-color: red;
}

.box {
  @extend %basic-space;
  font-size: 1rem;
}

.footer {
  @extend %basic-space;
}
```

**使用時機**：

* 元件共用基底樣式（如 `.btn`、`.card`）
* 多個區塊有相同 padding/margin 時
* 適合「樣式完全相同」的情況，否則建議改用 `@mixin`（因為更彈性）


### 總結

* **巢狀結構**：提升結構清晰度，但不要過深。
* **變數**：集中管理專案樣式，方便修改主題。
* **Mixin**：適合可重複使用又需要彈性的樣式（RWD、按鈕、特效）。
* **Extend**：適合共用完全相同的基底樣式，但要避免過度耦合。


---

## SCSS環境設置
[環境設置文章(簡略)](https://medium.com/ivycodefive/3-scss%E7%9A%84%E7%92%B0%E5%A2%83%E5%BB%BA%E7%AB%8B%E8%88%87%E5%AF%A6%E4%BD%9C%E6%B8%AC%E8%A9%A6-live-sass-compiler-6a2a94e76a0f) 作者下一篇有 檔案架構 說明可以看
[youtube  VScode設定說明](https://www.youtube.com/watch?v=mzuKtTuimEE&t=2900s) - 編譯格式說明


### 方法一 ： 控制台指令流程（不依賴 VS Code 套件）

**安裝環境**
1. 安裝 [Node.js LTS](https://nodejs.org/)  
2. 安裝 Sass
```bash
npm install -g sass
```
3. （選用）安裝 PostCSS + Autoprefixer
```bash
npm install -g postcss postcss-cli autoprefixer
```

**常用指令**
```bash
# 開發模式 (expanded, 有 Source Map)
sass --watch scss:style --style expanded --source-map

# 上線模式 (compressed, 無 Source Map)
sass scss/style.scss dist/style/style.min.css --style compressed --no-source-map

# 加上 Autoprefix (需搭配 PostCSS)
postcss dist/style/*.css --use autoprefixer -d dist/style/
```
4. 在 `package.json` 加入:
```jsonld
"scripts": {
  "dev": "sass --watch scss:style --style expanded --source-map",
  "build": "sass scss:dist/style --style compressed --no-source-map",
  "prefix": "postcss dist/style/*.css --use autoprefixer -d dist/style/"
}
```
用法：
```
npm run dev     # 開發模式
npm run build   # 上線模式
npm run prefix  # 自動加前綴
```

---

### 方法二 ： VS Code Live Sass Compiler 套件流程
1. 安裝套件 **Live Sass Compiler**
2. 建立/編輯 `.vscode/settings.json`
```jsonld
{
    "liveSassCompile.settings.formats": [
    {
        "format": "expanded",
        "extensionName": ".css",
        "savePath": "/style"
    },
    {
        "extensionName": ".min.css",
        "format": "compressed",
        "savePath": "/dist/style"
    }
    ],
    "liveSassCompile.settings.generateMap": false,
    "liveSassCompile.settings.autoprefix": [
        "> 1%",
        "last 2 versions"
    ],
}
```

**編譯流程**
1. 在 VS Code 打開 .scss 檔
1. 點擊右下角的 Watch Sass
1. 套件會自動：
* 產生一份 expanded CSS → 存到 /style
* 產生一份 compressed CSS（.min.css）→ 存到 /dist/style
* 自動排除 node_modules、.vscode
* 產生 Source Map（方便 DevTools 對應 SCSS 原始碼）
* 自動加前綴（符合 >1% 或最近兩版的瀏覽器）


**建議的專案資料夾結構**
```python
project/
├── index.html
├── scss/              # SCSS 原始檔
│   ├── style.scss     # 主檔，會 import 其他檔
│   ├── _variables.scss
│   ├── _mixin.scss
│   ├── _layout.scss
│   └── _components.scss
├── style/             # 編譯後的 expanded CSS (開發用)
│   └── style.css
├── dist/              # 上線用 (壓縮過的 CSS)
│   └── style.min.css
└── package.json       # (方法一需要)

```



#### 編譯格式說明
- **expanded**：手打（未壓縮，適合開發時閱讀）
- **compressed**：壓縮成一行（適合上線用）
- **excludeList**：排除不需要編譯的資料夾（如 node_modules, .vscode）
- **generateMap**：產生 Source Map，讓瀏覽器 DevTools 能對應回原始 SCSS
- **autoprefix**：自動加上瀏覽器前綴，條件：
  - 市佔率 > 1%
  - 最近兩個版本
  - 只要符合其中一個條件就會套用

#### VS Code Live Sass 設定範例
```json
"liveSassCompile.settings.formats": [
  {
    "format": "expanded",
    "extensionName": ".css",
    "savePath": "/style"
  },
  {
    "extensionName": ".min.css",
    "format": "compressed",
    "savePath": "/dist/style"
  }
],
"liveSassCompile.settings.excludeList": [
  "**/node_modules/**",
  ".vscode/**"
],
"liveSassCompile.settings.generateMap": true,
"liveSassCompile.settings.autoprefix": [
  "> 1%",
  "last 2 versions"
]
```

#### 建立各sass檔案
```bash
ni style.scss, _variables.scss, _mixin.scss, _layout.scss, _components.scss
```

---

2025/9/20 ~ 21
## 前端程式編譯流程總覽 (Webpack、PostCSS、Babel、SCSS)
[參考資料](https://yixuntseng-bruce.medium.com/%E4%BA%94%E5%88%86%E9%90%98%E5%AD%B8%E5%89%8D%E7%AB%AF-webpack-postcss-babel-sass%E5%88%B0%E5%BA%95%E6%98%AF%E4%BB%80%E9%BA%BC-21820404fdd3)
⭐ 重點：瀏覽器只懂 HTML / CSS / JavaScript  
所有框架、套件、工具最終都要轉換成這三種語言才能執行。

* **Webpack**：把 HTML、JS、CSS、圖片等模組「打包」成瀏覽器可載入的資源。
但需要其他工具(PostCSS、Babel)協助。
* **PostCSS**：PostCSS 解決的是「讓 CSS 更適合上線、相容更多瀏覽器」。
    * Autoprefixer → 自動加上 -webkit-、-ms-
    * cssnano → 壓縮 CSS
* **Babel**：JavaScript 編譯器/轉譯器 (Transpiler)。解決的是「JS 新語法與舊環境相容問題」
* **SCSS**：CSS 預處理器 (Preprocessor)。解決的是「寫 CSS 的開發體驗」。

---

#### 1. HTML 流程
| 階段             | 工具 / 技術                 | 輸出 |
|------------------|-----------------------------|------|
| Preprocessor     | Pug, Haml, Markdown, JSX(含 HTML 部分) | HTML |
| Template Engine  | EJS, Handlebars, Vue/React Template | HTML |
| 瀏覽器最終讀取   | -                           | HTML |

---

#### 2. CSS 流程
| 階段             | 工具 / 技術                 | 輸出 |
|------------------|-----------------------------|------|
| Preprocessor     | Sass/SCSS, Less, Stylus     | CSS |
| Postprocessor    | PostCSS (Autoprefixer, cssnano) | 優化後 CSS |
| 瀏覽器最終讀取   | -                           | CSS |

---

#### 3. JavaScript 流程
| 階段             | 工具 / 技術                 | 輸出 |
|------------------|-----------------------------|------|
| Preprocessor     | TypeScript, CoffeeScript    | JavaScript |
| Transpiler       | Babel (ES6+ → ES5)          | JavaScript |
| Bundler          | Webpack, Vite, Rollup, Parcel | 打包後 JS |
| 瀏覽器最終讀取   | -                           | JavaScript |


---

## [CSS 的模組化方法](https://www.cythilya.tw/2018/06/05/css-methodologies/)
### CSS 命名規則 / 架構思維 - OOCSS、SMACSS、BEM
* **OOCSS（Object-Oriented CSS）**
觀念：把樣式抽成「物件」，盡量重用，避免寫重複的 CSS。
* **SMACSS（Scalable and Modular Architecture for CSS）**
觀念：把 CSS 拆成 Base / Layout / Module / State / Theme。
* **BEM（Block Element Modifier）**
觀念：用明確的命名規則來管理 CSS（e.g. card__title--active）。

#### [BEM (Block Element Modifier)](https://w3c.hexschool.com/blog/35afa83f)
**B - Block (區塊)**
- 頁面獨立可重複使用的組件
- 不使用元素選擇器和 ID 選擇器
- 範例：`.header`、`.menu`、`.container`

**E - Element (元素)**
- 屬於 Block 的子部分，命名使用 `__`
- Element 無法脫離 Block 獨立存在
- 範例：`.menu__item`、`.header__title`

**M - Modifier (修飾符)**
- 用來描述狀態或屬性，命名使用 `--`
- 同一個 Block 或 Element 可以有多組 Modifier
- 範例：`.menu__item--active`、`.menu__item--danger`

### CSS 模組化 - CSS Modules、CSS-in-JS
* **CSS Modules**
特點：每個檔案的 class 名稱自動本地化，不會互相污染。
👉 適合 React/Vue 專案。
* **CSS in JS（如 styled-components, Emotion）**
特點：把 CSS 寫在 JS 裡，支援動態樣式。
👉 在 React 生態系超常見，Vue 較少。

---







# 其他觀念
### [PWA漸進式網頁](https://ithelp.ithome.com.tw/m/articles/10241311)
介於 App 與 Web 之間，各取兩邊的優勢而產生出的新形態，讓使用者在瀏覽網頁的時候地體驗感受像是手機)

---
               
### Wireframe 
- 盡量不要用色彩
- 不要在沒用的地方吹毛求疵

![image](https://hackmd.io/_uploads/rkOCxnmqgx.png)

我的理解:wireframe主要用於溝通，沒有特定形式，可避免設計不通過導致實作後不被採用、浪費時間。 # 獨自作業時，設計稿有7/80%即可

---

### 全端設計UI流程(較簡化)
1. 定好
- 字體
- 主色、輔色
- Components(card、heading、nav bar、footer)

2.組裝
- gride

#獨自作業可能不用做prototype
![image](https://hackmd.io/_uploads/SkuuM2Qceg.png)

---
### DevOps
[9min說明影片](https://www.youtube.com/watch?v=GcMqHnSDyc4)


---

## 🧩 Unit Tests × TDD × DDD × SOLID — 教學筆記

---

### 一、Unit Tests（單元測試）

#### 💡 定義
針對 **程式中最小可測試單位（函式、方法、類別）** 進行自動化測試，  
確保每個邏輯單元都能正常運作。

#### 🎯 目的
- 及早發現錯誤（早期防呆）  
- 重構（Refactor）後仍能確保功能正確  
- 作為「可執行的程式文件」

#### ⚙️ 關鍵重點
- 一次只測一件事（Single Concern）  
- 不連資料庫、不呼叫外部 API  
- 執行快、覆蓋率高、結果穩定  

#### 🧱 Mock 與測試隔離
> 為了讓測試更獨立，常用「Mock 物件」來模擬外部依賴（例如 Repository 或 API）。

---

### 二、TDD（Test-Driven Development，測試驅動開發）

#### 💡 定義
> 「先寫測試、再寫程式」的開發流程。  
由測試驅動開發方向，確保設計自然形成乾淨結構（Clean Code）。

#### 🔁 核心循環：Red → Green → Refactor
1️⃣ **Red**：先寫測試，因尚未實作 → 測試失敗。  
2️⃣ **Green**：撰寫最少程式碼 → 測試通過。  
3️⃣ **Refactor**：重構程式碼 → 維持測試全通過。

#### ⚙️ 優點
- 開發有明確目標（寫程式是為了通過測試）  
- 降低「最後才測」的風險  
- 幫助撰寫可測試、職責單一的程式  

#### 🔗 與 DDD 的關聯
- **TDD**：驅動程式邏輯的開發節奏。  
- **DDD**：驅動系統架構的設計方向。  
> TDD 寫測試，DDD 決定程式在哪一層實作。

---

### 三、DDD（Domain-Driven Design，領域驅動設計）

#### 💡 定義
> 一種以「業務邏輯」為核心的架構思維。  
讓軟體結構反映現實業務，降低技術與商業之間的落差。

#### 🏢 核心概念
| 名稱 | 說明 |
|------|------|
| **Domain（領域）** | 系統所在的業務範圍，如電商、銀行、醫療 |
| **Entity（實體）** | 具有唯一識別的物件（如客戶、訂單） |
| **Value Object（值物件）** | 無獨立身份，只由值組成（如地址、金額） |
| **Aggregate（聚合）** | 一組相關實體與值物件的集合 |
| **Repository（儲存庫）** | 定義資料存取介面（CRUD 操作） |
| **Service（服務）** | 跨領域或不屬於單一實體的行為 |

>💡 我的理解: 
DDD比較像是設計概念，使用 **Repository** (定義資料的存取介面（CRUD 操作）) 隔離 **Domain** (定義系統的核心概念) 與 **Infrastructure**(基礎設施層) ，讓後續實作人員不必知道資料庫的內容，也可以依據Repository定義的function去操控/使用資料。

</br>

#### 3.1 Domain（領域層）
只關心業務邏輯(定義/宣告)，不處理技術細節(實作)。

```csharp
public class Order {
    public Guid Id { get; private set; }
    public decimal Total { get; private set; }
    public bool IsPaid { get; private set; }

    public void AddItem(Product product, int qty) {
        Total += product.Price * qty;
    }

    public void Pay() {
        if (IsPaid) throw new InvalidOperationException("已付款不能重複付款");
        IsPaid = true;
    }
}
````
</br>

#### 3.2 Application（應用層）

組合多個 Domain 行為形成業務流程。
不關心技術、資料庫，只呼叫 Domain 與 Repository。

```csharp
public class OrderService {
    private readonly IOrderRepository _repo;

    public OrderService(IOrderRepository repo) {
        _repo = repo;   // 依賴抽象介面，而非具體實作
    }

    public void CreateOrder(Product product, int qty) {
        var order = new Order();
        order.AddItem(product, qty);
        _repo.Save(order);   // 呼叫 Repository（抽象介面）
    }
}
```
</br>

#### 3.3 Infrastructure（基礎設施層）

處理技術細節（DB、API、Mail、File...）。
實作 Domain 定義的抽象介面。

```csharp
public class SqlOrderRepository : IOrderRepository {
    private readonly DbContext _db;

    public SqlOrderRepository(DbContext db) {
        _db = db;
    }

    public void Save(Order order) {
        _db.Orders.Add(order);
        _db.SaveChanges();
    }

    public Order GetById(Guid id) {
        return _db.Orders.First(o => o.Id == id);
    }
}
```

</br>

#### 🔁 3.4 反向依賴（Dependency Inversion）

**📘 定義**

> 一般依賴是「上層依賴下層」，
> **反向依賴**是「高層與低層都依賴抽象介面」。

**🔄 結構圖**

```
（反轉前）
Application → SqlRepository → Database

（反轉後）
        ↑
Infrastructure（實作 IRepo）  
        │
Application（依賴 IRepo 介面）  
        │
Domain（定義介面 IRepo）
```

#### ✅ 優點

| 好處        | 說明                                  |
| --------- | ----------------------------------- |
| **可測試性高** | 可用「假 Repository（Mock）」代替資料庫         |
| **可維護性高** | 換技術只改 Infrastructure，不動 Application |
| **可擴充性高** | 支援 SQL、NoSQL、記憶體快取等多版本              |
| **低耦合**   | 各層透過介面連接，不互相干擾                      |

> 💬 反向依賴（DIP）是 SOLID 的 D 原則，也是 DDD 的實作基礎。

---

### 四、SOLID 原則

#### 💡 定義

> SOLID 是 5 條物件導向設計原則的縮寫，
> 目標：讓程式 **可維護、可擴充、可測試**。
> 同時是 DDD 架構能成功落地的基礎。

| 縮寫    | 原則名稱                  | 中文說明   | 精神           |
| ----- | --------------------- | ------ | ------------ |
| **S** | Single Responsibility | 單一職責原則 | 一件事一個類。      |
| **O** | Open/Closed           | 開放封閉原則 | 不改舊程式就能加新功能。 |
| **L** | Liskov Substitution   | 里氏替換原則 | 子類別要能替代父類別。  |
| **I** | Interface Segregation | 介面隔離原則 | 介面不要太胖。      |
| **D** | Dependency Inversion  | 依賴反轉原則 | 依賴抽象，不依賴具體。  |

> 💬 在 DDD 中，D 原則透過 Repository 與介面設計被明確實現。

---

### 五、綜合理解與應用

#### 🔗 三者關係總覽

| 層面        | 角色   | 關注重點         |
| --------- | ---- | ------------ |
| **DDD**   | 架構設計 | 如何劃分邏輯層、定義責任 |
| **TDD**   | 開發流程 | 如何以測試驅動程式撰寫  |
| **SOLID** | 設計原則 | 如何讓程式易於維護與測試 |

#### 🧭 架構依賴方向總圖

```
[ Presentation 層 ] (Controller / API)
          │
          ▼
[ Application 層 ]  → 組織業務流程，呼叫 Domain
          │
          ▼
[ Domain 層 ]        → 定義業務邏輯與抽象介面
          ▲
          │
[ Infrastructure 層 ]→ 實作抽象介面 (DB, File, API)
```

**🔄 資料流向**
1️⃣ 使用者 → Presentation（送出請求）
2️⃣ Presentation → Application（呼叫用例服務）
3️⃣ Application → Domain（執行業務邏輯）
4️⃣ Domain → Repository（要求資料存取）
5️⃣ Repository → Infrastructure（實際操作資料庫）
6️⃣ Infrastructure → 回傳結果給上層

#### 💬 實務開發建議

* 用 **TDD** 驅動開發（保證邏輯正確）。
* 用 **DDD** 設計分層（保持架構清晰）。
* 用 **SOLID** 指導程式結構（提高維護性）。

> ✅ 最佳實踐：
> DDD 是房子的藍圖，
> TDD 是施工流程，
> SOLID 是施工的工法規範。

---

# React
## 建立React專案 (Vite)
```
npm create vite@latest
(專案名稱)
(選框架)
(JacaScript)

cd 檔案位置
npm install
npm run dev
```

## 概念說明


### 1. Component（組件）

React 的畫面是由「組件」所組成。組件有兩種主要寫法：

**(1) Class Component（類別式組件）**

較舊的寫法，需要 `class`、`extends React.Component`，並且必須實作 `render()`。

**(2) Function Component（函式式組件）**

最推薦的寫法，用一個普通的 JavaScript 函式，並 **return JSX**。

例如：

```jsx
function MyComponent() {
  return <div>Hello</div>;
}
```

---

### 2. JSX 概念

JSX 是 React 使用的 UI 描述語法，看起來像 HTML，但實際上是 JavaScript 語法糖。
在使用 Vite、Babel 等工具時，JSX 會被轉譯成純 JavaScript，讓瀏覽器可以執行。

---

### 3. Component 的回傳限制

在 React 中，**每個 Component 只能回傳一個根元素（root element）**。
（這是因為 return 只能返回一個值，不是由 HTML 限制）

常見的解法有兩種：

**(1) 使用 `<div>` 包起來**

```jsx
return (
  <div>
    <h1>Hello</h1>
    <p>World</p>
  </div>
);
```

**(2) 使用 Fragment**

不會產生額外的 DOM 結構。

寫法：

```jsx
return (
  <>
    <h1>Hello</h1>
    <p>World</p>
  </>
);
```

---

### 4. JSX 語法細節

**(1) 空元素需要加 `/`**

例如 `<img />`、`<input />`

```jsx
<img src="a.png" />
```

**(2) `class` 要寫成 `className`**

因為 `class` 是 JavaScript 的保留字。

```jsx
<div className="box"></div>
```

**(3) `for` 要寫成 `htmlFor`**

同樣避免和 JavaScript 的 `for` 衝突。

```jsx
<label htmlFor="account">帳號</label>
```

**(4) inline style 使用 JavaScript 物件 `{ { } }`**

外層 `{}` 表示要執行 JavaScript
內層 `{}` 才是 style 物件

```jsx
<div style={{ color: "red", fontSize: "20px" }}>
  Hello
</div>
```

**(5) 使用 `{}` 在 JSX 中插入 JavaScript**

在 Props 或內容中插入動態變數時使用花括號。

```jsx
const name = "Eva";

return <h1>Hello {name}</h1>
```

---


## 回掉函數（Callback Function）

在 React 中，事件處理常使用「回掉函數」。回掉函數指的是當某個事件發生時，瀏覽器再「回頭呼叫」你提供的函數。

例如：按鈕被按下 → 觸發 `onClick` → React 呼叫你提供的函數。

### 寫法 1（直接在 JSX 裡寫匿名函數）

```jsx
function MyComponent() {
  return <h1>你好</h1>
}

function App() {
  return (
      <> 
        <button onClick={function(){alert('hello')}}>我是按鈕</button>
        <MyComponent />
      </>
  )
}

export default App
```

**說明：**

* 使用匿名函數 `function(){...}` 直接放進 `onClick`
* 這種寫法能正常工作，但每次 render 會重新產生一個新的函數
* 在複雜專案中可讀性較差

---

### 寫法 2（先宣告函數，再把引用傳給 JSX）

```jsx
function MyComponent() {
  return <h1>你好</h1>
}

function App() {
  const handleClick= () => {
    alert('hello')
  }

  return (
      <> 
        <button onClick={handleClick}>我是按鈕</button>
        <MyComponent />
      </>
  )
}

export default App
```

**說明：**

* 更常用、可讀性高
* `onClick={handleClick}` 表示「把函數本身傳給 React」，不是立即執行
* React 會在事件發生時替你呼叫它

---

## JSX 中的陣列處理

JSX 允許使用 JavaScript 表達式，因此可以直接用 `.map()` 渲染一組資料。

```jsx
function App() {
  const listItems = [
    {content:'Eva', id: '1'},
    {content:'Kitty', id: '2'},
    {content:'Miky', id: '3'}
  ]
  const filterItems = listItems.filter((item) => {
    if (item.content !== 'Eva') {
      return true   //如果content不是Eva就回傳（Kitty, Miky）
    }
  })
  return (
      <> 
        {filterItems.map((item) => {
          return <div key={item.id}>{item.content}</div>  //key可避免網頁報警告
        })}
      </>
  )
}

export default App
```

**補充說明：**

* `.filter()` 用來過濾資料
* `.map()` 用來把資料轉成 JSX
* `key` 是 React 要求的唯一識別碼，用來提升列表渲染效能、避免警告

---

## props（屬性）


## props 傳遞的進階寫法（含 callback）

Props 不只有傳「資料」，也可以傳「函數」。
這讓父組件能控制子組件的行為，稱為 **Callback props**。

### 1. 父傳子（一般 props）

```jsx
function Child(props) {
  return <h1>哈囉 {props.name}</h1>
}

function App() {
  return <Child name="Eva" />
}
```

### 2. 父傳子：傳 callback 函數

子組件可以呼叫父組件傳來的函數。

```jsx
function Child({ onAlert }) {
  return (
    <button onClick={onAlert}>點我通知父組件</button>
  );
}

function App() {
  const handleChildAlert = () => {
    alert("子組件呼叫了父組件的函數！");
  };

  return <Child onAlert={handleChildAlert} />;
}

export default App;
```

**重點：**

* 父組件透過 props 傳入 callback
* 子組件在事件中呼叫這個 callback
* 適用於「子要把事件告知父」的情境，例如：表單送出、按鈕點擊
---

## state（狀態）

State 是 React 組件自己的「可變資料」。
當某個 state 改變時，React 會重新 render 該組件。

**State 特性：**

* 每個組件的 state 彼此獨立
* state 的值可以透過 props 傳給子組件
* 必須使用 `useState()` 來管理，不可直接修改

### 範例（不修改原程式碼）

```jsx
import { useState } from "react";

  function MyComponent() {
    const [clicks, setClicks] = useState(0);    //[state內容, 用來更改state內容的函數]    useState(預設值)
    const handleClick = () => {
      setClicks(clicks+1)
      console.log(clicks);
      
    }
    return (
      <> 
        <h1>ouo</h1>
        <button onClick={handleClick}>點擊次數: {clicks}</button>
      </>
    );
  }

  function App() {
    return (
      <>
        <MyComponent />
      </>
    )
    
  }

  export default App
```

**補充說明：**

* `useState(0)` → 初始值為 0
* `clicks` 是目前的 state
* `setClicks()` 是唯一能用來修改 state 的函數
* 呼叫 `setClicks()` 會觸發重新渲染（re-render）

---

## two ways binding 雙向綁定
當UI發生改變時state也會發生改變
```jsx
import { useState } from "react";

function CreateForm() {

  const [content, setContent] = useState('');

  return (
    <form className="create-form">
      <input type="text" placeholder="輸入待辦事項"
        value={content}
        onChange={(e) => {setContent(e.target.value)}}/>
      <button type="submit">加入</button>
    </form>
  );
}

export default CreateForm
```

---

## 箭頭函數
箭頭函數不會產生自己的 this；一般函數會。
React 中 90% 情況用箭頭函數，是因為它能避免 this 的混亂。

一般函數常受到 this 綁定干擾：
```jsx
class App {
  constructor() {
    this.addTodo = this.addTodo.bind(this);
  }
  addTodo() { ... }
}
```

箭頭函數不會：
```jsx
addTodo = () => { ... }  // 自動綁定外層 this
```

| 特色                | 一般函數 function  | 箭頭函數 =>      |
| ----------------- | -------------- | ------------ |
| this              | ✔ 動態（由呼叫者決定）   | ❌ 固定為外層（不會變） |
| arguments         | ✔ 有            | ❌ 沒有         |
| 能不能 new           | ✔ 可以           | ❌ 不行         |
| prototype         | ✔ 有            | ❌ 沒有         |
| 適合用作 constructor  | ✔              | ❌            |
| React 事件/callback | 可以，但容易 this 混亂 | ✔ 最常用        |
| 簡潔程度              | 較冗長            | ✔ 最簡潔        |

---
## React icon
[React icons 網站](https://react-icons.github.io/react-icons/)
```
npm install react-icons
```
- 組件可以使用html元素，不會被當成props，因為icons組件會將html元素再傳給html
```
// 第一層{}表示要寫html， 第二層表示物件
<MdDelete style={{cursor: 'pointer'}}/>
```


