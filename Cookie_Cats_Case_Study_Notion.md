# Cookie Cats Gate Placement: A Product Experimentation Case Study

Sambhavya Nayak | Product Analytics Case Study
GitHub: github.com/<your-username>/cookie-cats-ab-testing-analysis

---

## 1. Context

Cookie Cats is a mobile puzzle game where players hit a "gate" at certain levels, forcing them to wait or pay to continue. The game's first gate sat at level 30. The product team wanted to test whether moving it to level 40 — giving players more uninterrupted play before the first ask — would improve retention. This case study evaluates that experiment for 90,189 players randomly split into two groups (Gate 30 vs. Gate 40) and makes a ship / no-ship recommendation.

## 2. Hypothesis & Experiment Design

- **Null hypothesis (H0):** Gate placement (30 vs. 40) has no effect on 7-day retention.
- **Alternative (H1):** Gate placement has a measurable effect on 7-day retention.

7-day retention was chosen as the primary metric over 1-day retention because it better reflects sustained engagement rather than a first-session bounce, and it's more predictive of long-term monetization potential.

A statistical power analysis confirmed **88.4% power** to detect the observed effect size — meaning the experiment was sufficiently sized to trust a negative result, not just a positive one.

## 3. Guardrail Check: Was the Test Even Valid?

Before trusting any result, the group split was checked for a **Sample Ratio Mismatch (SRM)** — a common but often-skipped step that catches broken randomization or logging bugs. The split held at roughly 44,700 (Gate 30) vs. 45,489 (Gate 40) users, consistent with a healthy 50/50 assignment. Without this check, a team risks shipping a decision based on a corrupted experiment.

`[Insert executive_dashboard.png here]`
*Fig 1. Executive summary of experiment scale and topline retention deltas.*

## 4. Results: Gate 30 Wins Overall

Gate 30 outperformed Gate 40 on both retention windows. The gap widens over time — a 0.59 point lift at 1 day grows to a 0.82 point lift at 7 days, suggesting the effect compounds rather than fades.

| Metric | Gate 30 | Gate 40 | Lift |
|---|---|---|---|
| 1-Day Retention | 44.82% | 44.23% | +0.59 pts |
| 7-Day Retention | 19.02% | 18.20% | +0.82 pts |

`[Insert overall_retention.png here]`
*Fig 2. 1-day and 7-day retention, Gate 30 vs. Gate 40.*

`[Insert retention_improvement.png here]`
*Fig 3. Retention lift of keeping the gate at level 30.*

## 5. The Real Insight: It Depends Who You Ask

Averages hide the story that matters for a product decision. Players were split into Low, Medium, and High engagement segments (roughly equal thirds, ~28-32K players each) based on total game rounds played. The segment breakdown shows the retention drop under Gate 40 is **not evenly distributed**:

- **Low-engagement players:** essentially unaffected, and marginally higher retention under Gate 40 (1.64% vs. 1.54% at day 7).
- **Medium-engagement players:** retention drops from 8.68% to 7.97% at day 7 under Gate 40.
- **High-engagement players:** the largest drop of any segment — 47.66% down to 46.38% at day 7, a 1.28 point loss.

High-engagement players are typically a game's most valuable users — the ones most likely to convert to paying customers over time. Moving the gate later hurts retention most for exactly this group, which a top-line average completely masks.

`[Insert segment_analysis.png here]`
*Fig 4. Retention by engagement segment, 1-day and 7-day.*

## 6. Recommendation

**Do not move the gate to level 40. Keep it at level 30.**

The overall retention lift is small in absolute terms, but it is directionally consistent, grows over the 7-day window, and is concentrated among the game's highest-value players — the segment a product team can least afford to lose. Shipping Gate 40 would trade a marginal early-funnel experience improvement for a measurable retention cost among the most engaged users.

## 7. Follow-Up Experiment

Rather than treating this as a closed question, the more interesting product move is to test a **soft gate** at level 40 — skippable via a rewarded ad or in-game currency — instead of a hard wall. This could capture the original intent (longer uninterrupted early play) without penalizing high-engagement players who are most sensitive to friction. If shipped, I would monitor 7-day retention by segment, ad-view rate, and in-app purchase conversion as the primary success and guardrail metrics.

---

*Appendix: Player engagement distribution (log scale), used to construct the Low / Medium / High segments above.*

`[Insert engagement_distribution.png here]`
