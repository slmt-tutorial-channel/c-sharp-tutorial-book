# 第 8 課 - string 簡介

## <span class="section_abstract">本課介紹</span>

此課在簡介 string (字串) 是甚麼，以及 string 之間的串接方式。

## <span class="section_video">教學影片</span>

<iframe width="560" height="315" src="https://www.youtube.com/embed/Ru7j2X3WH-4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## <span class="section_highlights">重點提示</span>

1. `string` 型別指的是由一連串文字所組成的資料，中文叫做「字串」。
2. `string` 與之前提到的 `int`、`float` 這些型別不同，記憶體空間並不是固定的，而是會隨著存放的文字量變化。
3. 兩個 `string` 的變數可以透過 `+` (加法符號)，將連個字串連接在一起。
    - 例如：以下例子之中，`str3` 最後會得到 `我是小山 哈哈 ` 這個結果。
        ```c#
        string str1 = "我是小山 ";
        string str2 = " 哈哈 ";
        string str3 = str1 + str2;
        ```
4. `+` 不但可以把兩個字串相接，也可以讓字串與非字串的變數相接起來。
    - 例如：以下例子之中，`str2` 最後會得到 `我是小山 54321` 這個結果。
        ```c#
        string str1 = "我是小山 ";
        int number = 54321;
        string str2 = str1 + number;
        ```
5. 字串的串接如同一般型別使用 `+` 的運算，也支援 `+=` 的寫法。
    - 例如：以下例子之中，`str1` 最後會得到 `我是小山 哈哈 ` 這個結果。
        ```c#
        string str1 = "我是小山 ";
        string str2 = " 哈哈 ";
        str1 += str2;
        ```

## <span class="section_supplementary">補充</span>

### 字串與非字串相接背後的魔法

本課中提到了字串在與非字串相加的時候，會自動將後者轉換成字串，然後再串接起來。那麼這是基於甚麼樣的原理做到的呢？

事實上，這利用到了 C# 之中的一個重要的設計，`Object` 型別的存在。

`Object` 型別是 C# 之中所有類別的基底類別 (類別與基底類別的概念後面課程會介紹)，其中它規定每一個 C# 中的型別必須要有 `ToString` 這個方法。這個方法簡單來說就是要求每一個型別的值或物件，都「必須要可以轉換成字串」。因此我們可以預期所有 C# 中的變數都會有這個方法可以呼叫。這也是為什麼在字串串接時，後者可以不一定要是字串。因為後者就算不是字串，也一定會有 `ToString` 可以把它轉換成字串。

至於實際上 `ToString` 是怎麼做到這件事情的，這個就利用到了物件導向的多型性的特性 (也是後面課程會介紹)。多型性讓每一個型別可以自行決定 `ToString` 該怎麼實作，因此不同的型別可以實作自己的 `ToString`，以確保自己的型別在轉換成字串時可以用自己想要的方法呈現。

因此當未來大家學會了類別以及 `override` 之後，就可以實作自己類別的 `ToString`，確保自己的資料被字串串接時按照自己喜歡的樣子呈現。

## <span class="section_references">相關資訊連結</span>

### C# 官方文件 - `string` 型別的介紹

<https://learn.microsoft.com/zh-tw/dotnet/api/system.string?view=net-7.0>
