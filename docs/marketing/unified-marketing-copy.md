# Kiword 统一营销文案指导（Unified Marketing Copy Guide）

> 版本：v1.2 · 2026-09-28
> 适用范围：Product Hunt、官网 Banner、站内 CTA、Discord、邮件、社交媒体私信
> 维护原则：**全渠道使用同一记忆点，一字不差**。如需修改，先改本文档，再同步代码与渠道。

---

## 1. 产品定位（Positioning）

| 项目 | 内容 |
|---|---|
| 一句话定位 | One private AI voice app for the whole family |
| 核心功能 1 | AI Dictation（实时语音听写） |
| 核心功能 2 | AI Translation（实时翻译） |
| 双模式 | **Kids Mode**（作业引导，不代写）+ **Work Mode**（职场听写/翻译） |
| 技术差异点 | On-device local LLM（Tauri + 本地模型），语音与数据留在设备上 |
| 标准定价 | 年度订阅三档：Solo `$9.9/year`（1 个孩子档案）、Family `$25.9/year`（最多 3 个）、Max `$35.9/year`（最多 5 个） |
| 商业钩子 | Founders 首发限时：任选档位 `Buy 1 year, get 3 years` |

### 三大铁律（所有文案必须遵守）

1. **品牌名永远是 `Kiword`**，禁止 `KiWord` / `KiWord.ai` 等变体。
2. **所有面向用户的文案一律 en-US**（北美拼写：`organize` 而非 `organise`，`color` 而非 `colour`）。
3. **三个核心形容词统一用**：`private` / `on-device` / `local LLM`。不要混用 `offline`、`no-cloud`、`self-hosted` 等近义表达。

---

## 2. 统一记忆点（Master Tagline）

> **AI dictation & translation for kids and parents. One app.**

（57 字符，符合 Product Hunt Tagline 长度限制）

### 使用位置对照表

| 渠道 | 用法 |
|---|---|
| Product Hunt Tagline | 原句直接使用 |
| 站内 Launch Banner | `Kiword — AI dictation & translation for kids and parents. One app.` |
| Discord 公告首行 | 原句 + PH 链接 |
| 邮件 Preview Text | 原句 |
| X/Twitter Bio 置顶 | 原句 |
| 评论区/回帖签名 | 原句 |

> ⚠️ 禁止在 Tagline 场景替换为其他句式（如 "Kids dictate homework..."）。对比句式仅允许用于 Maker Comment 正文和长文案中作为补充叙事。

---

## 3. Product Hunt 页面文案包

### 3.1 Tagline

```
AI dictation & translation for kids and parents. One app.
```

### 3.2 Product Description（Edit Product → Description）

```
Kiword is a private, on-device AI voice app with two modes for the whole family.

🎙️ Kids Mode — built for schoolwork
Kids dictate homework and essays out loud, and Kiword turns their speech into
guided outlines — never ghost-written text. Writing practice stays the point.

💼 Work Mode — built for professionals
Parents get fast dictation and real-time AI translation for emails, notes, and
multilingual meetings. Everything stays on the device.

🔒 Why local matters
Kiword runs a local LLM on-device, so your voice and data stay on your device.
One annual plan covers the whole household.

Solo is $9.9/year, Family is $25.9/year, and Max is $35.9/year. For the launch,
Founders buy 1 year and get 3 years on any plan. When that 3-year access ends,
your plan renews at its standard annual price.

Two modes. Two core engines (AI Dictation + AI Translation). One app.
```

### 3.3 Maker Comment（发布后立即以 Maker 账号发出）

```
Hi PH! I'm Kevin Cheng, maker of Kiword.

This started with my own kid: homework thoughts came faster than typing could keep
up, and every cloud AI tool either charged a monthly subscription — or happily
wrote the essay for them. Both felt wrong.

At the same time, I needed a fast, private dictation tool for my own work. So
instead of two apps, we built one with two modes:

1. 🎙️ Kids Mode — real-time dictation with guided outlines. Kids speak their
   ideas, Kiword structures them, but never writes the final text for them.
   Homework practice stays honest.

2. 💼 Work Mode — professional dictation plus real-time AI translation for
   emails, meeting notes, and multilingual calls.

3. 🔒 Everything runs locally (Tauri + local LLM). Your voice and data stay on
   your device. Plans start at $9.9/year (Solo); Family and Max cover more
   child profiles — one purchase for the whole household.

For the launch, Founders buy 1 year and get 3 years on any plan. When that
3-year access ends, your plan renews at its standard annual price. Try both
modes, and tell me which one your family uses more — genuinely curious 🙏
```

> 注：Maker Comment 中 "Kevin Cheng" 按实际 Maker 署名替换。

### 3.4 Tags

**必加**：`AI Dictation Apps`、`Translation`、`Education`、`Productivity`、`Voice Assistants`、`Privacy`

**移除**：`Artificial Intelligence`（过泛，把位置留给精准标签）

### 3.5 Gallery 配图顺序（4 张）

1. 分屏对比：左 **Kids Mode**（作业场景）右 **Work Mode**（会议/邮件场景）
2. 听写实时转文字界面（突出即时反馈）
3. AI Translation 双语对照界面
4. 隐私图：`Your voice never leaves this device.` + 本地 LLM 架构示意

---

## 4. 站内文案（与代码一致，改动需同步代码）

### 4.1 全站 Launch Banner

组件：`src/components/ProductHuntLaunchBanner.tsx`

```
NEW
Kiword — AI dictation & translation for kids and parents. One app.
{N} days left to upvote us on Product Hunt — one private, on-device app for the whole family.
[Upvote] [Review]
```

### 4.2 Feedback 提交成功 CTA 卡片

组件：`src/pages/Feedback.tsx`

```
标题：We just launched Kiword on Product Hunt 🚀
正文：Since you already took the time to share feedback with us — we'd really appreciate
an honest upvote or a 1-sentence review over on Product Hunt.
Kiword pairs AI dictation with AI translation across Kids and Work modes,
so one private, on-device app serves the whole family.
Every real review helps more families find it.
按钮：[Upvote on Product Hunt] [Leave a review]
```

### 4.3 邮件 Footer CTA（feedback 通知邮件，活动期内自动显示）

模板：`api/feedback/notify.js`

```
🚀 We're live on Product Hunt!
Kiword — private, on-device AI dictation & translation for kids and parents —
just launched on Product Hunt. If you find Kiword useful, an upvote or honest
review from you would mean the world.
[Upvote on Product Hunt] [Leave a review]
```

---

## 5. Discord 公告模板（Founders Club → #announcements）

```
@everyone

🚀 We just launched Kiword on Product Hunt!

AI dictation & translation for kids and parents. One app.

👉 Show your support: {PRODUCT_HUNT_URL}

How you can help (takes 2 minutes):
1️⃣ Try Kiword for 5 minutes first — real usage makes your vote count more
2️⃣ Upvote the launch page
3️⃣ Leave a 1-sentence honest review about how you'd use it

🎁 Launch perk: buy 1 year, get 3 years on any plan for early Founders
(Solo $9.9, Family $25.9, Max $35.9). When that 3-year access ends, your plan
renews at its standard annual price.

Every real review helps more families discover a private, on-device alternative
to cloud AI writing tools. Thank you! 🙏
```

---

## 6. Launch Email 模板（邮件列表全量发送）

```
Subject:   We just launched Kiword on Product Hunt 🚀
Preview:   AI dictation & translation for kids and parents. One app.

Hi {first_name},

Today is the day — Kiword is live on Product Hunt.

Kids Mode turns spoken homework thoughts into guided outlines (never ghost-written
essays). Work Mode gives you fast dictation and real-time translation for emails
and meetings. All of it runs locally on your device, so your voice and data stay
on your device.

🎁 Launch special: buy 1 year, get 3 years on any plan, exclusive to early
Founders (Solo $9.9, Family $25.9, Max $35.9). When that 3-year access ends,
your plan renews at its standard annual price.

[Upvote Kiword on Product Hunt →]

Even one sentence of honest feedback on the launch page makes a huge difference
for a small team like ours.

Thank you for being here early.

Kevin Cheng
Maker of Kiword
```

---

## 7. 一对一私信模板（用户/朋友个性化召回）

> 使用规则：必须个性化首行（提及对方实际情况），禁止无差别群发。

```
Hey {name}!

We just soft-launched Kiword on Product Hunt — the AI dictation & translation
app we've been building ({personalized line: e.g. "the one I showed you for my
kid's homework"}).

Right now we need ~50 real user upvotes to unlock Product Hunt's recommendation
flow. If you've tried Kiword and found it useful, could you:
1) Upvote here → {PRODUCT_HUNT_URL}
2) Leave a 1-sentence review of what you'd use it for

No pressure if it's not for you 🙏
```

---

## 8. 渠道执行清单（按优先级）

| # | 动作 | 时点 | 状态 |
|---|---|---|---|
| 1 | PH 页面：按第 3 节更新 Tagline / Description / Maker Comment / Tags / Gallery | 立即 | ☐ |
| 2 | PH 页面补充社交链接（Discord 邀请、LinkedIn、GitHub） | 立即 | ☐ |
| 3 | Discord #announcements 发第 5 节公告 | 24h 内 | ☐ |
| 4 | 发送第 6 节 Launch Email | 24–48h 内 | ☐ |
| 5 | 一对一私信 10–20 位真实用户（第 7 节模板） | 48h 内 | ☐ |
| 6 | Reviews ≥ 10 且 Upvotes ≥ 50 后，准备 Relaunch（如 "Kiword 1.1 — Homework Mode with Local Translation"） | 1–2 周 | ☐ |

### Relaunch 前检查项

- [ ] 定位文案已按本文档更新且全渠道一致
- [ ] 站内 Banner / Feedback CTA / 邮件 footer 处于激活状态（活动窗口见 `src/config/productHunt.ts`）
- [ ] 新增 10+ 真实 Reviews
- [ ] Gallery 配图与双模式定位匹配

---

## 9. 活动窗口配置

| 配置 | 位置 | 默认值 |
|---|---|---|
| 前端活动截止 | `src/config/productHunt.ts` → `DEFAULT_CAMPAIGN_END`（可用 `VITE_PRODUCT_HUNT_BANNER_END` 覆盖） | 2026-10-03T23:59:59-04:00 |
| 后端邮件活动截止 | `api/feedback/notify.js` → `getProductHuntConfig()`（可用 `PRODUCT_HUNT_BANNER_END` 覆盖） | 同上 |
| PH 链接 | `PRODUCT_HUNT_PRODUCT_URL`（前端）/ `PRODUCT_HUNT_PRODUCT_URL`（后端 env） | `https://www.producthunt.com/products/kiword-voice-to-text-translation` |

活动结束后：Banner 与邮件 footer CTA 自动隐藏，无需改代码；如需延期，仅更新上述环境变量即可。

---

## 10. 禁用表达清单

| 禁用 | 原因 | 替换为 |
|---|---|---|
| `KiWord` | 品牌大小写错误 | `Kiword` |
| `AI writing coach for kids`（单独使用） | 旧定位残留，与双核心不符 | `AI dictation & translation for kids and parents` |
| `ghost-writer` / `writes essays for you` | 与"不代写"价值观冲突 | `guided outlines, never ghost-written` |
| `offline AI` / `no-cloud` | 非统一术语 | `on-device` / `local LLM` |
| 英式拼写（`colour`、`organise`） | 违反 en-US 规范 | 北美拼写 |
