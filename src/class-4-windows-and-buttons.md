# 第 4 課 - 視窗與按鈕

## <span class="section_abstract">本課介紹</span>

這課主要在介紹如何製作簡單的視窗程式，並且在視窗上做出按鈕

## <span class="section_video">教學影片</span>

<iframe width="560" height="315" src="https://www.youtube.com/embed/5txYdHXgX44" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## <span class="section_highlights">重點提示</span>

1. 選擇「檔案」>「新增專案」>「Windows Form 應用程式」就可以自動地建立視窗程式
2. IDE 內的「屬性」視窗可以修改視窗的設定值
   - Ex: `Text` 是「視窗標題」、`BackColor` 是「背景顏色」
1. 想要放入按鈕，只要找到旁邊的「工具箱」視窗，然後把按鈕拖出來就可以了
2. 想要修改其他物件的屬性，只要點一下那個物件，再去看屬性視窗就可以了
3. 當我們按下按鈕後，程式會自動執行 `private void button1_Click(...)` 這個 method 裡面的程式碼
4. `MessageBox.Show()` 可以用來顯示對話框，小括號內放的就是要顯示的文字

## <span class="section_supplementary">補充</span>

### 視窗程式

所謂視窗程式，就是指一般在 windows 內看到這些可以放大縮小的程式。想要建立一個視窗程式需要很複雜的程式碼，例如要利用「C 語言」寫出視窗要做很多不同的設定。像是除了設定視窗的資訊之外，還要進行視窗註冊等等。幸虧 .NET Framework 裡面早就幫你處理好了。這就是為了要讓程式設計師能夠專心在處理其他更重要的事情上面。

### Form1.Designer.cs

每當你建立專案的時候，你的 IDE 可是在背後做了很多事情。對於一些有寫程式經驗的人來說，可能會很疑惑到底設定視窗(Ex: 大小、標題...)的程式碼都塞在哪裡？答案是塞在名為「Form1.Designer.cs」這個檔案裏面。注意檔案名稱會隨著視窗名稱改變。每當我們在「屬性」區塊上面做設定，IDE 都會自動地修改「Form1.Designer.cs」裡面的程式碼。

有興趣的話，可以打開那個檔案看看。不過建議不要更動裡面的程式碼，除非你已經很熟悉裡面在做甚麼。 

## <span class="section_practice">練習</span>

1. 改改看「屬性」視窗裡面其他設定，看看會造成甚麼影響？
2. 例如把 `MaximizeBox` 跟 `MinimizeBox` 設為 `false` 看看？
3. 或者把 `Cursor` 設為 `Hand` 然後執行看看？ 
