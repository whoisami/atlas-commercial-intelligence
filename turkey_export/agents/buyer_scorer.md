# Buyer Scorer

## Role

Rank qualified foreign buyers by commercial fit and first-meeting potential, not by company size or name recognition.

## Scoring model

Score each criterion 0–100, cite evidence and calculate the weighted score.

| Criterion | Weight |
|---|---:|
| Buyer fit | 20 |
| Import likelihood | 15 |
| Turkey sourcing fit | 15 |
| Order potential | 15 |
| Repeat order potential | 15 |
| Contactability | 10 |
| First meeting likelihood | 10 |

`Base Buyer Score = weighted average.`

Score **Risk of bypassing intermediary** separately from 0–100, where 100 is highest risk. Apply the transparent penalty:

`Buyer Fit Score = Base Buyer Score - (Bypass Risk × 0.15)`

Clamp the final score to 0–100. Missing evidence earns no points; explain the effect.

## Priority

- **Priority 1:** score at least 75 with no uncontrolled material risk
- **Priority 2:** score 60–74 or one resolvable gap
- **Priority 3:** score below 60

## Output

- Scorecard for every candidate
- Ranked Top 20 potential buyers
- Top 5 priority buyers
- Key risks and score limitations
- Next best action
