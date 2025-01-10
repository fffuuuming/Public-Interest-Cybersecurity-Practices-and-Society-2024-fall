---
title: Gophish 使用教學

---

# Gophish 使用教學

## 1. Gophish 是什麼
**Gophish** 是為企業和滲透測試人員所設計的開源網路釣魚工具。它提供了快速，輕鬆地設置和執行網路釣魚攻擊，以及安全意識培訓的能力。

## 2. 釣魚的嚴重性
**釣魚**（**Phishing**）是一種常見的網絡攻擊手法，其重要性在於它能夠影響個人和組織的安全。釣魚攻擊通常涉及偽裝成可信任的來源，如親朋好友，公司同事或老闆，以騙取個人信息，如密碼、信用卡號碼等。這些信息一旦落入惡意攻擊者手中，可能會用於盜竊、詐騙或其他犯罪活動。

常見例子如下：
- **假冒銀行郵件**：收到一封看似來自你銀行的電子郵件，要求更新帳戶資訊。
- **假網站**：點進某個連結後，進入一個看起來非常像真實網站的頁面，要求你輸入登入資訊。
- **假冒親朋好友**：收到一封看似朋友或家人寄的電子郵件，要你匯款或提供個人訊息。

更甚者，光是點擊釣魚信件裡的連結或檔案即可能造成損失：

- **惡意連結**：一封看似來自可信來源的郵件，要求你點擊一個連結來更新帳戶訊息或查看重要文件，但這個連結實際上會將你引導到一個惡意網站，並自動下載和安裝惡意軟體。

- **惡意 PDF 文件**：你可能會收到一個看似無害的 PDF 文件，當你打開它時，內嵌的惡意程式會在你的電腦上執行，從而感染你的系統。

## 3. 如何防範釣魚攻擊

- **謹慎點擊**：
    - 不隨便點擊郵件或訊息中的連結，特別是那些來自不認識或看起來可疑的人。
    - 不輕信緊急要求：釣魚攻擊經常利用緊急語氣來催促你行動。遇到這類要求時，保持冷靜並仔細檢查。
- **驗證來源**：打開任何附件或點擊任何連結之前，務必確認發件人的身份和訊息的真實性。
    - 檢查發件人地址：確認發件人的電子郵件地址是否來自可信來源。注意拼寫錯誤或不常見的域名。
    - 將滑鼠懸停在連結上以查看實際URL。釣魚攻擊常常使用與真實網站相似的URL。
- **使用防毒軟體**：確保你的電腦安裝並運行最新的防毒軟體，並定期進行掃描。
- **設置強密碼**：使用長度超過 12 個字符的強密碼，包括大小寫字母、數字和符號。避免使用常見詞語和個人訊息。
- **啟用雙重驗證**：增加額外的安全層，保護你的帳戶免受未經授權的訪問。

Google 專為釣魚攻擊所設計的測驗：[https://phishingquiz.withgoogle.com](https://phishingquiz.withgoogle.com)

## 4. Gophish 對防範釣魚的幫助
- **模擬釣魚攻擊**：Gophish 讓公司能夠創建和發送仿真的釣魚郵件給員工，從而測試其的應對能力，並識別哪些員工可能成為釣魚攻擊的目標。

- **教育和培訓**：通過定期的釣魚模擬，Gophish 能幫助員工提高對釣魚攻擊的警覺性和識別能力，從而減少上當受騙的機會。

- **數據分析**：Gophish 提供詳細的報告和數據分析(點擊率，提交率等等)，能清楚了解員工對釣魚攻擊的反應情況，有助於識別弱點並針對性地加強防禦措施。

- **提高安全意識**：資安最大的弱點即是人，透過持續的模擬和培訓能提高整個組織的安全意識，讓每人皆是防範釣魚攻擊的一部分，從而提高整體的網絡安全水準。

## 5. 安裝 Gophish
- 前往[Gophish 官方github](https://github.com/gophish/gophish/releases)，根據自己的電腦版本下載適合的壓縮檔並解壓縮，您可能需要滑動頁面到 Asset 的地方，如下圖：![gophish_zip](https://hackmd.io/_uploads/BkzvRhOMJx.png)
Windows 選擇`gophish-v0.12.1-windows-64bit.zip`，Mac選擇`gophish-v0.12.1-osx-64bit.zip`

- 運行Gophish : 
    - **Windows** : 進入到剛解壓縮完的資料夾，點擊Gophish.exe執行，會跳出命令提示字元(小黑框)如下圖所示:![window_exe](https://hackmd.io/_uploads/BytJGAYGke.png)
        - 紅線地方為初始預設的帳號及密碼，等等可能會用到 
        - 注意這裡需要保持命令提示字元（小黑框）不被關閉，若關閉則會終止運行，
    - **Mac** : 在剛解壓縮完的檔案夾下開啟終端機(terminal)，輸入 `./gophish` 並執行，具體流程如下：
        - 右鍵點擊解壓縮完的檔案夾 -> 新增位於檔案夾位置的終端機視窗![gophish_open_terminal](https://hackmd.io/_uploads/SJjtZTOf1l.png)
        - 輸入命令 `chmod +x ./gophish` 並按 enter 執行，這會賦予您執行的權限![chmod_gophish](https://hackmd.io/_uploads/HkXpT9ofke.png)
        - 輸入命令 `./gophish` 並按 enter執行，這會開始運行Gophish![initial_login](https://hackmd.io/_uploads/H1WSn9ozJx.png)
        - 紅線地方為初始預設的帳號及密碼，等等可能會用到 
        - 需保持終端機不被關閉，若關閉則會終止運行，


- 打開瀏覽器， 進入 [https://127.0.0.1:3333](https://127.0.0.1:3333) 以訪問登入頁面
    - windows 若遇到 "你的連線不是私人連線"，點選 "進階" -> "繼續前往網站" 即可![https_warning](https://hackmd.io/_uploads/HkxVQCYzyl.png)mac若遇到 "此連線非私人連線"，點選 "顯示詳細資訊" -> "參訪此網站" 即可![private_connect](https://hackmd.io/_uploads/rJ7lXsoGye.png)


- 輸入帳密 : 
    - 預設帳號皆為 `admin`
    - 如你的 Gophish 是 v0.10.1 之後的版本，在首次啟動Gophish時，會在命令提示字元/終端機上生成一個初始密碼，詳情請回剛才"**運行Gophish**"段落查看。
    - 若為 v0.10.1 之前的版本，則預設密碼為 `gophish`
    - 第一次使用初始密碼登入後會要求重設密碼，請重新設置並將其保存

成功登入頁面！

## 6. 實際操作
以下步驟將會帶您熟悉基本功能與操作，並進行情境模擬：公司高層為了提升員工的安全意識及對釣魚的敏感度，仿造了一封釣魚信件，要求其員工依指示點擊信件裡的連結來重設gmail帳密，但此連結實際被導到釣魚者的網頁。
> 備註 1：以下教學所顯示的gmail帳號皆為範例，等等操作時請以您想用哪個信箱發送釣魚郵件填寫即可。

### Sending Profile 寄件設定檔
- 為了能順利送信，Gophish 需要您對 SMTP 的相關配置進行設定。
- **SMTP (Simple Mail Transfer Protocol, 簡單郵件傳輸協議)** : 
您可以將其想像成電子郵件的郵遞系統。當你發送一封電子郵件時，SMTP 就像是郵遞員，他會拿著你的信，找到合適的路線，並把信件送到你朋友的信箱（郵件伺服器）。
- Gophish 中，SMTP 用來發送釣魚郵件給目標對象。它確保這些郵件被正確地路由並送達給指定的收件人。

以下是詳細步驟：
1. 點擊 "**+New Profile**" 新增設定檔
2. 會看到許多項目，以下一一說明如何填寫：
    - **Name** : 為這個Profile取一個任意的名字，ex : gmail test
    - **Interface Type** : 默認為SMTP
    - **SMTP From** : 受害者所看到的寄件人， ex : user@gmail.com
    - **Host**: 這裡我們使用Gmail SMTP server: smtp.gmail.com:587
    - **Username** : 同 **SMTP From**
    - **Password** : 這裡的密碼不是 google 帳號本身的密碼，而是要使用 google 生成的應用程式專用密碼，這需要您先為帳號開啟兩步驟驗證功能，開啟步驟如下：
        - 點擊Gmail 頭像 -> 點選 "**管理你的 Google帳戶**" (Manage your account) ![smtp_setting_a](https://hackmd.io/_uploads/Hk-lVKifye.png)


        - 點選安全性(Security) -> 下滑到登入Google的方式 -> 點選兩步驟驗證![smtp_setting_c](https://hackmd.io/_uploads/Hy2t4KsMJg.png)

        - 啟用兩步驟驗證功能，並啟用任一種登入方式![smtp_setting_d](https://hackmd.io/_uploads/H1woVKsfJe.png)

        - 回到 "**管理你的 Google帳戶**"，根據您的頁面是中文或英文介面，在搜尋列中輸入 "應用程式密碼" :![smtp_setting_e](https://hackmd.io/_uploads/H1CVSYoMkl.png)或 "app password" : ![app_password](https://hackmd.io/_uploads/HJvTI9sGJg.png)並點選


        - 輸入您的應用程式名稱(ex : Gophish)並點選建立![smtp_setting_f](https://hackmd.io/_uploads/Hk44wYoGJe.png) 

        - 複製 app password 並回到 Sending Profile 頁面，貼在**Password**欄位中 ![smtp_setting_g](https://hackmd.io/_uploads/SJc2wKifyg.png)



3. 您的頁面應該會類似下圖範例：![smtp_setting_5](https://hackmd.io/_uploads/ryp6zYYM1e.png)
為了確保設定成功，點選 "**Send Test Email**"，輸入First name, last name(皆任意)，輸入Email(當前用來設定Sending Profile的email即可)，點擊 "**Send**"，當看到出現 "Email Sent!" 如下圖，即代表設定成功。![smtp_setting_6](https://hackmd.io/_uploads/HkD_zYYGJe.png)
您也可至方才指定收信的信箱查看有無收到信，如看到下圖即代表成功：![smtp_setting_7](https://hackmd.io/_uploads/S1DYzatMJg.png)
4. 點擊 "**Save Profile**" 儲存設定檔，完成設置！
---
### Landing Page 釣魚頁面
Landing Page 是當用戶點擊郵件裡的連結時所跳轉的頁面，透過精心設計，它能誘使用戶在上面留下他們的敏感資料，並能在獲取這些資料後將用戶重新導向到另一個網站。以我們的情境而言，我們模擬gmail的登入畫面。以下是詳細步驟：
1. 點擊 "**+New Page**" 新增頁面
2. 輸入頁面名稱（任意）ex : google
3. 點擊 "**Import Site**" 來匯入網址，這裡我們用google登入的頁面：https://accounts.google.com，輸入完後點擊 "**import**" 完成匯入。若匯入成功，點選 "**Source**" 按鈕可以看到google登入的畫面，您應該會看到類似下圖範例：![landing_page_1](https://hackmd.io/_uploads/r1C94YYfkg.png)
4. 下方有 "**Capture Submitted Data**" 的選項，可以獲取用戶提交的資料（ex : 用戶名稱），點選後會再分別出現兩個選項：
    - Capture Passwords : 連受害者提交的密碼也一併獲取
      > 備註：若只是要測試與統計是否提交數據，請不要勾選以免洩漏帳號隱私，甚至觸法
    - Redirect to  : 受害者提交表單後可以將頁面重新導向到指定的 URL。為了不讓受害者起疑，我們使用 https://accounts.google.com，等受害者提交他們的資訊後將其重新導到真正的google登入頁面。
5. 點選 "**Save Page**" 完成設定
---
### Email Templates 釣魚郵件模板
郵件模板是發送給目標的電子郵件內容，用來誘騙受害者點擊連結、附件及輸入他們的隱密資料。模板可以從現有電子郵件匯入，或從頭開始創建。此外，模板還能通過設定追蹤用戶何時打開電子郵件。

以下示範如何用現有電子文件匯入，我們將用自己的信箱寄給自己一封釣魚郵件，並取出其原始郵件來做匯入，詳細步驟如下:
1. 先寫好釣魚郵件內容並寄給自己，以下提供兩個範例 :
 ```
 各位同仁好，

為符合內控規定，加強密碼管控，以降低帳號被盜之風險。
全體人員密碼預設為「P@ssw0rd」，請人員登入後修改密碼。

Gmail 系統網址為 : https://accounts.google.com

※密碼規則如下：

(1)最短密碼長度：8碼（最長10碼）
(2)啟用密碼複雜度：密碼需包含 -> 半形英文、半形數字、半形特殊符號
(3)定時更改密碼：180天需改一次密碼

如有任何疑問請洽資訊部，謝謝各位
 ```
 ```
 親愛的用戶您好，
 
 
 我們已經記錄了您個人資料的最近更新。如果這些更改是您本人進行的，則無需進一步操作。
 
如果您未授權這些更改，請立即檢查它們以確保您的帳戶安全。

請儘速登錄您的帳戶並驗證這些更改：https://accounts.google.com


感謝您的注意

 ```
2. 到自己信箱，複製剛剛發送的郵件的原文內容：
    - 點選剛剛發送的信件，點擊右上角三個點點，選擇"**<>顯示原始郵件**"![email_template_1](https://hackmd.io/_uploads/ryT415tzkl.png)

    - 點選"**複製到剪貼簿**"，複製郵件的原文內容![email_template_2](https://hackmd.io/_uploads/BybSk5Fz1l.png)
3. 點擊 "**+New Template**" 新增模板
4. 輸入模板名稱（任意）ex : mytemplate
5. 點選 "**Import Email**" 按鈕，將剛剛複製的原文內容貼上，並點選 "**Change Links to Point to Landing Page**"，這會將模板中的超連結自動變更為 Landing Page 的網址。點選"**Import**"儲存
6. 輸入您用來發送釣魚郵件的地址
7. 輸入郵件標題，ex : Gmail 密碼變更通知
8. 點選 "**Add Tracking Image**"，這能幫助您追蹤用戶何時打開電子郵件
您應該會看到類似下圖範例：![email_template_3](https://hackmd.io/_uploads/r1NItaFGkl.png)點選 "**Save Template**" 儲存模板
---
### User & Groups 用戶和群組
群組讓您能輕鬆管理每次釣魚活動想針對的用戶(受害者)
1. 點選 "**+New Group**" 
2. 輸入Group名稱（任意）ex : mygroup
3. 匯入用戶 : 有兩種選擇，以下分別介紹 :
    - 單筆增加：依序填入用戶的 first name(名), last name(姓), email 及 position(職位)後點選 "**+Add**" 即可 
    - 使用csv範本匯入：點選 "**+Bulk Import Users**" 並選擇要匯入的csv檔
        - 注意：上傳的csv檔須有下列四個欄位，範例如下圖：![csv_example](https://hackmd.io/_uploads/B1nByGFMyx.png)
    - 為求測試方便，您可以先創建一個只有自己的群組以便之後測試活動是否成功發起。
4.點選 "**Save changes**" 完成設定
---
### Campaigns 釣魚活動
Gophish 透過發起釣魚活動來完成釣魚，您將會把剛剛所做的設定(Sending Profile, Landing Page...)全部連結起來。以下是詳細步驟

1. 點選 "**+New Campaign**" 
2. 輸入活動名稱（任意）， ex : mycampaign
3. 依序選擇方才所建的 Email Template, Landing Page, Sending Profile, Users & Groups
4. **Launch Date** : 發起活動的時間，Gophish 預設您會馬上發起活動，可以不用更動。
5. **Send Emails By** ：何時會發送完全部的釣魚郵件，Gophish 預設您在發起活動後會立刻將全部釣魚信寄達至受害者的信箱。可以不用填寫。
6. **URL** : 您的釣魚伺服器的URL，用來將測試結果傳回至伺服器，同時這個網址也會是當受害者將滑鼠懸停在連結上時，實際顯示的URL。所以申請一個近似的網域名稱指向釣魚伺服器會使攻擊更加真實。在此教學中為了簡單起見，我們是在自己的電腦上跑Gophish，所以填 http://127.0.0.1 即可。
6. 您應該會看到類似下圖範例 ：![campaign_1](https://hackmd.io/_uploads/ry-Gc2FGke.png)
點選 "**Launch Campaign**"，發起活動！
---
### 查看結果
- 發起活動後，您會看到如下頁面：![campaign_result](https://hackmd.io/_uploads/BJjyccsGye.png)
  可以看到詳細的統計數據，如點擊率、提交率等等。


- 您也可以點選側邊欄的Dashboard : ![dashboard](https://hackmd.io/_uploads/B1ay9cizJl.png)
  下方會呈現曾發起過的活動，點選 "**View Result**" 查看活動的詳細資訊。
---
### 參考連結
- [https://docs.getgophish.com/user-guide](https://docs.getgophish.com/user-guide) Gophish 官方教學
- [https://www.youtube.com/watch?v=Yes4oc046hY&list=PL8q5RAVJcMdbZeiO0GHXH1LhalZka85YA](https://www.youtube.com/watch?v=Yes4oc046hY&list=PL8q5RAVJcMdbZeiO0GHXH1LhalZka85YA)
- [https://ithelp.ithome.com.tw/articles/10280378](https://ithelp.ithome.com.tw/articles/10280378)
- [https://medium.com/@jieshiun/如何在-azure-設定-sendgrid-smtp-發信-f02ab6074f2d](https://ithelp.ithome.com.tw/articles/10280378)
- [https://www.cnblogs.com/tomyyyyy/p/15503208.html](https://ithelp.ithome.com.tw/articles/10280378)
