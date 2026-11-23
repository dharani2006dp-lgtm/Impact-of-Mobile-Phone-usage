# Impact of Mobile Phone Usage on Students' Academic Performance

We're six B.Com (Business Analytics) students from Kangeyam Institute of Commerce, and we wanted to answer a simple question: **does our phone habit actually hurt our studies?**

So we asked 464 college students about their phone use, study habits, sleep and marks, then looked at what the numbers say. This repo holds our data, code and report.

**Affiliated to:** Bharathiar University, Coimbatore
**Academic year:** 2025 – 2026
**Guide:** _(add guide name)_

**Team:** V. Dharani Prakash, M. Rehana Gowsi, A. Akash, P. Janahariharasudhan, M. Aakash Renan, B. Haripriya

---

## What we wanted to find out

- How much do students use their phones, and for how long have they had one?
- Do they use phones while studying, and how often do they check them?
- Do students feel phones hurt their concentration and study time?
- Is phone use linked to their academic performance?
- Does late-night phone use affect sleep?
- Do digital well-being tools and self-discipline actually help?

---

## How we collected the data

We built a questionnaire with 25 questions in **Google Forms**. It covered:

- basic details (gender, age, course)
- how long they've had a smartphone and how many hours a day they use it
- phone use while studying and how often they check it
- +2 marks and current CGPA/percentage
- effects on concentration, study time, tiredness and sleep
- awareness, parental/teacher restrictions and digital well-being tools

We shared the link in student groups we could reach, and people answered voluntarily. This is called **convenience sampling**. In the end we had **464 valid responses**, mostly B.Com and BBA students, collected during 2025–2026.

For the background reading, we used published articles, journals and reports.

---

## How we cleaned the data

>  _Edit this section to match exactly what your team did._

Google Forms gives you a messy export, so before analysing anything we:

1. Downloaded the responses as a CSV/Excel file.
2. Removed blank, incomplete or duplicate submissions, which left 464 valid responses.
3. Fixed inconsistent labels (spacing, capital letters, small spelling differences) so each answer appeared in only one form.
4. Left unanswered questions blank instead of guessing. That's why a few tables show a different number of responses (for example, 463 for checking frequency and 352 for main distraction).
5. Dropped the "Not Applicable" CGPA answers (for example, students who don't have a CGPA yet) from the CGPA tests, leaving 401 responses there.
6. Turned answers into numbers where needed: Likert answers became 1–5, and CGPA bands became their midpoints (70–80% became 75) so we could run ANOVA.
7. Kept the dataset anonymous. No names, emails or phone numbers.

---

## Tools we used

| What | Tool |
|------|------|
| Collecting responses | Google Forms |
| Storing and tidying data | Microsoft Excel |
| Writing the report | Microsoft Word |
| Sharing the project | Git and GitHub |

---

## How we analysed it

- **Frequency and percentages** for every question.
- **Cross-tabulation** to compare academic performance across screen-time groups and across "use phone while studying" groups.
- **Chi-square test** to check whether those links could be down to chance.
- **One-way ANOVA** to see if average concentration score and CGPA differ between screen-time groups.
- **Two-way ANOVA** to test screen time and phone use while studying together.
- **Charts** (pie, donut, line, bar, and a Pareto chart) to show the results.

---

## What we found

**Usage**
- 97% of students own a smartphone.
- The most common daily usage is 2–4 hours (42%). About one in three uses it for more than 4 hours.
- 51% use their phone while studying, and another 34% said "maybe".
- Social media notifications are the biggest distraction (about 53%).

**Effects**
- Around 56% agree that phones affect their concentration.
- 44.6% say phones have cut into their study time.
- On academic performance, 47% saw no change, 30% said it improved and 23% said it dropped.
- 39% use their phone late at night, and 33% of all students say it affects their sleep.

**What helps**
- 61% already use tools like screen-time limits or focus mode, and 58% say their concentration improved.
- Students think **self-discipline (45.5%)** and **time limits (34.5%)** work best.

### The statistics

| Test | Result |
|------|--------|
| Screen time × performance (chi-square) | Significant (χ² = 45.272, df = 9, p < 0.001) |
| Phone use while studying × performance (chi-square) | Significant (χ² = 25.893, df = 6, p < 0.001) |
| Late-night use × sleep effect (chi-square) | Significant (χ² = 39.551, df = 2, p < 0.001) |
| Screen time → concentration / CGPA (one-way ANOVA) | Not significant (p = 0.442 / 0.678) |
| Screen time × phone use while studying (two-way ANOVA) | Not significant (all p > 0.05) |

**In plain words:** how and when students use their phones seems to matter more than how many hours they spend on them. Using the phone in an unplanned way during study, or for more than 4–6 hours a day, shows up more often alongside lower performance. Moderate, purposeful use doesn't seem to do much harm.

---

## What we'd suggest

- Try phone-free study blocks (the Pomodoro method is a good start).
- Switch on focus mode and app time limits.
- Cut down late-night scrolling, or use night mode.
- Use phones for learning (educational apps, online classes) instead of banning them outright.
- Focus on building self-discipline, since students themselves ranked it highest.

---

## Things to keep in mind

We want to be upfront about the limits of this study:

- Everything is **self-reported**, so people may misremember or answer how they'd like to look.
- Marks are given as **ranges**, not checked against real records.
- We used **convenience sampling** at one institution, so the results may not apply to all students.
- It's a **single snapshot** in time, not a long-term study.
- We found **associations, not proof of cause and effect**.
- ANOVA on banded and Likert data isn't perfect. Non-parametric tests would be a good next step.

---

## Repo layout

```
├── data/
│   ├── raw/          # anonymised Google Forms export
│   └── cleaned/      # cleaned dataset
├── notebooks/
│   └── analysis.ipynb
├── charts/
├── report/
│   └── Impact_of_Mobile_Phone_Usage_Report.pdf
├── questionnaire/
└── README.md
```

## Run it yourself

```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
pip install pandas matplotlib scipy statsmodels jupyter
jupyter notebook notebooks/analysis.ipynb
```

---

## References

- Kothari, C. R., *Research Methodology: Methods and Techniques*, New Age International Publishers.
- _(Add your literature-survey references here.)_

## Thank you

To our guide, our Head of Department and faculty, everyone who filled in the questionnaire, and our families and friends for the support.

This project was done for academic purposes.
