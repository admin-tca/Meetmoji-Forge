# 🧿 Meetmoji Forge  
**The Ritual Calendar Crafter — Where Time Meets Glyph**  
*...and where your visual processing cortex takes over from your guilt-ridden monkey mind!*

---

## 📖 What is Meetmoji Forge?

**Meetmoji Forge** is a handcrafted calendaring ritual tool that generates .ics files for your academic year — complete with phase-based planning blocks and visually anchored, emoji-coded meeting slots.

It is not a generic scheduling app.  
It is a **semantic and cognitive system**, built from first principles to reduce scheduling fatigue, promote rhythm, and enable high-coherence collaboration across global time zones.

You don't schedule meetings with numbers or guilt.  
You schedule meetings by asking:  
**“What emoji are you today?”** 🐝🦊🌀🌿

---

## 🎯 Why This Exists

Traditional calendar systems are designed for corporate compliance — not creative clarity.  
Their UX treats your mind like a command-line buffer: linear, overloaded, guilt-prone.

But human cognition isn’t built like that.  
It’s *spatial*. *symbolic*. *visually driven*.

So we rebuilt scheduling:

- Using the **semesters of the academic year** as natural blocks for rhythm.
- Designing **time slots** that align with real-world cognitive stamina (24-minute blocks + decompression).
- Choosing **global-friendly time zones** mapped to major cities.
- Embedding **nature and animal emojis** to stimulate the visual cortex.
- Pre-generating 3-week rotation cycles so you never again ask: “When are you free?”

Meetmoji Forge encodes all this into shareable, modular `.ics` files.

You get structure, *without rigidity*.  
You get clarity, *without clutter*.  
And most of all, you **get to lead your schedule instead of being crushed by it**.

---

## 🗺️ System Overview

- 📅 **Academic Calendar Basis:**  
  Anchored on the **European university year** (September–September), with **two semesters**, clear **downtime**, and a **deep summer work phase**.

- ⏰ **Time Slots:**  
  Each weekday contains up to 10 × 24-minute slots (every 30 mins, with a 6-min decompression).  
  Events recur every **3 weeks** by default — allowing **natural pacing without burnout**.

- 🌍 **Timezone Anchoring:**  
  Slot blocks are designed to align with local lunch / afternoon hours in:
  - Tokyo
  - South Asia (Delhi)
  - Brussels
  - Washington DC
  - Seattle
  - *(Optionally: Oceania – Mondays and Fridays)*

- 🌀 **Emoji Assignment:**  
  Each slot is deterministically assigned a unique emoji — drawn from a carefully curated pool of 150 glyphs.  
  When scheduling a meeting, you just rename the emoji to the person's name, assign the Zoom link, and go.

- 📂 **Modular ICS Output:**  
  Each **phase** gets its own `.ics` file.  
  Each **meeting slot block** is structured with its emoji, time, and metadata in `SUMMARY` and `DESCRIPTION`.

---

## 🔧 How to Use

```bash
git clone https://github.com/admin-tca/meetmoji-forge.git
cd meetmoji-forge
python3 meetmoji_forge.py
```

## 🛠 Configuration
At the top of the script, you’ll find a clearly marked # 🔧 USER CONFIGURATION block.
There you can set:

  - Start date of the academic year (year_start)
  - Semester vs quarterly mode
  - Whether to include Oceania
  - Number of total cycles
  - Emoji reuse logic (per phase or global)

All configuration lives inside the Python file for now — no external dependencies.

## 📁 Output

The tool generates:

  - output/semester_phases.ics – all-day blocks for each phase (e.g., Semester A, Winter Break)
  - output/meeting_<phase_slug>.ics – detailed meeting slot files, one per phase
    
CLI --dry-run mode for inspection
CLI --year YYYY support for future academic years

Each event includes:

  - 📛 SUMMARY: E.g., Tokyo Slot 🐝 #12 (13:30–14:30 JST)
  - 🧾 DESCRIPTION: Auto-generated 🤖🔐☕️💬 — Semester A (Seed)
  - 🎨 (Optionally: ICS Category/Color tags)

## 📎 Suggested Workflow

1. Import the .ics files into your calendar.
2. When you want to book a 1:1:
  - Ask: “What city are you in, and what weekday works?”
  - Visually scan for that region’s emoji slots on that day.
  - Pick one. Rename the event’s emoji to their name. Done.
  - Tell them what emoji they are. It starts a conversation.
3. “Hey! You’re my 🐝 meeting this semester — perfect, you’re pollen-powered.”
  - It creates immediacy, identity, and a bond — without overhead.

## 🌀 Future Directions

  - 🧠 AI integration for predictive slot optimization
  - 📊 Visual printout calendar overlays
  - 📜 TCA-aligned “Time Rites” ceremonial framing (for TCA ritual integration)
  - 📆 Apple Shortcuts or mobile wrapper

## 📡 The EBI24\_CLOCK Convention: A Ritual Lexicon for Coordinated Time

**Meetmoji Forge** is more than a meeting calendar generator — it is a human-centric calendrical ritual system designed for resilient collaboration across fractured geographies and time zones. One of its most quietly revolutionary components is the **EBI24\_CLOCK**, a deterministic, emoji-based time alphabet built to serve as a globally legible alternative to traditional numeric hour references.

## 🤔 Why Replace Numeric Time?

Coordinating time across time zones is cognitively expensive and error-prone. Most humans are not wired to convert between UTC, local daylight shifting, or regional quirks like India’s +5:30 offset. When collaborating across cultures and continents — especially over degraded or unreliable connections — even seemingly trivial scheduling tasks can introduce friction.

To address this, we designed a **spoken-friendly, emoji-anchored system** that avoids numeric ambiguity and encodes **UTC hours into 24 distinct animal faces**, each chosen for:

  - **Verbal distinctiveness**, even in noisy or low-fidelity voice environments.
  - **Cross-cultural recognizability**, avoiding animals with negative or culturally complex associations.
  - **Minimal syllabic overlap**, allowing for fast recognition and reduced ambiguity.

The result is a human-parseable ritual time lexicon that sounds more like aviation call signs or poetic code than a dry timestamp.

> "Let's meet at **Badger Face Thirty** next Wednesday."
>
> "I'm only free during **Bunny Face** or **Fox Face** hours this week."

## 🧬 Format

Each UTC hour is mapped to an emoji and a **Standard Description** (e.g., “Dog Face”, “Sloth Face”) that can be used in speech or text.

| Hour (UTC) | Emoji | Description   |
| ---------- | ----- | ------------- |
| 00         | 🐶    | Dog Face      |
| 01         | 🐱    | Cat Face      |
| 02         | 🐭    | Mouse Face    |
| 03         | 🦝    | Raccoon Face  |
| 04         | 🐰    | Bunny Face    |
| 05         | 🦊    | Fox Face      |
| 06         | 🐻    | Bear Face     |
| 07         | 🐴    | Horse Face    |
| 08         | 🐐    | Goat Face     |
| 09         | 🐯    | Tiger Face    |
| 10         | 🦁    | Lion Face     |
| 11         | 🦬    | Bison Face    |
| 12         | 🐸    | Frog Face     |
| 13         | 🦥    | Sloth Face    |
| 14         | 🐔    | Chicken Face  |
| 15         | 🦔    | Hedgehog Face |
| 16         | 🦡    | Badger Face   |
| 17         | 🦜    | Parrot Face   |
| 18         | 🐺    | Wolf Face     |
| 19         | 🦆    | Duck Face     |
| 20         | 🦉    | Owl Face      |
| 21         | 🦇    | Bat Face      |
| 22         | 🐢    | Turtle Face   |
| 23         | 🐵    | Monkey Face   |

Each full emoji-time phrase is composed of:

```
<Animal Face> + <Minute Offset>
```

For example:

  -  “🦡 Badger Face Thirty” → UTC 16:30
  -  “🐺 Wolf Face Fifteen” → UTC 18:15
  -  “🦝 Raccoon Face at the top” → UTC 03:00

## 🗺️ Cultural + Technical Considerations

  -  **No animals with strong regional taboos** (e.g. pigs in Islamic contexts, snakes in East Asia).
  -  **Avoids emoji ambiguity** by choosing animal face emojis with high visual distinctiveness across platforms.
  -  **Tested for verbal clarity** among non-native English speakers.
  -  **Machine-readable** for deterministic lookup in calendaring systems and future EBI6 protocol extensions.

## 🛠 Integration with Meetmoji Forge

The EBI24\_CLOCK is used internally to:

  - Tag calendar slots with **distinct, memorable visual cues**.
  - Enable **voice-friendly scheduling shorthand** across global teams.
  - Support **ritual linguistic framing** in ceremonial or distributed scheduling contexts.

It is also extensible — allowing integrations with:

  - Localizations (e.g., translating “Badger Face” to “Tête de blaireau”)
  - Offline paper planners with emoji glyphs
  - Braille + AAC-compatible symbol boards

---

This convention is part of a broader philosophy we call **Semantic Resilience**: the design of systems that stay useful and expressive even when degraded, misunderstood, or disconnected from their origin.

If the Internet fractures and time zones blur, **Badger Face Thirty** will still make sense.

## 🌍 On Prayer Times and Rhythmic Coexistence

The **Meetmoji Forge** meeting system was designed from first principles to optimize **cognitive cadence**, **global time-zone fairness**, and **visual-semantic coherence** using unique emoji identifiers. While primarily aligned to secular work rhythms, we recognize that **spiritual timekeeping** is an equally ancient and vital human pattern.

In particular, we acknowledge the daily prayer cycles observed by over **1.8 billion Muslims worldwide**. The five daily *salat* prayers are tied to **solar positions**, not fixed clock time, but often occur within the following general local ranges:

| Prayer  | Typical Time Range (local)        |
| ------- | --------------------------------- |
| Fajr    | \~05:00–06:00 (before sunrise)    |
| Dhuhr   | \~12:15–13:45 (after solar noon)  |
| Asr     | \~15:30–17:30                     |
| Maghrib | \~19:00–20:00 (just after sunset) |
| Isha    | \~20:00–22:00                     |

We have analyzed our default emoji-based slot schedules and confirmed:

  - ✅ No overlap with **Fajr**, **Maghrib**, or **Isha**
  - 🟡 **Dhuhr** may occasionally overlap with 13:30–14:30 meetings in some regions (e.g., Brussels, Kuala Lumpur)
  - ✅ Most slots avoid **Asr** in typical configurations

To ensure respectful coexistence, we recommend:

  - Flexibility in local interpretation of time blocks
  - Optionally shifting series slightly in high-observance zones
  - Recognizing that **time itself is plural** — cultural, solar, symbolic

This project honors the **layered rhythms of human life**, from Gregorian structure to solar shadows to digital glyphs.

🧭 *Where time meets glyph, let coherence also meet conscience.*

## 💬 Credits

Originally designed by Trey Darley as a practical calendaring ritual for the
Threshold Continuity Alliance.

> Built with clarity, empathy, and some damned fine emoji taste by chatgpt.
