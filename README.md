# scrust

**scrust** 是一個基於 Rust 語言的 SDK，用於與 [scrapyd](https://github.com/scrapy/scrapyd) 進行交互。此專案使用 [pyo3](https://pyo3.rs/) 編寫，並透過 [maturin](https://github.com/PyO3/maturin) (版本要求 `>=1.8,<2.0`) 編譯，利用 `abi3-py38` 實現與 Python 3.8 及更高版本的兼容性。

---

## 目錄

- [簡介](#簡介)
- [特性](#特性)
- [安裝要求](#安裝要求)
- [安裝指南](#安裝指南)
- [開發與貢獻](#開發與貢獻)
- [常見問題](#常見問題)
- [授權條款](#授權條款)
- [聯繫方式](#聯繫方式)

---

## 簡介

在現今的項目中，使用 Rust 能夠獲得更高的性能和內存安全，而 pyo3 讓我們能夠輕鬆地把 Rust 的高效功能帶給 Python 開發者。**scrust** 作為 scrapyd 的 SDK，使得 Python 用戶可以方便地調用 scrapyd 的 API 來管理分布式爬蟲任務，無論是啟動、停止還是監控任務執行情況，都能夠簡化操作流程並提升效能。

---

## 特性

- **高性能**：利用 Rust 的執行速度和內存安全特性，提供穩定的後端支援。
- **Python 兼容**：基於 pyo3 與 `abi3-py38` 實現，確保與 Python 3.8 及以上版本的廣泛兼容。
- **成熟穩定的編譯工具**：使用 maturin (版本 `>=1.8,<2.0`) 進行編譯和打包，確保項目在各平台的穩定性。
- **簡單易用的 API**：提供一系列精心設計的函數，幫助用戶輕鬆操作 scrapyd 的各項服務。
- **擴展性**：模組化設計，方便後續功能擴展與自定義修改。

---

## 安裝要求

在開始使用 scrust 前，請確保系統中已安裝以下組件：

- **Rust 編譯環境**：請安裝最新穩定版本的 Rust。
- **maturin**：版本要求 `>=1.8` 且 `<2.0`。參考 [maturin 安裝說明](https://github.com/PyO3/maturin)。
- **Python**：Python 3.8 或更高版本（基於 `abi3-py38` 實現）。

---

## 安裝指南

### 從 PyPI 安裝

當你的專案已發布到 PyPI 後，可以通過 pip 安裝：

```bash
pip install scrust
```

### 從源碼構建

如果需要從源碼構建或參與開發，請按照以下步驟操作：

1. **克隆項目代碼**

   ```bash
   git clone https://github.com/OxideZoo/scrust.git
   cd scrust
   ```

2. **安裝 maturin**

   可以通過 pip 或使用 Rust 的包管理工具安裝 maturin（請確認版本範圍 `>=1.8,<2.0`）：

   ```bash
   pip install maturin==1.8.0  # 或者其他符合要求的版本
   ```

3. **構建並測試**

   使用 maturin 進行構建及安裝：

   ```bash
   maturin develop
   ```

   如果你希望生成二進制輪子（wheel）包，則可使用：

   ```bash
   maturin build --release
   ```

---

## 開發與貢獻

我們歡迎各界開發者參與 scrust 的開發工作！如果你對此專案有建議或者想要貢獻代碼，請參考以下指南：

1. **Fork 並克隆代碼庫**

2. **創建一個新的分支**：為你的功能或修正創建獨立分支

   ```bash
   git checkout -b feature/my-new-feature
   ```

3. **提交你的修改**：請撰寫清晰的提交信息

   ```bash
   git commit -m "feat: 新增功能描述"
   ```

4. **推送至你的 Fork 並提交 Pull Request**

5. **編寫或更新測試用例**：確保新功能或修正不會破壞現有功能

---

## 常見問題

### 問：如何確保 scrust 能正確與 scrapyd 進行交互？

答：請確認 scrapyd 的 URL 配置正確，並檢查服務狀態。同時，請參考 [scrapyd 官方文檔](https://scrapyd.readthedocs.io/) 確認你對 scrapyd 配置和運行的要求。

### 問：編譯過程中出現錯誤，我該如何排查？

答：請確認你的系統中安裝了最新版本的 Rust 編譯器、符合版本要求的 maturin 以及相應的 Python 版本。另外，可以參考 [maturin 官方文檔](https://github.com/PyO3/maturin) 獲取更多診斷信息。

---

## 授權條款

本項目採用 [MIT License](./LICENSE) 開源授權協議。詳細條款請參閱 [LICENSE](./LICENSE) 文件。

---

## 聯繫方式

如果你有任何疑問、反饋或者建議，歡迎通過以下方式與我們取得聯繫：

- GitHub Issues: [https://github.com/OxideZoo/scrust/issues](https://github.com/OxideZoo/scrust/issues)
- 郵件：your.email@example.com

---

感謝你對 **scrust** 的關注與支持！希望這個項目能夠幫助你更高效地與 scrapyd 進行交互，享受 Rust 和 Python 帶來的性能與便捷。

---