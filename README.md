# France-U23-vs-Spain-U23-Tactical-Video-Analysis-of-the-Paris-2024-Olympic-Final-Using-Nacsport
Tactical video analysis of the Paris 2024 Olympic final (France U23 3–5 Spain U23) using Nacsport: 17 tagged event types, all 8 goals analysed and defensive shapes with screenshots.

**Competition:** Paris 2024 Olympic Games, Men's Football Gold Medal Match
**Date and venue:** 9 August 2024, Parc des Princes, Paris
**Result:** France 3–5 Spain (after extra time)
**Formations :** France 4-1-2-1-2 · Spain 4-2-3-1
**Tagging software:** Nacsport
**Dashboard software:** Tableau (Tableau Public)
**Author:** Mwanahamisi Juma

---

## 1. Executive Summary

This project analyses the Paris 2024 Olympic final between France U23 and Spain U23 through manual video tagging in Nacsport. Seventeen event types covering possession, defensive organisation, transitions and set pieces were tagged for both teams across the full 120 minutes. The tagged data was combined with written tactical observations and a goal-by-goal analysis of all eight goals.

The main findings are:

- **France controlled territory.** France recorded more final third entries (137 vs 76), more shots (29 vs 19) and more attacking corners (12 vs 2).
- **Spain were more efficient.** Spain scored five goals from 19 attempts, while France scored three goals from 29 attempts.
- **Spain defended deeper.** Spain recorded 30 low-block phases against France's 10, and the video shows Spain using 4-4-2, 5-4-1 and 5-3-1 defensive shapes at different moments.
- **France's goals all followed dead-ball situations.** Their three goals came from a corner sequence, a free kick and a penalty awarded after a corner and VAR review.
- **Spain scored four of their five goals from open play,** through patient build-up, a regain followed by a long ball and cross, a rapid counterattack, and a ball played into the box after France's defenders left their line.

---

## 2. Project Objective

To analyse the attacking, defensive and transitional behaviours of France U23 and Spain U23 using Nacsport to identify key tactical patterns during the match.

## 3. Project Question

How did France U23 and Spain U23 organise themselves across the main phases of play, and what tactical patterns can be identified through video analysis of the match?

---

## 4. Software, Data Source and Method

| Item | Detail |
|---|---|
| **Tagging software** | Nacsport |
| **Dashboard software** | Tableau (Tableau Public) |
| **Match source** | Full match footage from YouTube. I tried to obtain the match through Ligue 1+, which is not available in my country, and through beIN Sports, where I could not find the full match. |
| **Analyst** | Single analyst, manual tagging |
| **Time reference** | All event times in this README are **actual match time**. Nacsport clip times were converted using the kickoff (clip 07:03), second-half start (clip 61:04) and extra-time start (clip 115:30). |

**Method**

I built a Nacsport code window with 15 buttons in four panels (In Possession, Out of Possession, Transitions, Set Pieces), plus Goal and Transition to Defence tags.
2. I tagged the full match for both teams.
3. I removed duplicate rows from the tag export and re-counted each tag.
5. I wrote tactical observations by phase of play and a goal-by-goal analysis.
6. I built a one-page Tableau dashboard from the cleaned tag data and the goal list.

---

## 5. Tagging Framework (Definitions Used)

### Panel 1: In Possession

| Tag | Definition |
|---|---|
| Build Up | The team initiates and develops an attacking phase from the defensive area through passing, player movement and coordinated positioning. |
| Progression | The team advances the ball towards the opposition goal through passing, dribbling or coordinated movement into available space. |
| Line Breaking Pass | A pass that bypasses one or more opposition players or defensive lines, allowing the team to progress the ball and gain a positional advantage. |
| Final Third Entry | The team enters the attacking third by passing or carrying the ball across the boundary into the area closest to the opposition goal. |
| Shot | An attempt to score by directing the ball towards the opposition goal, including shots on target, shots off target and blocked shots. |

### Panel 2: Out of Possession

| Tag | Definition |
|---|---|
| High Press | The team applies coordinated pressure in the opposition's defensive half or advanced areas to force errors, restrict build-up options or regain possession. |
| Defensive Block | The team organises its defensive shape in a **low block**, maintaining positional relationships and restricting the opposition's attacking space. Only low-block phases were tagged. |
| Interception | A player anticipates and cuts out an opposition pass, preventing it from reaching its intended target and potentially gaining possession. |
| Tackle | A defensive action in which a player attempts to dispossess an opponent who has control of the ball. |

### Panel 3: Transitions

| Tag | Definition |
|---|---|
| Ball Recovery | The team regains possession after the opposition has controlled the ball, through an interception, tackle, loose-ball recovery or another defensive action. |
| Counterattack | The team launches a rapid attacking action immediately after regaining possession, seeking to exploit unbalanced opposition positioning before the defence reorganises. |
| Counterpress | The team immediately applies pressure after losing possession, attempting to recover the ball before the opposition can establish controlled possession or launch an attack. |
| Transition to Defence | The moment possession is lost until the team regains the ball or sets its defensive shape. |

### Panel 4: Set Pieces

| Tag | Definition |
|---|---|
| Attacking Corner | A corner kick taken by the team to create a scoring opportunity. |
| Defensive Corner | The team's defensive response to an opposition corner, including marking, space protection, clearances and second-ball recovery. |
| Free Kicks | Every free kick awarded to the team, in any area of the pitch. |

### Result

| Tag | Definition |
|---|---|
| Goal | The ball fully crosses the goal line legally, including penalties and free-kick goals. Extra time I include. |

---

## 6. Dataset: Tagged Events (Nacsport)

| Event | France | Spain |
|---|---|---|
| Build Up | 59 | 51 |
| Progression | 82 | 58 |
| Shot | 29 | 19 |
| Final Third Entry | 137 | 76 |
| Line Breaking Pass | 22 | 13 |
| Interception | 13 | 6 |
| High Press | 12 | 5 |
| Defensive Block (low block) | 10 | 30 |
| Tackle | 38 | 59 |
| Ball Recovery | 60 | 56 |
| Counterattack | 15 | 10 |
| Counterpress | 8 | 11 |
| Transition to Defence | 45 | 33 |
| Goal | 3 | 5 |
| Attacking Corner | 12 | 2 |
| Defensive Corner | 2 | 12 |
| Free Kicks | 15 | 20 |

### Tableau Dashboard

I used Tableau (Tableau Public) to turn the tagged data into a one-page
dashboard. The data sources are `data/nacsport_tags_france_spain.csv`
(the cleaned Nacsport tag counts) and `data/goals_france_spain.csv` (the
eight goals).

The dashboard has four views:

1. **Event comparison.** France and Spain counts for all 17 tags, grouped by the four Nacsport panels (In Possession, Out of Possession, Transitions, Set Pieces).
2. **Efficiency.** Shots against goals for each team (France 29 shots and 3 goals, Spain 19 shots and 5 goals), with the conversion rate.
3. **Goals timeline.** The eight goals by match minute, coloured by origin: open play or dead-ball situation (corner sequence, free kick, penalty).
4. **Territory against defensive structure.** Final Third Entry compared with Defensive Block (low block) for each team.

The counts are raw event counts from a single match and are not rates. Line Breaking Pass, Final Third Entry and Defensive Block follow my own definitions (Section 5), so they should be read as descriptions of this analysis and not as official match statistics.

---

## 7. Goal-by-Goal Analysis

| # | Minute | Team | Scorer | Score | Origin |
|---|---|---|---|---|---|
| 1 | 11' | France | Millot | 1–0 | Corner sequence (second phase) |
| 2 | 18' | Spain | F. López | 1–1 | Patient build-up |
| 3 | 25' | Spain | F. López | 1–2 | Regain, long ball, cross |
| 4 | 28' | Spain | Baena | 1–3 | Free kick |
| 5 | 79' | France | Akliouche | 2–3 | Free kick |
| 6 | 90+3' | France | Mateta | 3–3 | Penalty after corner and VAR |
| 7 | 100' | Spain | Camello | 3–4 | Ball into the box behind France's loosened line |
| 8 | 120+1' | Spain | Camello | 3–5 | Rapid counterattack from goalkeeper distribution |


### Goal 1: France, 11' (1–0)
France built from the goalkeeper to the right back. A long ball reached the central midfield and then the right-sided midfielder, who stayed slightly ahead of the halfway line and played the ball into the final third while Spain's defenders were still positioned centrally. A Spanish defender stopped the French striker, and France won a corner. Olise's corner did not travel far and returned to him. His strike was missed by a Spanish defender who tried to block it, which allowed a French player to take the ball and score.

### Goal 2: Spain, 18' (1–1)
Spain won the ball with a tackle (15:40) while France's players were in Spain's half. The ball was passed between defenders and moved to the centre of the pitch, where Spain began to build up, with other players spreading wide in France's half. Their attempt to enter the final third failed, so they moved the ball back to the centre. Seeing many opponents in the centre and on the right, they switched to the left, where it was two French players against three Spanish players. As France moved towards that side, a Spanish midfielder played a quick low pass to a striker, who finished. The build-up lasted about 75 seconds.

### Goal 3: Spain, 25' (1–2)
The move began with a line-breaking pass towards a French striker who was already high up the pitch. A Spanish defender, running back towards his own area, intercepted it, turned and passed back through his defenders. When the ball reached the centre, the midfield was not available and two defenders stayed in the centre, so the ball was returned and a defender played a long, high ball to the right side near the corner. A Spanish midfielder received it and crossed from the corner area to the centre of the penalty area. Abel Ruiz's attempt was saved, and Fermín López arrived quickly to score the follow-up.

### Goal 4: Spain, 28' (1–3)
France built from the goalkeeper to a centre back and then to the right back, whose long ball to the centre was not received because a Spanish midfielder closed down the French midfielder before it landed. The ball bounced, a Spanish player headed it to a teammate, and a French midfielder then tackled to win it. As France tried to progress, a Spanish midfielder pressed and Spain counterattacked, changing direction immediately towards France's half. At the centre of the pitch Spain stopped and built up. A Spanish striker already in France's half moved towards the centre, which pulled French defenders with him. Spain played the ball into the space left behind to a nearby striker; two French defenders came quickly to stop him and one fouled him. Spain scored from the resulting free kick.

### Goal 5: France, 79' (2–3)
A Spanish midfielder tried to pass to a nearby teammate, but a French midfielder was covering that teammate, stepped between them and intercepted in Spain's half. As the French player looked to pass to a striker, Alex Baena fouled him and was booked. France were awarded a free kick, which Akliouche struck with his left foot; it deflected on its way in for France's goal.

### Goal 6: France, 90+3' (3–3)
France built from the goalkeeper and progressed into Spain's final third without strong opposition. Spain tried to tackle the French midfield, and Olise countered a Spanish striker, won the ball and played a long ball towards Spain's goal. Kalimuendo headed it, a defender deflected the header, and the ball went out of play for a corner. The corner delivery was so long that nobody touched it, the players protested, and the referee went to VAR. The decision was a penalty, which Mateta scored.

### Goal 7: Spain, 100' (3–4)
Camello's attempt at 97' was deflected by a French defender and went off target, and the ball was cleared forward. Spain regained possession, built up well and spread across the pitch. France's defenders had moved out of the defensive line and were working like midfielders, which loosened their defensive structure. Spain played the ball through to a striker inside the penalty box, who scored. A French 5-3-2 defensive shape, formed by a midfielder dropping into the defensive line, was observed seven seconds before the goal, at 98:58 (see the screenshot in Section 8).

### Goal 8: Spain, 120+1' (3–5)
Spain launched a rapid attack from the goalkeeper, who distributed the ball towards the centre of the pitch. A Spanish forward collected it and advanced quickly into France's half, using the space behind France's advanced defensive line. Two French defenders tried to recover, but one stopped pursuing the forward, who continued towards goal and scored. The attack lasted about nine seconds.

---

## 8. Tactical Observations by Phase (Match Time)

### France

| Match time | Phase | Observation |
|---|---|---|
| 0:47 | Build-up | Spain kicked off and France began to build from the centre backs, using short passes through the central midfield. When Spain pressed harder, France sometimes played the ball forward more directly. |
| 6:09 | Counterattack | After a Spanish throw-in from the right, a French defender challenged the ball carrier, recovered possession and helped France regain control. |
| 12:29 | Defensive intervention | Spain progressed through a half-space near France's final third. A French defender challenged the ball carrier and recovered possession, but Spain's midfield blocked France's next attempt to progress. |
| 13:04 | Counterpress | French midfielders applied immediate pressure to a Spanish ball carrier. France regained possession and progressed into the final third, and the move ended with the Spanish goalkeeper controlling the ball. |
| 80:55 | Decision-making | A French player received the ball in the penalty area with two Spanish defenders in front and a teammate available. The options were a direct shot through the right side, a carry or short pass between the defenders, or a pass through the left lane. My assessment is that the carry or short pass was the most promising option. |
| 86:57 | Space behind the line | After a French corner that did not produce a goal, Spain recovered the ball and advanced. French defenders tried to recover, and the Spanish attempt went off target. France had committed a large number of players forward. |
| 90:40 (extra time) | Decision-making | A French striker passed to a teammate inside the box whose route to goal was blocked. Another French teammate on the right had more space and was facing the goalkeeper. The receiver shot high over the goal. My assessment is that a pass to the free teammate offered a better chance. |
| 98:58 (extra time) | Defensive shape | France appeared in a 5-3-2 defensive shape because a midfielder dropped into the defensive line to form a back five, seven seconds before Spain's fourth goal. The team  line-up had four defenders on the pitch at that point, so the fifth player in the line came from midfield (screenshot below). |

### Spain

| Match time | Phase | Observation |
|---|---|---|
| 6:46 | Out of possession | Spain used close man-oriented marking when France advanced towards the Spanish final third. |
| 7:35 | Counterpress | Spanish midfielders pressed the ball carrier immediately after losing possession. The French player still managed to pass to a teammate. |
| 10:02 | Defensive shape | Spain appeared in a 4-4-2 shape, one minute before France's first goal. |
| 15:40 | Tackle | A Spanish player challenged the French ball carrier in Spain's half and won the ball. Spain moved possession away from its defensive half. |
| 15:57 | Build-up | Spain began the build-up that led to their first goal at 17:12. |
| 19:46 | Defensive shape | Spain appeared in a 5-4-1 defensive shape. |
| 41:18 | Defensive shape | Spain appeared in a 5-3-1 defensive shape, while leading 3–1. |
| 73:12 | Counterattack | A Spanish midfielder advanced against France's midfield, the ball reached another player, and Spain progressed towards the final third. |
| 73:15 | Shot | The move ended with a shot that went off target. My assessment is that a more central position before shooting would have given a better angle. |
| About 120:00 | Rapid attack | Spain's goalkeeper distributed the ball and a forward advanced behind France's line, nine seconds before Spain's fifth goal. |

The 4-4-2, 5-4-1, 5-3-1 and 5-3-2 shapes are recorded as temporary defensive structures observed at those moments, not as changes of starting formation.

### Defensive Shape Screenshots

Broadcast screenshots of each observed defensive shape, labelled with match time and score.

**Spain 4-4-2, 10:02 (0–0)**

**Spain 5-4-1, 19:46 (1–1)**

**Spain 5-3-1, 41:18 (Spain 3–1)**

**France 5-3-2, 98:58 (extra time, 3–3)**

*A France midfielder has dropped into the defensive line, forming a 5-3-2 shape, seven seconds before Spain's fourth goal.*

---

## 9. Key Findings

1. **Territory against efficiency.** France recorded 137 final third entries to Spain's 76 and 29 shots to 19, but scored three goals to Spain's five. Spain's five goals came from 19 attempts.
2. **Spain's defensive structure.** Spain tagged 30 low-block phases against France's 10, and the video shows Spain in 4-4-2, 5-4-1 and 5-3-1 defensive shapes.
3. **France's goals followed dead balls.** The 11' goal followed a corner, the 79' goal a free kick after a foul, and the 90+3' goal a penalty awarded after a corner and a VAR review. This matches France's 12 attacking corners against Spain's 2.
4. **Spain's goals came from open play, in four different ways.** A 75-second patient build-up that exploited a 3 v 2 on the left (18'), an interception followed by a long ball, a cross and a follow-up finish (25'), a ball played into the box when French defenders had left their line (100'), and a nine-second counterattack from goalkeeper distribution (120+1').
5. **Spain's burst.** Spain scored three goals between the 18th and 28th minutes.
6. **Transitions decided several goals.** Spain's goals at 25', 28', 100' and 120+1' began with a regain or a counter, and France's space behind their defensive line appears in the observations at 86:57 and at the fifth Spanish goal. Seven seconds before the fourth Spanish goal, France were observed in a 5-3-2 shape formed by a midfielder dropping into the defensive line (98:58).
7. **France's decisions in the penalty area.** At 80:55 a French player had three options, and the carry or short pass was the one I judged most promising. At 90:40 the receiver shot high over the goal under pressure while a teammate on the right had more space and was facing the goalkeeper.

---
## 9. Conclusion

France and Spain approached this final in different ways. France spent more time attacking and created more opportunities to enter the final third. They recorded 137 final third entries and 29 shots, compared with Spain's 76 entries and 19 shots. However, having more attacking opportunities did not translate into more goals. Spain scored five times from 19 attempts, while France managed three goals from 29 shots.

Spain also showed that their defensive organisation could change depending on the situation. At different stages of the match, they used 4-4-2, 5-4-1 and 5-3-1 shapes, while spending more time defending in a low block. Rather than trying to match France's attacking volume, Spain were able to defend deeper and look for opportunities to attack when possession was regained.

Looking at the goals, the difference between the teams becomes clearer. All three of France's goals came from dead-ball situations, while Spain found different ways to score, including patient build-up, a regain followed by a long ball and cross, and quick attacks that took advantage of the space behind France's defensive line.

For me, one of the biggest lessons from this match is that having more possession in attacking areas and taking more shots does not always mean a team is more effective. France had the greater attacking numbers, but Spain made better use of their chances and managed the important moments more successfully. Their defensive adjustments and ability to exploit spaces during transitions played an important part in the result.


## 10. Recommendations

**1. Pay more attention to defensive balance when attacking**

France committed players forward, but this sometimes left space behind their defensive line. This became particularly costly in extra time, when Spain found opportunities to attack that space and score. When pushing forward, teams should also consider how they will protect themselves if possession is lost.

**2. Make better use of attacking opportunities**

France had 29 shots but scored three goals, while Spain scored five from 19 attempts. It would be useful to review the decisions made in front of goal, especially when a player has the option to pass to a teammate in a better position. The situations at 80:55 and 90:40 are good examples from this match.

**3. Prepare for different defensive situations**

Spain did not stay in one defensive shape throughout the match. They were observed using 4-4-2, 5-4-1 and 5-3-1 structures. This highlights the importance of preparing players to adjust their positions according to the opponent's attacking movements and the current match situation.

**4. Give more attention to defending set pieces**

France scored all three goals from dead-ball situations. Spain's defending of corners and free kicks is therefore an area worth reviewing. Teams should pay attention not only to the first delivery but also to second balls and situations that develop after the initial clearance.

**5. Use video analysis to understand what happens before key moments**

The goals alone do not explain everything that happened in this match. Looking at the build-up to each goal, the defensive positions, the decisions made by players and the transitions before the attack provides more useful detail. Video analysis can help coaches identify these situations and use them when preparing for future matches.


- ## 11. Limitations

-   I tagged the match manually as the sole analyst, so there was no
    second analyst to check inter-rater reliability.
-   The footage is a YouTube broadcast, which meant I could not always
    assess the movement of players who were outside the camera frame.
-   I did not use fixed time thresholds when tagging Counterattack and
    Counterpress events.
-   Defensive Block includes low-block phases only. I did not tag
    mid-block or high-block phases, so these figures do not cover all of
    a team's defensive work.
-   I used my own definitions for Line Breaking Pass and Final Third
    Entry, so these figures cannot be compared directly with FIFA's
    measures.
-   Ball Recovery can overlap with Interception and Tackle, so the
    counts should not be added together.
-   The man-marking example and each defensive shape are individual
    observations; I did not track how often they occurred across the
    full match.

MWANAHAMISI JUMA

Mwanahamis050@gmail.com

Tableau : https://public.tableau.com/app/profile/mwanahamisi.juma/viz/EventComparisonView/EventComparisonView?publish=yes

Tableau : https://public.tableau.com/app/profile/mwanahamisi.juma/viz/ShootingEfficiency_17933652882070/Sheet2?publish=yes

Tableau : https://public.tableau.com/app/profile/mwanahamisi.juma/viz/GoalsTimeline/Sheet1?publish=yes

Tableau : https://public.tableau.com/app/profile/mwanahamisi.juma/viz/TerritoryAgainstDefensiveBlock/TerritoryAgaistDefensiveStructure?publish=yes

Linkedin profile : www.linkedin.com/in/mwanahamisi-juma-00576b394
