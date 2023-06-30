# 第 7 課 - 變數宣告意義與型別

## <span class="section_abstract">本課介紹</span>

此課解釋為何變數需要進行宣告，另外進一步地介紹之前提過的 `int` 型別，並另外介紹 `float`、`double`、`bool` 型別的變數。

## <span class="section_video">教學影片</span>

<iframe width="560" height="315" src="https://www.youtube.com/embed/k2kjfxbWUuM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## <span class="section_highlights">重點提示</span>

1. 宣告變數的意義在於，先告知電腦到底我們要給這個變數多少記憶體空間 (電腦會從型別判斷) 以及它的名稱是甚麼。
2. 在 C# 裡面，每個 `int` 的變數可以分配到 32 bits(4 bytes) 的記憶體空間。也就是說，對於每個 `int` 的變數，電腦會存放 32 個 0 或 1 在記憶體裡面。
3. `int` 只能儲存有限大小的數字，而這個範圍是從 2^31 - 1 到 - 2^31，也就是 2,147,483,647 到 - 2,147,483,648 這之間的數字。
4. 想要儲存小數可以使用 `float` 或 `double`，一般會推薦使用 `double`，因為可以儲存較廣的數字。
5. C# 預設情況下會將所有數字當成 `double` 來處理。
6. 有一種型別 `bool` 只能儲存 `true`、 `false` 兩種資料，這種數值通常用來儲存判斷式的結果。

## <span class="section_supplementary">補充</span>

### 32 bits 的整數

本課提到 C# 裡面的 `int` 是使用 32 bits 的空間。但是在 C/C++ 裡面，int 變數使用的空間則跟 CPU 與 Compiler 有關。有時候會是 32-bit ，有時候是 64-bit。而 C# 並沒有這個問題。因為事實上，C# 內建了三種 `int` 型別，分別為 `Int16`、`Int32`、`Int64`，代表16、32、64 bits 的整數。當我們打 `int` 時，程式會自動解析為 `Int32` 來處理。因此固定都是 32-bit 的整數。

### 大數 Big Integer

`int` 能儲存的數字有限，因此當我們需要儲存更大的數字時，可能就不夠用了。從上一段文中可以知道，C# 還有內建的 `Int64` 這個型別可以使用。但是在密碼學中，進行 RSA 演算法時，因為內含大量的指數 (exponential) 與模數 (mod) 預算，使得 64-bit 的數字也不足以儲存計算結果。這個時候，大數 (Big Integer) 就登場了。

「大數」其實與一般的「整數」無異，不過它使用的記憶體空間會隨著儲存的數字做動態變化。基本上只要你的記憶體夠大，想要儲存多大的數字都不是問題。大數實作方式有很多種，而 Java 跟 C# 都有官方寫好的版本供大家使用。如何實作大數並加以使用也是程式競賽中時常出現的考題呢！

## <span class="section_references">相關資訊連結</span>

### 變數的內建型別列表

<https://learn.microsoft.com/zh-tw/previous-versions/visualstudio/visual-studio-2008/cs7y5x0x(v=vs.90)?redirectedfrom=MSDN>

### 大數 Big Integer 相關資訊

<https://learn.microsoft.com/zh-tw/dotnet/api/system.numerics.biginteger?view=net-7.0&redirectedfrom=MSDN>
