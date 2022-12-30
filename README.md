# swag_live_downloader
:movie_camera::movie_camera::movie_camera::movie_camera:
#### Windows application for download Live stream video from https://app.swag.live/ 

## Step 1:
  Download application from [Here](https://drive.google.com/file/d/1mKl55TKWp9rwcfqVzt2SO3GjHoVuH5vp/view?usp=sharing)(google drive).:toolbox:

## Step 2:
  Install Streamlink.exe
  Or you can donwload from [Here](https://github.com/streamlink/streamlink/releases/tag/3.2.0)

## Step 3:
  Open browser and **Navigate** to https://app.swag.live/ and **Login** your account.
  
## Step 4:
  To extract token open any page in https://app.swag.live/ and **Press F12** to open DevTool from your browser then **Paste** the following code into the console. Hit **Enter** then your token will be printed.
  Try
  ```
  var db;
  var request = indexedDB.open("localforage", 2);
  request.onsuccess = function() {
    db = request.result;
    var tx = db.transaction("keyvaluepairs", "readonly");
    var store = tx.objectStore("keyvaluepairs");
    var _request = store.getAll("_accessToken")
    _request.onsuccess = function() {
      var token = _request.result.toString();
      console.log(token);
    };
  };
  ```
  Or
  ```
  var db;
  var request = indexedDB.open("localforage", 3);
  request.onsuccess = function() {
    db = request.result;
    var tx = db.transaction("keyvaluepairs", "readonly");
    var store = tx.objectStore("keyvaluepairs");
    var _request = store.getAll("_accessToken")
    _request.onsuccess = function() {
      var token = _request.result.toString();
      console.log(token);
    };
  };
  ```
 
  
## Step 5:
  **Copy and paste** your token into `token.txt` then save and close it.
    
## Step 6:
  **Double click** to run the application `swag_live_downloader.exe`.
  
## Step 7:
  **Paste** the id of swager you want to download, if is live stream is on start download if not check every 10 mins.
  
  
---------------

# swag 直播下載器
:movie_camera::movie_camera::movie_camera::movie_camera:
#### Windows的程式，用來下載在 https://app.swag.live/ 上的直播影片.

## 第一步:
  **下載**[主程式](https://drive.google.com/file/d/1mKl55TKWp9rwcfqVzt2SO3GjHoVuH5vp/view?usp=sharing)(google drive).:toolbox:

## 第二步:
  安裝 streamlink.exe
  或者到[官方](https://github.com/streamlink/streamlink/releases/tag/3.2.0)下載

## 第三步:
  使用瀏覽器開啟網頁 https://app.swag.live/ 並且**登入**Swag帳號.
  
## 第四步:
  在 https://app.swag.live/ 的任何頁面**按下F12** 打開開發者工具把下面的程式碼複製貼上在console內按下**Enter**鍵, Token就會印在下方
  試試 indexedDB有些人的瀏覽器升級到v3了請改用第二個程式碼如果不確定請兩個都嘗試看看
  ```
  var db;
  var request = indexedDB.open("localforage", 2);
  request.onsuccess = function() {
    db = request.result;
    var tx = db.transaction("keyvaluepairs", "readonly");
    var store = tx.objectStore("keyvaluepairs");
    var _request = store.getAll("_accessToken")
    _request.onsuccess = function() {
      var token = _request.result.toString();
      console.log(token);
    };
  };
  ```
  或者
  ```
  var db;
  var request = indexedDB.open("localforage", 3);
  request.onsuccess = function() {
    db = request.result;
    var tx = db.transaction("keyvaluepairs", "readonly");
    var store = tx.objectStore("keyvaluepairs");
    var _request = store.getAll("_accessToken")
    _request.onsuccess = function() {
      var token = _request.result.toString();
      console.log(token);
    };
  };
  ```
  
## 第五步:
  打開`token.txt`檔案並把token複製貼上來, 存檔並關閉`token.txt`.
    
## 第六步:
  執行應用程式`swag_live_downloader.exe`
  
## 第七步:
  驗證Token成功後輸入要下載的主播ID 1. 開始下載(如果正在直播) 2. 每10分鐘檢查主播是否上線如果上線開始下載 :+1:
