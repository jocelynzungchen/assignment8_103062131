# assignment8_103062131

assigment8                 103062131陳映竹

這次的作業只需將lab10的東西和提供的socket sample拼湊再一起即可。
把lab10的兩個page再新增一個ip_page，將ip_page設成一開始的初始畫面。

onCreate()
創建初始畫面。
照助教原本SocketSample給的，我只將原來onClick()中"SUMMIT"按鍵的功能(跑thread)移到ip_page
按下"OK"之後執行。

jumpToMainLayout() & jumpToResultLayout()
在activity_main跟result_page的執行畫面。
用跟lab10一樣的code。

onClick()
加減乘除鍵按下去之後的處理。


這次遇到的問題主要在把結果傳到server的部分。原本想說把client端弄成while(true)看能不能一直
讀新結果，結果沒反應，後來把讀answer的部分丟到ans產生的地方(onClick)還是沒有反應。
後來是把server的讀值也加上while(true)才成功執行。(但明明外面已經有一層while(true)了，也不
知道為神麼還需要加一層...)
至於server端要一直顯示更新answer的部分，由於開新視窗的方法我只知道JFrame，所以就在server 
extends JFrame，用label顯示。
