# HK Salaries Tax + MPF Calculator | 香港薪俸稅 + 強積金計算機

Free, offline, single-file calculator for Hong Kong employees: work out your
salaries tax (allowances, progressive vs standard rate, one-off reduction) and
your MPF contributions in one place. No login, no upload, no server — your
inputs are stored only in your browser's localStorage.

免費、離線、單一檔案：一次計出香港薪俸稅（免稅額、累進稅率 vs 標準稅率、
一次性寬減）及強積金供款。免登入、免上傳、無伺服器；輸入只存於你瀏覽器的
localStorage。

## Use 使用

Open `index.html` in any browser (including iOS 16 Safari) — or host it on
GitHub Pages. Enter monthly salary, bonus, rent, TVC, marital status,
children and dependent parents, pick the tax year, and press Calculate.

直接用瀏覽器開啟 `index.html` 即可（包括 iOS 16 Safari），或放上 GitHub
Pages。輸入月薪、花紅、租金、自願性供款、婚姻狀況、子女及供養父母數目，
選擇課稅年度，按「計算」。

## What it calculates 計算內容

- **Annual income 全年入息** — monthly salary × 12 + bonus / 13th month.
- **MPF 強積金** — employee and employer each 5% of monthly relevant income.
  Below HK$7,100/month the employee pays nothing (employer still pays 5%).
  Capped at HK$1,500/month each from HK$30,000/month
  (HK$18,000/year max mandatory contribution, which is also the max
  tax-deductible amount).
- **Deductions 扣除** — mandatory MPF (max $18,000), TVC voluntary
  contributions (max $60,000/year, shared with qualifying deferred annuity
  premiums), domestic rent (max $100,000/year, or $120,000 if you live with a
  child born on/after 25 Oct 2023), home loan interest (max $100,000/year,
  up to 20 years), self-education expenses (max $100,000/year) and elderly
  residential care expenses (max $100,000/year, for a dependent parent /
  grandparent aged 60+ in a licensed residential care home).
- **Allowances 免稅額** — basic / married, child per child, dependent parent
  (60+, doubled if living with you continuously all year; 55–59 is half),
  single-parent allowance (unmarried with a dependent child, same amount as
  basic), an extra child allowance in a child's year of birth — which
  from 2026/27 runs for a second year (children born on/after 1 Apr 2025) —
  disabled dependant allowance ($75,000 / $82,500 each, additional to the
  child / parent allowance for the same person), personal disability
  allowance (same amounts, if you are eligible for Disability Allowance)
  and dependent brother / sister allowance ($37,500 / $41,250 each).
- **Tax 稅款** — progressive rates on net chargeable income vs standard rate
  on net income; IRD charges the lower. One-off 100% reduction toggle where
  announced.
- **Take-home pay 實得工資** — monthly, after employee MPF and salaries tax;
  plus the effective tax rate.
- **Year comparison 年度比較** — the same inputs in 2025/26 and 2026/27
  side by side (tax, take-home, allowances, net chargeable income), with the
  cheaper year highlighted and the reason explained (higher 2026/27
  allowances vs the announced 2025/26 reduction).
- **Progressive bands 累進稅率分層** — every band shown with its income,
  rate, tax and a bar, so you can see exactly where the tax comes from.
- **What-if 多想一步** — marginal tax on a +HK$1,000/month raise, and the
  tax each deduction (rent / TVC / home loan / self-education) saves you.
- **MPF projection 強積金預測** — total annual MPF (employee + employer)
  projected 10 and 30 years at a 3% return (estimate only).
- **Joint vs separate assessment 合併 vs 分開評稅** — optional spouse
  salary, deductions and dependant inputs; compares the two methods with
  per-person / per-couple pooling (mandatory MPF sums per person; TVC,
  self-education and elderly care pool per person; rent and home-loan
  interest pool per couple under one cap each; disabled-dependant and
  sibling allowances pool by count).
- **Copy summary / print 複製摘要 / 列印** — one-tap text summary and a
  print-friendly view (Save as PDF).

## Rates used (verified against IRD, Nov 2026) 已核實稅率

| Item | 2025/26 | 2026/27 |
|---|---|---|
| Basic allowance 基本免稅額 | $132,000 | $145,000 |
| Married person's allowance 已婚人士免稅額 | $264,000 | $290,000 |
| Child allowance, each (1st–9th) 子女免稅額每名 | $130,000 | $140,000 |
| Dependent parent 60+, each 供養父母每名 | $50,000 | $55,000 |
| + additional if living together 全年同住額外 | +$50,000 | +$55,000 |
| Disabled dependant, each 傷殘受養人每名 | $75,000 | $82,500 |
| Personal disability 傷殘人士 | $75,000 | $82,500 |
| Dependent brother / sister, each 供養兄弟姊妹每名 | $37,500 | $41,250 |
| Elderly residential care, max 長者住宿照顧開支上限 | $100,000 | $100,000 |
| Progressive 累進稅率 | 2% / 6% / 10% / 14% / 17% per $50,000 band | same 相同 |
| Standard rate 標準稅率 | 15% first $5M, 16% remainder | same 相同 |
| One-off reduction 一次性寬減 | 100%, max $3,000 | not yet announced 未公布 |

Sources 資料來源：

- IRD, *Allowances, Deductions and Tax Rate Table* (PAM 61, Aug 2026) —
  https://www.ird.gov.hk/eng/pdf/pam61e.pdf — allowances, deduction caps,
  progressive bands, two-tier standard rate, and the tax-reduction table
  (2025/26: 100%, max $3,000).
- IRD, *2025-26 Budget – Tax Measures* FAQ —
  https://www.ird.gov.hk/eng/faq/budget2025_26.htm — the $1,500 cap belonged
  to year of assessment **2024/25**, not 2025/26.
- MPFA — mandatory MPF 5%, minimum relevant income $7,100/month, maximum
  $30,000/month, cap $1,500/month each side.
- IRD domestic rent deduction — basic cap $100,000/year; additional $20,000
  (total $120,000) from 2024/25 for taxpayers living with a child born
  on/after 25 Oct 2023.

### Corrections to the figures in the original brief 原要求數字的更正

The brief that commissioned this tool contained three figures that do not
match the IRD table; the calculator uses the IRD figures, not the brief's:

1. **Child allowance 子女免稅額** — brief said "$130,000 each first two
   then $120,000". IRD: **$130,000 for each of the 1st–9th child**
   in 2025/26 ($140,000 in 2026/27); the $120,000 figure was the pre-2023/24
   amount. There is an extra $130,000 in the child's year of birth, which
   this tool models — and from 2026/27 the extra runs for a second year
   (children born on/after 1 Apr 2025), also modelled. The Sep 2026 Policy
   Address proposal of $160,000 for second and subsequent children born
   on/after 16 Sep 2026 is not yet law and is not applied.
2. **Dependent parent allowance 供養父母免稅額** — brief said "$50,000 each /
   $25,000 if living with you". IRD: it is the other way round —
   **$50,000 base (60+), plus an additional $50,000 if the parent lives with
   you continuously all year = $100,000 total**; age 55–59 is $25,000 base
   (+$25,000 if living together). This tool assumes age 60+ and lets you
   tick "living together" to double it.
3. **One-off tax reduction 一次性寬減** — brief said "2025/26: 100%, capped
   at $1,500". IRD PAM 61: **2025/26 is 100% capped at $3,000**; the $1,500
   cap was for 2024/25. For 2026/27 no reduction has been announced yet
   (expected in the Feb 2027 Budget), so the toggle applies $0 for that year.

## Limitations 限制

- Estimate only — not tax advice. 僅供估算，並非稅務建議。
- MPF is calculated on monthly salary only. A bonus counts as relevant
  income in the month it is paid, so your real MPF in a bonus month may be
  higher (still capped at $1,500). 花紅在發放月份亦屬有關入息，實際供款
  可能較高（仍以 $1,500 為上限）。
- Does not model: personal assessment 個人入息課稅 (it only helps if you
  have rental or business income to aggregate with your salary — this tool
  covers salaries tax on employment income only), the proposed $160,000
  child allowance for second and subsequent children born on/after 16 Sep
  2026 (not yet law), the spouse's own personal-disability allowance under
  joint assessment, or separate rent / mortgage arrangements under joint
  assessment (rent and home-loan interest are modelled as one cap per
  couple — see §6 in the page). The page itself lists these cases in a
  "When this tool does NOT apply" box. 未計：個人入息課稅、建議中第二名及
  之後子女 $160,000 免稅額（未立法）、合併評稅下配偶本人的傷殘人士免稅額、
  夫婦分開租住/供樓的安排（租金/房貸以每對夫婦一個上限計）。報稅前請核對
  ird.gov.hk。

## Tests 測試

```sh
node tests/test_tax.js
```

195 checks, all passing (as of 2026-11-11): the original 55, plus 49 new —
home-loan and self-education deductions and their $100,000 caps, single-parent
allowance ($132,000, not when married), extra child allowance in the birth
year, dependent-parent rate at 55–59 (half), year comparison both ways
(2026/27 cheaper without a reduction, 2025/26 cheaper with one), progressive
band breakdowns summing to the progressive tax, marginal tax on a +$1,000/mo
raise ($980/yr, 8.17% at $20k), savings from rent / TVC, MPF projections
(10y / 30y at 3%), joint-vs-separate cases (separate cheaper by $31,920 with
a $30k spouse; identical with a non-working spouse), and unchanged results
for the original inputs. Plus 11 more in this pass — the second-year newborn
allowance from 2026/27 ($140,000 extra, $740 tax at $40k/mo with 1 child;
$0 in 2025/26 where the rule does not apply; $280,000 with both flags;
joint comparison with the flag correctly kept off the spouse: mine $0,
spouse $15,580, joint $21,780, separate wins by $6,200). MPF $1,000/mo at $20k salary,
capped $1,500/mo at $100k, $0 below $7,100, $355 at exactly $7,100,
standard-vs-progressive lower-of rule ($500k/mo uses standard),
child / rent / TVC / married / dependent-parent effects, 2025/26 vs 2026/27
rates, reduction caps ($3,000 for 2025/26, $0 unannounced for 2026/27),
band boundaries, bonus handling, zero income, take-home and effective rate.
Plus 80 more in the third pass (2026-11-11) — disabled dependant allowance
($75,000 / $82,500, $7,500 tax at $30k/mo with one dependant vs $17,700
without, saves $10,200), personal disability allowance (same amounts, same
effect), dependent brother/sister allowance ($37,500 / $41,250, 2 siblings
= $75,000), elderly residential care expenses ($120,000 claimed capped at
$100,000, $5,000 tax at $30k/mo; $8,700 saved by $60,000 of expenses), a
disabled child getting both the child and the disabled allowance
($337,000 total allowances, $100 tax), and joint pooling: spouse TVC
$60,000 (spouse $17,700 → $9,000, joint $63,600, joint deductions $96,000),
rent and home-loan interest pooled per couple under one $100,000 cap
($96,000 + $96,000 rent → joint $56,800 vs separate $9,600; $80,000 +
$80,000 home loan → joint $56,800 vs separate $12,800 — the per-couple cap
makes joint worse in both cases), disabled dependants pooled by count
(1 + 1, joint $48,300 vs separate $13,800), self-education and elderly care
pooled per person ($100,000 each side, joint deductions $436,000, joint
$8,000 vs separate $200), a spouse sibling (spouse $12,150, joint $67,425),
no-spouseOpts regression (joint $73,800, separate $33,420, unchanged), page
wiring for all 11 new inputs plus the "does NOT apply" box, and an automated
ES5 guard over the shipped JS.

The pure functions in `tests/test_tax.js` are duplicated from the
`<script>` block in `index.html` (noted in a comment there). Keep the two
copies in sync if you change the maths.

## Tech 技術

Single `index.html`, ES5 only (safe for iOS 16 Safari), white background, no
external resources, no frameworks, no network calls. Inputs persist via
localStorage only.

## License

MIT — see `LICENSE`.
