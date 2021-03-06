# 第 5 課 - 變數

## <span class="section_abstract">本課介紹</span>

這課主要是在介紹「變數」
包括如何宣告變數、指定數值、以及將值顯示出來等等

## <span class="section_video">教學影片</span>

<iframe width="560" height="315" src="https://www.youtube.com/embed/lAO0YRPONkU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## <span class="section_highlights">重點提示</span>

1. 「變數」主要是在扮演「儲存資料」的腳色
2. 所有的變數在使用之前，都必須先宣告過一遍
   - 目的在於讓電腦先知道變數的「型別」是甚麼
1. 想要宣告多個變數，只需要在變數中間用「,」區隔即可
2. 「`int`」代表「整數(Integer)」，例如：-2、10、800000、-9999
3. 「`=`」不是「相等」，而是「指定」
4. 在使用變數之前，務必先存入某個數值。如果沒有這樣做，電腦不會讓你編譯它
5. 如果怕自己忘記設定數值，可以在宣告的時候順便指定數值，像是...
    ```c#
    int number = 10;
    ```
8. 一般來說，變數的值是可以一直修改的

## <span class="section_supplementary">補充</span>

### 變數的名稱限制

C# 對於變數的命名有一套限制規則，並不是所有的名稱都可用來當作變數名稱使用。最基本的限制就是，變數不可以使用「關鍵字(Keyword)」作為名稱。那甚麼是關鍵字呢？就是 C# 裡面與程式結構有關的字眼，例如：class、using、namespace.... 基本上就是那些你在 IDE 中看起來有顏色的字。

那另外，其他限制還包括，在同一個 Scope(下面有解釋) 內，不可以使用一樣的變數名稱。變數的第一個字必須是英文、底線等等。詳細可以看看「相關資訊連結」的文章。

那還有一個問題是，可不可以用中文字當作變數名稱呢？可以，但是我強烈建議不要這樣做。主要是因為中文字與一般文字的儲存方式不同，也許會發生不可預期的錯誤。

### Scope

變數並不是永久長存的，也不會一直在程式裡面儲存著。每個變數都有它作用的限制範圍，或者也可以說是變數的生存期限。而這個範圍，就稱作「Scope」。今天你在某個地方宣告了變數，但是只要超出了變數的 scope，就無法使用它了。

那要怎麼判別變數的 scope 呢？ 很簡單，只要看「大括號 { }」的包起來的區塊就行了。基本上，變數只在大括號包起來的範圍內才有效。而在大括號外面使用變數就會無法呼叫到它。目前只需要知道這樣就好了。

這 個 scope 還提供了一個好處。變數名稱是不可以重複的，不過它有個例外存在。 就是如果你在一個變數的 scope 外宣告了一樣名稱的變數，那就不會互相影響。例如，你在 void button1_Click() 裡面宣告了 num，跟在 void button2_Click() 裡面宣告了 num，這樣就不會互相衝突。

### 型別 Type

變數在使用之前必須要先宣告型別。這個作用是在於讓電腦知道，它要配給這個變數多少記憶體空間。另外也是要在後面進行一些使用上的判斷，通常可以預防不少語法上的錯誤。

變數的型別有很多種，詳細的種類後面會慢慢介紹。

### 指定

這課提到「=」代表「指定」，而不是「相等」。真正的「相等」是使用「==」這個符號。這個區分非常重要，因為這是程式設計師常犯的錯誤。在這裡，「指定」代表的意思其實就是把「右邊的值存入左邊的變數」裡的意思。只要這樣記就比較不會出錯。

### 個人對於變數的命名習慣

我個人對於變數命名有個習慣。如果我的變數名稱是由多個單字拼成的，那我第一個單字的第一個字母會小寫，後面單字的第一個字母會大寫。這不是硬性規定的，但有一部分的趨勢是這樣的。

Ex: 假設某個變數是由「form、background、color」組合而成

```c#
formBackgroundColor
```

## <span class="section_practice">練習</span>

1. 試著在 button1_Click 裡面宣告兩個「名稱相同」的變數，可以發現甚麼問題？
2. 那如果我分別在 button1_Click 跟 Form1 這兩個 method 中宣告一樣的變數呢？
3. 那或者我在 button1_Click 裡面跟外面(注意不是在 Form1 的 method 中)，宣告名稱一樣的變數呢？

上面這三種情況，為什麼有時候變數可以名稱相同，有時候不行？  
(參考補充的 Scope)

參考解答：<https://github.com/slmt-tutorial-channel/c-sharp-solutions/blob/master/class_1_10/class5.md>

## <span class="section_references">相關資訊連結</span>

### 變數的內建型別列表

<http://msdn.microsoft.com/zh-tw/library/cs7y5x0x%28v=vs.90%29.aspx>
