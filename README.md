
## 使用說明
在其他網頁中，用 JQuery 引入 gallery

### 網站的絕對路徑
在 index.js 有 url，必須設定絕對路徑。
- index.html 需引入 <script src="index.js"></script>
- gallery/index.html 需引入 <script src="../index.js"></script>

因為當你使用 jQuery 的 load() 方法時，程式的「基準點」會變成是由主目錄的 index.html 來發出請求，這時如果你在被載入的檔案裡用相對路徑（例如 ../categories.json），它就會往上一層去找（變成去根目錄的上一層找），自然就會找不到檔案而報錯。

如果你改用絕對路徑（或是以主目錄 index.html 為基準的路徑），就可以順利抓到檔案。

### gallery 內的相片集
- 只需將照片的檔名改成 photo001 ~ photo999.jpg 
- 並在 info.json 輸入網頁相關內容

### 顯示相片集
在 categories.json 依序輸入想要顯示的相片集資訊即可。




