# 使用方式

## 網頁版
1. ### 安裝油猴擴充
    下載連結 : https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo?hl=zh-TW
  
2. ### 點新增腳本

3. ### 將 notion-zh_CN.js 所有內容貼上並儲存

## 電腦版

### windows
1. （自**2.0.4**版本後，任意語言都等同於中文了）
2. notion 安裝目錄：`C:\Users\使用者名稱\AppData\Local\Programs\Notion\`
3. 打開`C:\Users\使用者名稱\AppData\Local\Programs\Notion\resources\app\renderer`文件夾
4. 下載 `notion-zh_CN.js` 到上述文件夾（renderer）
5. 打開 `preload.js`
6. 在最後一行加上
   ```js
   //# sourceMappingURL=preload.js.map
    require("./notion-zh_CN") // 新增該行
   ```
7. 重新啟動

- 上述操作也可以使用 PowerShell 命令來完成。
  命令執行完成後，在 Notion 中使用 <kbd>CTRL</kbd>+<kbd>R</kbd> 可以熱更新界面。
   ```powershell
   Invoke-WebRequest -Uri "https://github.com/Reamd7/notion-zh_CN/releases/latest/download/notion-zh_CN.js" -OutFile "$HOME\AppData\Local\Programs\Notion\resources\app\renderer\notion-zh_CN.js"
   Add-Content "$HOME\AppData\Local\Programs\Notion\resources\app\renderer\preload.js" 'require("./notion-zh_CN")'
   ```


###### 修改自專案 [notion-zh_CN](https://github.com/Reamd7/notion-zh_CN)
