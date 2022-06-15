# 第 46 課 - 五子棋小遊戲 (七) - 簡單勝利判斷

## <span class="section_abstract">本課介紹</span>

本課為五子棋系列最後一課  
這次的目標就是要寫一個簡單的勝利判斷  
來看看怎麼寫吧！  

## <span class="section_video">教學影片</span>

<iframe width="560" height="315" src="https://www.youtube.com/embed/LSg15Q54TeI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## <span class="section_highlights">重點提示</span>

### 製作重點

- 檢查勝利的方式 - 只要檢查最後下的那顆棋子的八個方向是否有五顆棋子連成一直線
- 在測試程式時，若發生錯誤，可以把滑鼠移到變數上。此時就會顯示該變數的值為多少。
- 注意在 if 內有多個條件時，若程式發現只要檢查前面的條件就足夠，後面的條件就不會被執行。

### 製作步驟

1. 在 `Board` 內新增一個 private `Point` 變數，`lastPlacedNote`，一開始設為 `NO_MATCH_NODE`
    1. 新增一個 public get 存取器 `LastPlacedNote`，用來取得 `lastPlacedNote`
    2. 在 `Board` 內的 `PlaceAPiece` 把最後下子的位置存在 `lastPlacedNote`
2. 在 `Game` 內新增一個 private `PieceType` 變數 `winner`，一開始設為 `PieceType.NONE`
    - 新增一個 public get 存取器 `Winner`，用來取得 `winner`
3. 在 `Game.PlaceAPiece` 內的交換選手前，加入 `CheckWinner`。代表在交換前會先檢查勝利者。
4. 實作 `Game` 的 `CheckWinner()` (先檢查一個方向)
    1. 先用兩個變數 `centerX` 跟 `centerY` 儲存 `board.LastPlacedNote` 的 X 跟 Y 座標
    2. 加入一個 while 迴圈檢查五顆座標連續的棋子是否顏色相同。檢查棋盤上某個位置的顏色可以用 `board.GetPieceType(x, y)`。
        - 記得在呼叫 `board.GetPieceType(x, y)` 前，先檢查座標是否有超出棋盤邊界
        - 若發現有一顆顏色不同就提早跳出 (break)
    3. 檢查是否看到五顆棋子，若沒看到代表沒有勝利者
5. 在 `Form1_MouseDown` 內檢查 `game.Winner`。
    - 若為 `PieceType.BLACK`，就用 `MessageBox` 印出「黑色獲勝」。白色也用類似方式處理。
6. 在 `Game.CheckWinner` 內增加兩個 for 迴圈檢查八個方向

## <span class="section_practice">練習</span>

1. 嘗試解決最後棋子下在五顆連線的中間，而不是邊邊時無法判斷勝利的 bug
2. 嘗試實作重新啟動遊戲的功能
3. 在有人快勝利時提出警告訊息
4. 想出一個方法讓白色自動下子 (例如：最簡單的作法，隨便找個讓白色隨機亂下)

參考解答：<https://github.com/slmt-tutorial-channel/c-sharp-solutions/blob/master/class_41_50/class46.md>
