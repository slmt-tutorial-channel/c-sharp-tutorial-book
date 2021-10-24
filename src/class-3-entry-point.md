# 第 3 課 - 程式結構與進入點

## <span class="section_abstract">本課介紹</span>

這課主要介紹上一課所寫的 HelloWorld 程式碼架構  
以及 C# 的 Entry Point(程式進入點)

## <span class="section_video">教學影片</span>

<iframe width="560" height="315" src="https://www.youtube.com/embed/B9YGbcXuGck" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## <span class="section_highlights">重點提示</span>

1. 我們可以大致將 C# 程式碼分成兩塊，一塊是含有 `using` 的區塊，一塊是程式碼的主要部分
   - `using` 部分主要是在呼叫內建的程式庫
   - 主要區塊就是我們編寫程式邏輯的地方
2. C# 裡面，用大括號包起來的程式碼算是一個「區塊」。這個區塊屬於括號上面的程式碼所有。
3. Hello World 的這個程式由裡到外分成三層，namespace、class、method
4. namespace 可以想成是自己的程式庫，所以在 namespace 內寫程式碼就是在編寫自己的程式庫
5. class 一般負責 namespace 裡面一部分的工作
6. method 是在 class 下，負責更細部事務的東西。它有一個明顯的特徵，通常 method 後面都會跟著一個小括號，像是：`void Example(int num)`
7. `static void main(string[] args)` 是特別的 method，所有的 C# 程式都會從這個 method 開始執行。 一般稱之為「進入點(Entry Point)」
8. `Console.WriteLine` 跟 `Console.ReadKey` 也都是 method。前者會在黑色視窗上顯示文字，後者會等待使用者輸入任意字元
9. 每一行程式碼都必須要加上「;」(分號)，代表一行的結束

## <span class="section_supplementary">補充</span>

### `using System`

大家可以看到程式裡面出現了 Console.WriteLine 以及其他 method。那這些 method 到底都寫在哪裡呢？事實上，就是寫在那些名為「System」的程式庫裡。那些程式庫包含了大量可以讓我們寫 C# 更方便的程式碼，以及我們之後會用到的「視窗」也都是寫在名為「System.Windows.Forms」的程式庫內。想要使用這些程式庫，就必須要在程式碼上面打上「using {程式庫名稱}」才行。不過剛開始不太需要注意，因為你的 IDE 都會自動地幫你打理好這些問題。

### Console

寫過 C\C++ 程式的人，我想大多數顯示出來的結果都是出現在這個黑色的視窗上對吧？其實我們現在所看到這些視窗、按鈕甚麼的，背後都是由大量的程式碼所建立出來的。而且事實上，這些圖形的畫面是非常耗費資源。早期的程式設計師寫程式，都是在我們看到那個黑底白字的畫面上跑的。而 Console 就是 Windows 下的黑底白字介面。大家可以在「附屬應用程式」>「命令提示字元」那邊開啟 Console 的畫面。

### Entry Point

每個程式都會有個獨一無二的「進入點」，也就是作為電腦一開始執行的 method。C\C++ 一般是使用「int main(void)」，win32 的程式是使用「int WINAPI WinMain(...)」，而 C# 就是這個「static void main(string[] args)」。基本上，這個名稱是規定好的，所以不可以隨便更改。如果改成別的名字，電腦就會不知道該從哪裡開始執行。

## <span class="section_practice">練習</span>

1. 試著讓程式顯示多行的文字
例如：

    ```
    C# 真好玩
    而且我會寫第一個程式了
    這是第三行的說
    ```

2. 接上一題，試著讓程式顯示一行停頓一次。每次停頓時，必須要按下鍵盤按鍵才會繼續。

3. 根據「相關資訊連結」的「Console 可以使用的 method 清單」，查查看還有甚麼其他 method 可以使用。例如：讓電腦發出 Beep 的一聲。

參考解答：<https://github.com/slmt-tutorial-channel/c-sharp-solutions/blob/master/class_1_10/class3.md>

## <span class="section_references">相關資訊連結</span>

### System 程式庫裡面包含的 Class 清單

<http://msdn.microsoft.com/zh-tw/library/system%28v=vs.80%29.aspx>

### Console 可以使用的 method 清單

<http://msdn.microsoft.com/zh-tw/library/system.console_methods%28v=vs.80%29.aspx>
