# 專案說明文件存放規範

## 📋 規範目的

本規範定義與專案有關的說明文件（README、draw.io、架構圖、流程圖等）的統一存放位置和結構，確保文件管理的一致性和可維護性。

## 📁 檔案結構規範

### 標準結構

每個專案都必須遵循以下結構：

```
{專案名稱}/
├── Docs/                          # 專案說明文件資料夾（統一存放所有文件）
│   ├── README.md                  # 專案主要說明文件
│   ├── Diagrams/                  # 架構圖和流程圖資料夾
│   │   └── *.drawio
│   └── {其他說明文件}.md          # 其他專案相關說明文件
└── {其他專案檔案}/
```

### 範例

#### BoardingPass.Contracts
```
BoardingPass.Contracts/
├── Docs/
│   ├── README.md
│   └── Diagrams/
│       └── BoardingPass_Architecture.drawio
```

#### BoardingPass.GoogleWallet
```
BoardingPass.GoogleWallet/
├── Docs/
│   ├── README.md
│   └── Diagrams/
│       └── GoogleWallet_ExecutionFlow.drawio
```

#### BoardingPass.AppleWallet
```
BoardingPass.AppleWallet/
├── Docs/
│   ├── README.md
│   └── Diagrams/
│       ├── AppleWallet_ExecutionFlow.drawio
│       ├── AppleWalletWebService_Architecture.drawio
│       └── AppleWalletWebService_Flow.drawio
```

## 📝 檔案命名規範

### README 檔案
- **位置**：`{專案名稱}/Docs/README.md`
- **命名**：固定為 `README.md`
- **內容**：專案的主要說明文件，包含：
  - 專案目的
  - 專案結構
  - 使用方式
  - 核心元件說明
  - 依賴關係
  - 設計原則

### Draw.io 檔案
- **位置**：`{專案名稱}/Docs/Diagrams/`
- **命名規則**：使用專案or架構or流程or功能or服務 的描述性名稱，使用大寫字母和底線
- **範例**：
  - `BoardingPass_Architecture.drawio`
  - `GoogleWallet_ExecutionFlow.drawio`
  - `AppleWalletWebService_Architecture.drawio`

### 其他說明文件
- **位置**：`{專案名稱}/Docs/`
- **命名規則**：使用描述性名稱，使用大寫字母和底線
- **範例**：
  - `API_DOCUMENTATION.md`
  - `DEPLOYMENT_GUIDE.md`
  - `TROUBLESHOOTING.md`

## ✅ 必須遵守的規則

### 1. 統一存放位置
- ✅ **所有說明文件**必須存放在 `{專案名稱}/Docs/` 資料夾下
- ✅ **所有 draw.io 檔案**必須存放在 `{專案名稱}/Docs/Diagrams/` 資料夾下
- ❌ **禁止**在專案根目錄或其他位置建立 Diagrams 資料夾
- ❌ **禁止**將說明文件散落在專案各處

### 2. 資料夾結構(如有需要時才建立對應的檔案)
- ✅ 每個專案**非必須**有 `Docs/` 資料夾
- ✅ 每個專案**非必須**有 `Docs/Diagrams/` 資料夾（即使暫時沒有圖表）
- ✅ 每個專案**非必須**有 `Docs/README.md` 檔案

### 3. 檔案引用
- ✅ 在 README 中引用圖表時，使用相對路徑：`[Diagrams/{檔案名稱}.drawio](./Diagrams/{檔案名稱}.drawio)`
- ✅ 在根目錄的總 README 中引用時，使用完整路徑：`{專案名稱}/Docs/Diagrams/{檔案名稱}.drawio`

### 4. 舊檔案清理
- ✅ 移動檔案到新位置後，**必須刪除**舊的 Diagrams 資料夾
- ✅ 合併重複檔案時，保留最新版本，刪除舊版本

## 🔄 遷移檢查清單

當需要遷移或整理文件時，請確認：

- [ ] 檢查專案根目錄是否有舊的 `Diagrams/` 資料夾
- [ ] 檢查是否有 draw.io 檔案散落在其他位置
- [ ] 將所有 draw.io 檔案移動到 `Docs/Diagrams/` 資料夾
- [ ] 確保 `Docs/README.md` 存在且內容完整
- [ ] 更新所有文件中的引用路徑
- [ ] 刪除舊的 Diagrams 資料夾（如果存在）
- [ ] 確認檔案結構符合規範

## 📌 適用範圍

本規範適用於以下專案：
- ✅ `BoardingPass.Contracts`
- ✅ `BoardingPass.GoogleWallet`
- ✅ `BoardingPass.AppleWallet`
- ✅ 未來新增的所有專案

## 🎯 規範目標

1. **一致性**：所有專案使用相同的文件結構
2. **可維護性**：文件集中管理，易於查找和更新
3. **清晰性**：明確的命名規則和存放位置
4. **完整性**：確保所有專案都有完整的說明文件

---

**最後更新日期**：2025-12-15  
**維護者**：開發團隊

