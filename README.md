# 🐾 MiMoPetName

### AI Pet Naming Advisor — Powered by Xiaomi MiMo V2.5

Describe your pet's personality and appearance. Get 10 names with meaning, origin, and vibes — tailored to who they are.

[![Live Demo](https://img.shields.io/badge/Live-Demo-000?style=for-the-badge&logo=github)](https://gyoomei.github.io/mimopetname/)
[![Try Now](https://img.shields.io/badge/Try-Now-f472b6?style=for-the-badge&logo=googlechrome)](https://gyoomei.github.io/mimopetname/)
[![AI](https://img.shields.io/badge/AI-Xiaomi%20MiMo%20V2.5-f97316?style=for-the-badge)](https://huggingface.co/XiaomiMiMo)
[![Pets](https://img.shields.io/badge/Pets-8%20Types-a78bfa?style=for-the-badge)](#supported-pets)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

---

## 📖 The Problem

You just got a pet. Everyone asks "what's their name?" and you freeze. Google "cat names" gives you the same 20 generic lists: Luna, Milo, Bella, Charlie. None of them capture that your cat is a grey fluffball who sleeps 18 hours a day and is terrified of cucumbers.

**MiMoPetName fixes that.** Describe your pet — their looks, quirks, personality. MiMo V2.5 generates names from across world cultures, each with meaning that connects to who your pet actually is.

---

## ✨ How it works

```
You describe: 🐱 Cat · Grey fur, shy but loves cuddles,
              sleeps 18 hours, scared of cucumbers

MiMo writes:  1. HAZE — English · "Like morning fog, soft
              and quiet, always drifting back to sleep."
              vibes: cozy · dreamy · gentle

              2. NAMI (波) — Japanese · "Wave — moves in
              gentle rhythms, always finding the warmest spot."
              vibes: serene · elegant · sleepy

              3. PHANTOM — English · "Appears silently,
              disappears mysteriously — classic grey cat energy."
              vibes: mysterious · playful · sneaky
```

**That's the entire UX** — describe, discover, name, love.

---

## 🎯 Core Features

| Capability | Detail |
|---|---|
| 🐾 **8 Pet Types** | Cat, Dog, Bird, Fish, Rabbit, Hamster, Turtle, Other |
| 🌍 **Multi-Cultural Names** | Japanese, Greek, Norse, Arabic, Indonesian, Celtic, Latin, Sanskrit |
| 🎨 **5 Style Filters** | Cute, Cool, Funny, Elegant, Mythology |
| 📖 **Meaning & Origin** | Every name comes with cultural origin and why it fits |
| 🏷️ **Vibe Tags** | 2-3 vibes per name (cozy, mysterious, playful, regal...) |
| ☁️ **Name Cloud** | Canvas visualization of generated names |
| 📋 **Click to Copy** | Copy individual names or all at once |
| 💬 **Ask MiMo** | Chat about name origins, meanings, and naming tips |
| 📖 **History** | Save up to 20 naming sessions |
| 🌗 **Dark/Light Mode** | Pink accent, WCAG-AA |
| 🌐 **Bilingual EN/ID** | Full Indonesian + English |
| 📱 **Mobile Responsive** | Fluid from 375px to 1920px |

---

## 🐾 Supported Pets

| Pet | Icon | Name Examples |
|---|---|---|
| 🐱 Cat | Felis catus | Haze, Nami, Phantom, Misty |
| 🐶 Dog | Canis lupus | Atlas, Zara, Bear, Luna |
| 🐦 Bird | Aves | Kira, Phoenix, Echo, Skye |
| 🐟 Fish | Pisces | Neptune, Ripple, Kai, Azure |
| 🐰 Rabbit | Oryctolagus | Mochi, Clover, Thumper, Sage |
| 🐹 Hamster | Cricetinae | Peanut, Biscuit, Nugget, Bean |
| 🐢 Turtle | Testudines | Sheldon, Yoda, Atlas, Jade |
| 🌍 Other | Any animal | Custom-adapted to any species |

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────┐
│  Input: Pet type + personality + appearance + style          │
│                          ↓                                   │
│  Prompt Builder           →  pet-specific naming prompt      │
│  (8 pet types + 5 styles)    with trait extraction           │
│                          ↓                                   │
│  MiMo V2.5 (Pollinations.ai) → 10 names with metadata       │
│                               origin, meaning, vibes         │
│                          ↓                                   │
│  Name Cloud (Canvas 2D)   →  visual name arrangement         │
│  Name Cards               →  click-to-copy with metadata    │
│                          ↓                                   │
│  Chat (Pollinations.ai)   →  naming advice + origins         │
│  History (localStorage)   →  save sessions                   │
└─────────────────────────────────────────────────────────────┘
```

**Zero backend.** Everything runs client-side. No API key. No tracking.

---

## 💡 Architecture Decisions

**Why personality-based instead of appearance-only?**
A grey cat could be "Shadow" (mysterious) or "Cloud" (soft) or "Gandalf" (wise). Personality determines which name resonates. "Sleeps 18 hours" + "shy" → dreamy, gentle names. "Energetic" + "destroyed the couch" → mischievous, bold names.

**Why multi-cultural names?**
The best pet names come from diverse languages. Japanese for elegance (Nami, Kaze), Greek for mythology (Atlas, Nyx), Norse for strength (Freya, Loki), Arabic for beauty (Layla, Amir). Limiting to English names limits creativity.

**Why a name cloud?**
Seeing names arranged visually helps you feel which one fits — it's an emotional decision, not a logical one. The cloud creates a "mood board" effect that makes the choice feel right.

---

## 🧪 Try these examples

| Pet | Description | Expected Names |
|---|---|---|
| 🐱 Grey cat, shy, sleeps 18h | Gentle, dreamy | Haze, Nami, Phantom, Mist |
| 🐶 Husky, energetic, destroys toys | Bold, mischievous | Loki, Atlas, Storm, Ragnar |
| 🐱 Orange tabby, loves food, lazy | Funny, cozy | Mochi, Cheddar, Biscuit, Pumpkin |
| 🐶 Small poodle, elegant, prissy | Elegant, regal | Duchess, Coco, Pearl, Empress |
| 🐢 Old turtle, wise, slow | Mythology, timeless | Yoda, Sheldon, Athena, Sage |

---

## 🛠️ Stack

- **Frontend:** Vanilla JavaScript, single HTML file (~31KB)
- **AI:** [Xiaomi MiMo V2.5](https://github.com/XiaomiMiMo) via [Pollinations.ai](https://text.pollinations.ai/) — free, no API key
- **Fonts:** [Sora](https://fonts.google.com/specimen/Sora) + [Nunito](https://fonts.google.com/specimen/Nunito) + [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono)
- **Storage:** localStorage for history
- **Hosting:** GitHub Pages (zero infra cost)

---

## 🚀 Quick Start

```bash
git clone https://github.com/gyoomei/mimopetname.git
cd mimopetname
python3 -m http.server 8080
# Open http://localhost:8080
```

Or just visit the [live demo](https://gyoomei.github.io/mimopetname/).

---

## 📄 License

MIT — name your pet, share the love.

---

**Built with 🧠 [Xiaomi MiMo V2.5](https://github.com/XiaomiMiMo) · Submitted to the [Xiaomi MiMo 100T program](https://100t.xiaomimimo.com/)**
