<p align="center">
 <img src="../../logo.png" alt="i-have-adhd" width="140" />
</p>
<p align="center">
 <strong align="center">對 ADHD 友善的輸出。無需確診 ADHD！ </strong>
</p>
<p align="center">
 <a href="../../LICENSE"><img src="https://img.shields.io/github/license/ayghri/i-have-adhd?style=flat" alt="許可證"></a>
</p>

<p align="center">
 <a href="../../README.md" title="English" aria-label="English">🇬🇧</a> ·
 <strong title="簡體中文" aria-label="簡體中文">🇨🇳</strong> ·
 <a href="README.id.md" title="Bahasa Indonesia" aria-label="Bahasa Indonesia">🇮🇩</a> ·
 <a href="README.pt-BR.md" title="Português (Brasil)" aria-label="Português (Brasil)">🇧🇷</a> ·
 <a href="README.ja.md" title="日本語" aria-label="日本語">🇯🇵</a> ·
 <a href="README.vi.md" title="Tiếng Việt" aria-label="Tiếng Việt">🇻🇳</a> ·
 <a href="README.ko.md" title="한국어" aria-label="한국어">🇰🇷</a> ·
 <a href="README.fa.md" title="فارسی" aria-label="فارسی">🇮🇷</a> ·
 <a href="README.th.md" title="ภาษาไทย" aria-label="ภาษาไทย">🇹🇭</a> ·
 <a href="README.ar.md" title="العربية" aria-label="العربية">🇸🇦</a> ·
 <a href="README.fr.md" title="Français" aria-label="Français">🇫🇷</a>
</p>


## 安裝

複製並貼上到你的 CLI 對話框中：

```text
Install the i-have-adhd skill/plugin from https://github.com/YU-XIANG-0925/i-have-adhd, refer to the repo's AGENTS.md for instructions.
```

或 🔗 [查看安裝說明](../install/INSTALL.zh-CN.md)

## 功能

一個給程式設計助手的技能，讓它別把答案埋進長篇大論。行動優先。步驟編號。不說“希望這能幫到你！”


## 有什麼變化


<table>
<tr>
<td width="50%">

## 之前

> 問得好！讓我想一想。你的身分驗證流程包含幾個環節：中間件、令牌驗證和 Cookie 處理。在查看 `src/auth.ts` 後，`verifyToken` 函數（大約第 42–58 行）似乎使用了舊版 `jsonwebtoken` API。一種做法是升級這個套件並重寫該函數。完成修改後，你需要執行身份驗證測試，確認沒有破壞任何功能。順便一提，你可能還想整體檢查一下依賴版本。希望這能幫到你！如果你想進一步研究，請告訴我。

</td>

<td width="50%">

## 之後

> 編輯 `src/auth.ts:42`，更新令牌驗證邏輯。
>
> 1. 開啟 `src/auth.ts`
> 2. 將 `verifyToken`（第 42–58 行）替換為下面的程式碼片段
> 3. 運行 `npm test -- auth.spec.ts`
>
> 下一步：如果有測試失敗，請貼上第一行報錯。

</td>
</tr>
</table>


## 規則

共 10 條規則。完整內容請見 [SKILL.md](../../skills/i-have-adhd/SKILL.md)。

1. 先說下一步行動。
2. 多步驟任務使用編號。
3. 以具體的下一步收尾。
4. 抑制離題內容。
5. 每輪重述目前狀態。
6. 給出具體的時間估計（以分鐘計，不說「一會兒」）。
7. 讓完成的工作看得見。
8. 就事論事地報告錯誤。
9. 每個清單最多 5 項。
10. 不寫開場白、回顧或結束語。

## 自訂

Fork 此倉庫，編輯 `skills/i-have-adhd/SKILL.md`，然後換成你的副本：

『`bash
claude plugin uninstall i-have-adhd # 先移除上游副本：
claude plugin marketplace remove i-have-adhd # fork 與上游使用相同名稱
claude plugin marketplace add <your-username>/i-have-adhd
claude plugin install i-have-adhd@i-have-adhd
```

重啟 Claude Code，然後再次呼叫 `/i-have-adhd`。

## 致謝

內容大致參考 J. Russell Ramsay 和 Anthony L. Rostain 所寫的 *The Adult ADHD Tool Kit*。本技能針對 LLM 應如何回應進行了改編，而不是教導人們如何安排日常生活。

## 許可證

[MIT](../../LICENSE)。

如果它幫你省下一次滾動、少看一句“問得好！”，請點個 Star ⭐
