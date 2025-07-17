# 🧿 Meetmoji Forge

**The Ritual Calendar Crafter — Where Time Meets Glyph**
*...and where your visual cortex takes over from your guilt-ridden monkey mind!*

---

## 📖 What is Meetmoji Forge?

**Meetmoji Forge** is a handcrafted calendaring ritual tool that generates `.ics` files for your academic year — complete with phase-based planning blocks and visually anchored, emoji-clock-coded meeting slots.

This is not a generic scheduling app.
It is a **semantic time protocol**.
A **cognitive architecture**.
A tool to bring order, rhythm, and signal to your collaborative life.

You don’t schedule meetings with guilt.
You schedule them by asking:

> **“What animal face are you today?”** 🐻🦊🦡🦉

---

## 🎯 Why This Exists

Most calendars are built for compliance — not cognition.

They assume your brain is a command-line buffer:
linear, overclocked, contextless.

But human minds aren’t machines. They are:

* **Visual**
* **Rhythmic**
* **Symbolic**
* **Context-sensitive**

**Meetmoji Forge** is designed from first principles to support high-coherence scheduling across global teams, without sacrificing clarity or dignity.

It works by:

* Aligning to the **natural flow of the academic year**
* Building in **cognitive affordances** (25-min focus slots + decompression time)
* Anchoring to **global cities** and fair-time blocks
* Using **deterministic emoji-hour tags** (via `EBI24_CLOCK`) for symbolic shorthand
* Outputting **modular, shareable `.ics` files** — ready to drop into any modern calendar

No apps. No cloud. Just clean, meaningful time encoded in human-readable glyphs.

---

## 🗺️ System Overview

### 📅 Academic Calendar Basis

Anchored on the European academic year (default: **September 15**).
Each year is divided into symbolic phases:

* Semester A (Seed)
* Winter Break
* Semester A (cont.)
* Downtime A→B
* Semester B (Flame)
* Summer Rest
* Deep Work Phase
* Preflight Prep
* Liminal Drift

Each phase outputs its own `.ics`.

### ⏰ Time Slot Design

Each participating weekday includes **8 meeting slots**, recurring every **3 weeks**, with:

* 25 minutes of focused conversation
* 5-minute decompression buffer
* Aligned to globally humane windows (e.g., 13:30–13:55 JST)

### 🌐 Time Zone Anchors

Slots are defined for:

* 🗼 Tokyo
* 🕌 Delhi
* 🏛 Brussels
* 🏛 Washington DC
* 🏞 Seattle
  *(Optional: Oceania region)*

### 🧠 Emoji Time Protocol — `EBI24_CLOCK`

Each slot is tagged with a **unique animal face emoji**, deterministically mapped by UTC hour.

This provides:

* Visual shorthand
* Cross-lingual clarity
* Low-bandwidth legibility
* Symbolic rhythm

---

## 🔁 From Random Emoji Chaos to Ritual Time Glyphs

Originally, each slot used a randomized emoji — but this caused:

* Confusion across meetings
* Duplicate emojis per cycle
* No reliable naming convention

Now, the **EBI24\_CLOCK** defines a canonical mapping:
**One emoji face per UTC hour** — globally consistent, culturally neutral.

> “Let’s meet at **Badger Face Thirty** next Thursday.”
> “I’m only free during **Fox Face** or **Wolf Face** today.”

---

## 🧬 EBI24\_CLOCK Reference

| UTC Hour | Emoji | Label         |
| -------- | ----- | ------------- |
| 00       | 🐶    | Dog Face      |
| 01       | 🐱    | Cat Face      |
| 02       | 🐭    | Mouse Face    |
| 03       | 🦝    | Raccoon Face  |
| 04       | 🐰    | Bunny Face    |
| 05       | 🦊    | Fox Face      |
| 06       | 🐻    | Bear Face     |
| 07       | 🐴    | Horse Face    |
| 08       | 🐐    | Goat Face     |
| 09       | 🐯    | Tiger Face    |
| 10       | 🦁    | Lion Face     |
| 11       | 🦬    | Bison Face    |
| 12       | 🐸    | Frog Face     |
| 13       | 🦥    | Sloth Face    |
| 14       | 🐔    | Chicken Face  |
| 15       | 🦔    | Hedgehog Face |
| 16       | 🦡    | Badger Face   |
| 17       | 🦜    | Parrot Face   |
| 18       | 🐺    | Wolf Face     |
| 19       | 🦆    | Duck Face     |
| 20       | 🦉    | Owl Face      |
| 21       | 🦇    | Bat Face      |
| 22       | 🐢    | Turtle Face   |
| 23       | 🐵    | Monkey Face   |

```text
🦡 Badger Face Thirty → UTC 16:30
```

---

## 📦 Output

You’ll receive:

* `output/semester_phases_<year>.ics` — full-year block markers
* `output/meeting_<phase>_<dates>.ics` — detailed 25-min meeting slots

Each `VEVENT` includes:

```ics
SUMMARY: Tokyo 🦊 Fox Face Slot #1 (13:30–13:55 JST)
DESCRIPTION: 🌱 — Semester A (Seed)
CLASS: PRIVATE
```

---

## 🛠 Configuration

In `main.py` or CLI args:

* `--year=YYYY` → Academic year start
* `--dry-run` → Simulate without writing files
* Configurable region, slot cadence, Oceania inclusion
* Deterministic UID generation for ICS re-import stability

All in standard Python 3 — no external dependencies required.

---

## 🧪 Usage

```bash
git clone https://github.com/admin-tca/meetmoji-forge.git
cd meetmoji-forge
python3 main.py --year=2039
```

To inspect or simulate without writing `.ics` files:

```bash
python3 main.py --year=2039 --dry-run
```

---

## 🙏 On Rhythmic Coexistence

**Meetmoji Forge is secular — but rhythm-aware.**

We’ve cross-checked time blocks against Islamic prayer times, for empathy in scheduling:

| Prayer  | Local Time Range | Conflict Risk         |
| ------- | ---------------- | --------------------- |
| Fajr    | \~05:00–06:00    | ❌ None                |
| Dhuhr   | \~12:30–13:45    | ⚠️ Potential conflict |
| Asr     | \~15:30–17:30    | ✅ Avoided             |
| Maghrib | \~19:00–20:00    | ❌ None                |
| Isha    | \~20:00–22:00    | ❌ None                |

> Wherever you are: treat others' solar, cultural, and spiritual rhythms with **grace**.

---

## 💬 Suggested Usage Flow

1. Import the relevant `.ics` files to your calendar.
2. Ask collaborators:

   > “What weekday + city block works for you?”
3. Pick a shared animal face slot:

   > “How about **Otter Face Twenty-Five** next Wednesday?”
4. Book the event, rename it with the person’s name.

---

## 🧭 Design Philosophy: Semantic Resilience

**Meetmoji Forge** is a component of the [Threshold Continuity Alliance (TCA)](https://longnow.eu).

It is designed to:

* Withstand technological drift
* Remain interpretable across collapse
* Encode **meaning** in minimal forms

> If nothing survives but emoji glyphs and printed calendars,
> **Badger Face Thirty** will still make sense.

---

## 🙌 Credits

* 🧠 Ritual Design & Calendar Theory: **Trey Darley**
* 🔧 Semantic Architecture & Engineering Support: **ChatGPT**, Claude
* 🦊 Glyph Taste Consulting: **ChatGPT**
* 🏛 Affiliation: **Threshold Continuity Alliance (TCA)**

---

> Calendars should be kind.
> Time should be meaningful.
> **Coherence is not optional.**

**Fox Face Out.** 🔥

---
