[README.md](https://github.com/user-attachments/files/32446876/README.md)
# One More Billable Hour

A fill-in operating brief for heavy-duty repair shop ownership. Enter a shop's figures
and the page calculates what one additional billable hour per technician per week is
worth — then prints on a single sheet as a leave-behind.

Part of the Fullbay adoption program.

## Use it

Open `index.html` in any browser, or host it (see below). Enter:

| Field | What it is |
|---|---|
| Shop | Name shown on the printed brief |
| Technicians | Techs the figures cover |
| Labor rate $/hr | The shop's billed labor rate |
| Tech wage $/hr | Median technician wage |
| Burden × | Wage plus payroll taxes, insurance and benefits (1.30 means a $33 wage costs $42.90) |
| Working weeks | Weeks used to annualize; 50 allows for holidays and shutdowns |

Everything recalculates as you type. To hand it over, print the page (⌘P / Ctrl+P) and
save as PDF — the input panel drops away and the brief prints on one page.

Entered values are remembered in the browser that typed them. Nothing is sent anywhere;
the page makes no network calls beyond loading its fonts.

## Host it on GitHub Pages

Settings → Pages → Source: *Deploy from a branch* → branch `main`, folder `/ (root)` → Save.
The page publishes at `https://<user>.github.io/<repo>/` within a minute or two.

GitHub Pages is free on public repositories. On a private repository it requires a paid plan —
if this stays private, open `index.html` locally or share the file instead.

## Change the defaults

The starting values live in the `value="..."` attributes of the inputs near the top of
`index.html`. The calculation is the `render()` function at the bottom — contribution per
hour is the labor rate less the technician's loaded cost, on the basis that fixed overhead
is already covered by current volume.

## Where the industry figures come from

Labor rate, technician wage, turnaround, inspection and workforce figures:
Fullbay *State of Heavy-Duty Repair 2025–2026* (~900 survey respondents plus 3,400+ Fullbay
shops, collected late 2025). Efficiency and utilization benchmarks: Fullbay Help Center,
"Benchmarks."

Figures quoted in the brief are industry medians. Shop-specific week-by-week numbers
belong in the weekly technician workbook, not here.
