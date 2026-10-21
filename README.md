# India-Stocks-1381-1410-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 1381 to 1410)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-1381-1410-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (1381 to 1410)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 1381 | `CCAVENUE` | AvenuesAI Limited | `CCAVENUE.NS` |
| 1382 | `HDFIRE` | HD Fire Protect Limited | `HDFIRE.NS` |
| 1383 | `IIRM` | IIRM Holdings India Limited | `IIRM.NS` |
| 1384 | `JAYSREETEA` | Jayshree Tea & Industries Limited | `JAYSREETEA.NS` |
| 1385 | `JENBURPH` | Jenburkt Pharmaceuticals Limited | `JENBURPH.NS` |
| 1386 | `JETFREIGHT` | Jet Freight Logistics Limited | `JETFREIGHT.NS` |
| 1387 | `JGCHEM` | J.G.Chemicals Limited | `JGCHEM.NS` |
| 1388 | `JHS` | JHS Svendgaard Laboratories Limited | `JHS.NS` |
| 1389 | `JINDALPHOT` | Jindal Photo Limited | `JINDALPHOT.NS` |
| 1390 | `JINDALPOLY` | Jindal Poly Films Limited | `JINDALPOLY.NS` |
| 1391 | `JINDRILL` | Jindal Drilling And Industries Limited | `JINDRILL.NS` |
| 1392 | `JINDWORLD` | Jindal Worldwide Limited | `JINDWORLD.NS` |
| 1393 | `JISLDVREQS` | Jain Irrigation Systems Limited | `JISLDVREQS.NS` |
| 1394 | `JISLJALEQS` | Jain Irrigation Systems Limited | `JISLJALEQS.NS` |
| 1395 | `JITFINFRA` | JITF Infralogistics Limited | `JITFINFRA.NS` |
| 1396 | `JKIL` | J.Kumar Infraprojects Limited | `JKIL.NS` |
| 1397 | `JKIPL` | Jinkushal Industries Limited | `JKIPL.NS` |
| 1398 | `JKLAKSHMI` | JK Lakshmi Cement Limited | `JKLAKSHMI.NS` |
| 1399 | `JKPAPER` | JK Paper Limited | `JKPAPER.NS` |
| 1400 | `JLHL` | Jupiter Life Line Hospitals Limited | `JLHL.NS` |
| 1401 | `JMA` | Jullundur Motor Agency (Delhi) Limited | `JMA.NS` |
| 1402 | `JNKINDIA` | JNK India Limited | `JNKINDIA.NS` |
| 1403 | `JNPR` | Juniper Green Energy Limited | `JNPR.NS` |
| 1404 | `JOCIL` | Jocil Limited | `JOCIL.NS` |
| 1405 | `JPOLYINVST` | Jindal Poly Investment and Finance Company Limited | `JPOLYINVST.NS` |
| 1406 | `JSFB` | Jana Small Finance Bank Limited | `JSFB.NS` |
| 1407 | `JSIPL` | Jindal Supreme (India) Limited | `JSIPL.NS` |
| 1408 | `JSLL` | Jeena Sikho Lifecare Limited | `JSLL.NS` |
| 1409 | `JSWDULUX` | JSW Dulux Limited | `JSWDULUX.NS` |
| 1410 | `JSWHL` | JSW Holdings Limited | `JSWHL.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream CCAVENUE 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-1381-1410-Historical-Data/main/CCAVENUE/1m/2026/10/CCAVENUE_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
