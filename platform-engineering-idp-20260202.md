# 平台工程與內部開發平台（IDP）（2026 更新）

CNCF 平台工程白皮書把「平台」定義為一個為內部使用者打造的產品，核心目標是降低認知負荷、提供自助式能力，並以「鋪好的路（golden paths）」加速交付。平台工程關注的是組織內部供應鏈的品質，而不是把每支團隊變成基礎設施專家。

## 核心觀念

1. 平台是產品，不是專案
2. 以自助式為預設，減少跨團隊等待
3. 用「可組合的能力」取代一次性客製
4. 以 golden paths 降低認知負荷與錯誤率
5. 把安全性內建為預設，而不是最後的檢查

## 成熟度（白皮書五層）

1. 自助式內部服務
2. 自助式 CI/CD Pipeline
3. 自助式基礎設施
4. 自助式內部開發平台（IDP）
5. 自助式 PaaS

## 平台價值鏈（示意）

```mermaid
%%{init: {'theme': 'dark'}}%%
flowchart LR
  PT[平台團隊] --> Cap[能力組合與基礎元件]
  Cap --> GP[Golden Paths]
  GP --> Dev[產品/服務團隊]
  Dev --> Value[更快、更安全的交付]
```

## Staff 工程師可以扮演的角色

1. 把跨團隊的痛點整理成平台需求
2. 設計「可採用」而不是「可擴充」的介面
3. 建立 golden paths 的驗證與量測機制
4. 建立平台治理（何時自助、何時升級）
5. 用 DevEx 指標追蹤平台成效

## 避免的陷阱

1. 平台只提供基礎設施，沒有可採用路徑
2. 平台沒有用戶研究，功能堆疊但沒人用
3. 平台把規範當成門檻，而不是護欄

## 參考資料

1. CNCF Platforms White Paper：https://tag-app-delivery.cncf.io/whitepapers/platforms/
2. CNCF Platform Engineering TCG：https://tag-app-delivery.cncf.io/working-groups/platforms/

