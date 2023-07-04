# 第 9 課 - Label 與 點擊次數記錄程式

## <span class="section_abstract">本課介紹</span>

這課主要是在利用寫一個小型程式來複習前面學到的內容，另外再順便介紹一個新的元件 Label。

## <span class="section_video">教學影片</span>

<iframe width="560" height="315" src="https://www.youtube.com/embed/j2HL_tZqqVQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## <span class="section_highlights">重點提示</span>

1. Label 指的是顯示在視窗上的標籤，可以藉由修改 Text 屬性來變更他顯示的文字內容
2. 變數不可以存在 `button1_Click` 內，因為每一個變數都有一個「有效期限」。當程式碼執行完 `button1_Click` 之後，這個變數就會「過期」。如果希望變數一直存在，就必須要放在外面的區塊中。
3. 修改 Label 的 Name 屬性就可以讓我們透過程式碼取得該元件來操作它的內容。
4. 每次修改完 `times` 這個變數之後，記得順便更新 Label 的文字哦~ 不然就會出現沒有同步到的狀況。

## <span class="section_practice">練習</span>

1. (基礎) 試試看再加上另一個按鈕，然後按下去會一次 +2
2. (進階) 試試看再加上一個遞減按鈕，然後按下去會減少，但最低只能減少到 0 哦！
   - 本題需要 `if ...` 語法的概念
