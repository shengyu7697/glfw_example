# glfw example

### Windows
切換目錄到 `thirdparty/glfw` 執行 `gen_vs2015_64.sh` 產生 `GLFW.sln` 專案檔  
開啟 `build/GLFW.sln` 執行 INSTALL 專案  
(此時確保 `C:\Program Files` 有寫入權限, 預設會安裝到 `C:\Program Files\GLFW` 底下)  

再回到 `glfw_example/` 目錄下執行 `gen_vs2015_64.sh` (腳本預設找 `C:/Program Files/GLFW/lib/cmake/glfw3` 底下的 .cmake 檔)  
開啟 `glfw_example.sln` 建置方案即可完成  

### 顯示卡驅動
確保有安裝正確的顯示卡驅動  
[nvidia 驅動下載](http://www.nvidia.com.tw/Download/index.aspx?lang=tw)  
