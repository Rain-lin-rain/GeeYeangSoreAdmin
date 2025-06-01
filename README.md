# 租屋平台專案

## 專案概述

這是一個使用前後端分離架構開發的租屋平台系統，提供房客和房東之間的租屋媒合服務。

## 技術架構

### 前端技術

- 開發工具：Visual Studio Code
- 框架：Vue 3（元件型架構）
- 狀態管理：Pinia
- 環境配置：使用 .env 檔案管理 API 路由
  - API 基礎路徑：`https://localhost:7022`

### 後端技術

- 框架：ASP.NET MVC Core
- 資料儲存：Session 管理
- API 設計：RESTful API

## 專案結構

### 後端架構

後端採用模組化的設計，主要包含以下部分：

#### API 控制器

1. **AuthController.cs**

   - 位置：`GeeYeangSore/APIControllers/Auth/AuthController.cs`
   - 功能：處理前台房客的登入與登出
   - 主要職責：
     - 帳號驗證
     - Session 設定與清除
     - 使用者資訊管理

2. **SessionManager.cs**

   - 位置：`GeeYeangSore/APIControllers/Session/SessionManager.cs`
   - 功能：統一管理 Session 欄位存取
   - 主要職責：
     - Session Key 的存取管理
     - Session 資料的清除

3. **BaseController.cs**
   - 位置：`GeeYeangSore/APIControllers/BaseController.cs`
   - 功能：共用基底控制器
   - 主要職責：
     - 會員身分管理
     - 權限控制
     - 登入狀態判斷
     - 房東/黑名單狀態管理

### 資料傳輸

- 使用 DTO（Data Transfer Object）模式
- 依功能分類（Response/Request）建立獨立的 DTO 檔案

## 開發環境設置

### 前端設置

1. 安裝 Node.js 和 npm
2. 安裝 Vue 3 相關依賴
3. 配置 .env 檔案
4. 啟動開發伺服器

### 後端設置

1. 安裝 .NET SDK
2. 還原 NuGet 套件
3. 設定資料庫連接
4. 啟動 API 伺服器

## 系統需求

- Node.js 16.0 或以上
- .NET 6.0 或以上
- Visual Studio Code
- Visual Studio 2022（後端開發）
