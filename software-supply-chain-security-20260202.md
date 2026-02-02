# 軟體供應鏈安全：SBOM、SSDF、SLSA（2026 更新）

供應鏈安全不是單一控制點，而是「規範（SSDF）× 透明度（SBOM）× 完整性（SLSA）」的組合。Staff 工程師需要把這三者串成可落地的交付流程，讓安全不只在審查，而是在日常交付中被驗證。

## 三層結構（定位各自角色）

1. SSDF（NIST SP 800-218）：定義安全開發的高階實務與共同語言
2. SBOM：提供組成透明度與供應鏈可追溯性
3. SLSA：提供建置與供應鏈完整性的保證等級

## 近期更新（截至 2026-02-02）

1. NIST 於 2025-12-17 釋出 SSDF 1.2 初版草案，徵求意見到 2026-01-30 為止
2. NIST SP 800-218A（AI/雙用途基礎模型）已在 2024-07-26 正式發布
3. CISA 於 2025-08-22 發布「2025 SBOM Minimum Elements」草案並徵求意見（已於 2025-10-03 結束）
4. CycloneDX 規格 1.7 於 2025-10-21 發布
5. SPDX 3.0 擴展到 AI 模型、資料集與建置資訊等供應鏈資料

## SBOM 的最小元素（NTIA 2021 基線）

1. Data Fields（元件基本資訊）
2. Automation Support（可機器化）
3. Practices and Processes（生成、交付、使用流程）

## SLSA 水準（強度與投資順序）

1. Level 1：建置可被描述與追溯
2. Level 2：建置服務具備抗竄改
3. Level 3：更強的威脅防護與不可偽造的證明
4. Level 4：最高完整性（例如雙人審查與可重現建置）

## 供應鏈工作流（示意）

```mermaid
%%{init: {'theme': 'dark'}}%%
flowchart LR
  S[Source] --> B[Build]
  B --> A[Artifact]
  A --> D[Deploy]
  S -.SSDF 實務.-> B
  B -.SLSA Provenance.-> A
  A -.SBOM.-> D
```

## Staff 工程師可以做的事

1. 把 SSDF 實務轉成團隊可執行的交付清單
2. 建立 SBOM 產出與稽核流程（格式與頻率）
3. 要求關鍵系統具備 SLSA 目標層級與可驗證證明
4. 讓採購與供應商治理對齊 SBOM/SSDF 共同語言
5. 定義「例外」流程，避免安全成為停擺的理由

## 參考資料

1. NIST SSDF 1.2 初版草案公告：https://www.nist.gov/news-events/news/2025/12/secure-software-development-framework-ssdf-version-12-available-public
2. NIST SP 800-218 Rev.1 初版草案：https://csrc.nist.gov/pubs/sp/800/218/r1/ipd
3. NIST SP 800-218A（AI 社群檔）：https://www.nist.gov/news-events/news/2024/07/secure-software-development-practices-generative-ai-and-dual-use-foundation
4. NIST SBOM 定義（EO 14028）：https://www.nist.gov/itl/executive-order-14028-improving-nations-cybersecurity/software-security-supply-chains-software-1
5. NTIA SBOM Minimum Elements：https://www.ntia.gov/report/2021/minimum-elements-software-bill-materials-sbom
6. CISA 2025 SBOM Minimum Elements 草案：https://www.cisa.gov/resources-tools/resources/2025-minimum-elements-software-bill-materials-sbom
7. SLSA 介紹：https://slsa.dev/
8. SPDX 3.0 概覽：https://spdx.dev/learn
9. CycloneDX Spec Overview：https://cyclonedx.org/specification/overview

