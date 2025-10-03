# In The Name of God

---

## ⏱️ tm : Minimalistic Terminal timer with Study session tracking

### Features

- Countdown timer:
  - `tm 10s`, `tm 25m`, `tm 1h30m`
- Study/Train modes:
  - `tm --study` → track study sessions (resets daily, accumulates across multiple runs)
  - `tm --train` → track training sessions (same behavior, separate table)
- Daily logging:
  - Records totals in `~/.tm_timer/data.json`
  - Each day resets at midnight
- Statistics:
  - Average daily hours
  - Standard Deviation of Time
  - Status report:
    - **Very Good** (SD < AVG/2)  
    - **Good** (SD = AVG/2)  
    - **Not Good** (SD > AVG/2)
- Export:
  - `tm --studystatus` → show study table + stats
  - `tm --trainstatus` → show train table + stats
  - `tm --tables` → export both tables to `tables.md`
- Controls:
  - `p` → pause/resume
  - `q` → quit and save

---

### Installation

```bash
sudo apt install pipx       # if not installed
pipx install tm-timer       # install tm-timer
pipx ensurepath             # add tm to PATH
exec $SHELL                 # reload shell
````

---

### Example Usage

```bash
# Start a study session
tm --study

# Check study stats
tm --studystatus

# Start a train session
tm --train

# Export tables to tables.md
tm --tables
```

---

### Example Tables Output

```markdown
# tm_timer Tables

---

## STUDY Table

| Date       | Day | Time   |
| ---------- | --- | ------ |
| 2025-10-03 | FRI | 05:00:00 |
| 2025-10-02 | THU | 02:50:00 |
| 2025-09-29 | MON | 04:05:00 |
| 2025-09-27 | SAT | 03:36:00 |

**[AVG] = 3.98h    [Standard Deviation of Time] = 0.75h    Status = Very Good**

---

## TRAIN Table

| Date       | Day | Time   |
| ---------- | --- | ------ |
| 2025-10-03 | FRI | 00:57:00 |
| 2025-10-02 | THU | 00:50:00 |
| 2025-09-30 | SUN | 00:35:00 |
| 2025-09-28 | SAT | 01:36:00 |

**[AVG] = 1.05h    [Standard Deviation of Time] = 0.38h    Status = Very Good**
```

---

### Preview


![Timer preview](demo1.gif)

![Timer preview](demo2.gif)

![Timer preview](demo3.gif)
