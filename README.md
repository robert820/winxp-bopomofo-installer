<div align="center">

<a href="https://blog.dei3c.com" target="_blank" rel="noopener noreferrer">
  <img src="https://github.com/user-attachments/assets/2830eb70-512c-4ddb-87ec-5213a6e465b1" alt="得翼科技 | 微軟舊注音 (ㄅ半) 一鍵免費安裝器" height="70" />
</a>

<br /><br />

**繁體中文** · [English](docs/readme/README_en.md) · [简体中文](docs/readme/README_zh-CN.md)

# 微軟舊注音 (ㄅ半) 一鍵免費安裝器 (Microsoft Legacy Bopomofo 1-Click Installer)

### 專為 Windows 10 / 11 系統打造的原生一鍵安裝、自動修復與還原工具
告別升級 Windows 10/11 後找不到舊注音、新版記事本無選字框的困擾！一鍵極速找回熟悉順手的打字體驗。

[![Platform](https://img.shields.io/badge/Platform-Windows%207%20%7C%208%20%7C%2010%20%7C%2011%20%7C%20WinPE-blue?style=flat-square&logo=windows)](https://github.com/robert820/winxp-bopomofo-installer)
[![License](https://img.shields.io/badge/License-Freeware-informational?style=flat-square)](LICENSE)
[![Type](https://img.shields.io/badge/Type-Freeware%20%7C%20Portable-success?style=flat-square)](#-下載與使用說明)
[![Download](https://img.shields.io/badge/Download-GitHub%20Releases-blue?style=flat-square&logo=github)](https://github.com/robert820/winxp-bopomofo-installer/releases)

[軟體簡介](#-軟體簡介) · [核心功能](#-核心功能) · [軟體操作畫面](#-軟體操作畫面) · [下載與使用說明](#-下載與使用說明) · [系統需求](#-系統相容性與需求) · [常見問題](#-常見問題-faq) · [問題反饋](#-問題反饋與支援)

</div>

---

## 📖 軟體簡介

「微軟舊注音（ㄅ半）」陪伴無數台灣使用者數十年，以確定性高、打字迅速、不強制自動選字等特性深受眾多使用者、程式設計師與行政文書人員喜愛。

然而自從微軟推出 **Windows 10** 與 **Windows 11** 以來：
1. 系統預設全面移除舊注音選項，僅保留微軟新注音。
2. 許多使用者手動匯入傳統登錄檔後，常遇到微軟更新後設定失效、在新版記事本 (Notepad)、Office 或瀏覽器中打不出字、選字浮框消失等 TSF 框架相容性問題。
3. 手動設定機碼步驟極為繁瑣，稍有不慎容易損毀系統語系配置。

**「微軟舊注音 (ㄅ半) 一鍵免費安裝器」** 由得翼科技 (DEI 3C) 開發，採用 Rust 與現代化 Slint GUI 框架打造，專為簡化安裝流程而設計。程式能自動識別系統架構與版本，完整配置系統註冊表（含關鍵之 Tsf3Override 機碼與 TSF TIP 註冊）、自動調用原生 API 並重新啟動輸入法架構，**無須手動重開機，一鍵立即找回微軟舊注音！**

---

## ✨ 核心功能

### 1. ⚡ 一鍵自動化極速安裝
- 自動偵測目前 Windows 版本 (Win 11 / 10 / 8.1 / 8 / 7) 與架構 (x64 / x86)。
- 自動配置系統機碼，注入關鍵 Tsf3Override 與 TSF TIP 註冊，完美相容新版 Windows 現代應用程式。
- 調用 Windows 原生 InstallLayoutOrTip API，並重啟 ctfmon.exe，安裝完畢立即可用，免重新開機！

### 2. 🔄 一鍵乾淨解除安裝
- 若日後不再需要使用，可隨時點擊「解除安裝」，一鍵還原系統乾淨設定，不殘留冗餘註冊表垃圾。

### 3. 📋 即時進度日誌與一鍵複製
- 視窗內建可視化安裝進度日誌，清楚呈現每一個系統調用步驟。
- 支援「複製日誌」功能，方便排查與技術支援。

### 4. 🔒 純淨綠色、零隱私傳輸 (100% Offline & Pure Privacy)
- 軟體完全於本地離線執行，無任何網路連線與資料傳輸功能。
- 絕不收集、側錄或上傳任何鍵盤輸入紀錄與個人隱私資料。
- 32 位元通用 PE 原生單檔（Portable），無須安裝任何 .NET 或 VC++ 依賴庫，亦可隨身放入 WinPE 維護隨身碟。

---

## 📸 軟體操作畫面

<div align="center">
  <img src="images/應用程式執行畫面.png" alt="微軟舊注音 (ㄅ半) 一鍵免費安裝器 軟體操作介面" width="720" />
</div>

---

## 📦 下載與使用說明

### 📥 下載方式
1. 前往本專案的 [Releases 頁面](https://github.com/robert820/winxp-bopomofo-installer/releases) 下載最新版 微軟舊注音 (ㄅ半) 一鍵免費安裝器.exe。
2. 本程式為**單一免安裝綠色執行檔**，下載後即可直接執行。

### 🚀 安裝操作指南
1. **以系統管理員身分執行**：由於本工具需調用 Windows 系統級輸入法 API 與配置登錄檔，請對執行檔點擊右鍵選擇「以系統管理員身分執行」。
2. **點擊「開始安裝」**：程式會自動完成作業系統偵測、機碼配置與服務喚醒，整個過程僅需 1~3 秒。
3. **切換使用**：安裝成功後，按鍵盤快速鍵（如 Ctrl + Shift 或 Win + Space）切換至「微軟舊注音 (ㄅ半)」即可開始打字！

---

## 🖥️ 系統相容性與需求

- **作業系統**：Windows 11 / Windows 10 / Windows 8.1 / Windows 8 / Windows 7 (SP1)
- **架構支援**：64 位元 (x64) 與 32 位元 (x86)
- **執行權限**：需要系統管理員權限 (Administrator)
- **環境依賴**：單一原生二進位執行檔，免安裝任何外部運行庫

---

## ❓ 常見問題 (FAQ)

<details>
<summary><b>Q1: 為什麼安裝完成後在某些新版軟體（如新版記事本或 Word）還是打不出字？</b></summary>
A: 本工具已預設配置微軟 TSF (Text Services Framework) 相容機碼與 Tsf3Override。如果在極少數系統環境仍出現選字框異常，請嘗試將該應用程式完全關閉後重新開啟，或將電腦重新開機一次以使所有背景服務完全載入。
</details>

<details>
<summary><b>Q2: 這款軟體完全免費嗎？電腦維修同業可以使用嗎？</b></summary>
A: 是的！本軟體免費提供個人、企業與電腦維修工作室使用，亦可自由放置於工程維修隨身碟中幫客戶安裝修復舊注音。但嚴禁單獨販售、出租或捆綁收費營利。
</details>

<details>
<summary><b>Q3: 為什麼防毒軟體或 Windows SmartScreen 偶爾會提示或誤報？</b></summary>
A: 本程式為使用 Rust 語言編寫的純淨工具，絕無任何惡意代碼。由於安裝輸入法必須調用 Windows 底層 API 修改系統機碼與啟動 ctfmon，部分防毒軟體啟發式引擎判定標準較為嚴格，請安心選擇「允許執行」或加入信任清單。
</details>

---

## 💬 問題反饋與支援

- 🐛 **錯誤回報與功能建議**：歡迎至本專案的 [Issues 頁面](https://github.com/robert820/winxp-bopomofo-installer/issues) 提出。
- 🌐 **得翼科技官方網站**：[https://blog.dei3c.com](https://blog.dei3c.com)

---

## 📄 授權條款 (License)

本軟體採用專有免費軟體授權（Proprietary Freeware），完整授權規範、使用條款與免責聲明請參閱 [LICENSE](LICENSE) 檔案。
