# France-U23-vs-Spain-U23-Tactical-Video-Analysis-of-the-Paris-2024-Olympic-Final-Using-Nacsport

Tactical video analysis of the Paris 2024 Olympic final (France U23 3–5 Spain U23) using Nacsport: 17 tagged event types, all 8 goals analysed and defensive shapes with screenshots.

**Competition:** Paris 2024 Olympic Games, Men's Football Gold Medal Match
**Date and venue:** 9 August 2024, Parc des Princes, Paris
**Result:** France 3–5 Spain (after extra time)
**Formations:** France 4-1-2-1-2 · Spain 4-2-3-1
**Tagging software:** Nacsport
**Dashboard software:** Tableau (Tableau Public)
**Author:** Mwanahamisi Juma

---

## 1. Executive Summary

I analysed the Paris 2024 Olympic final between France U23 and Spain U23 by tagging the whole match in Nacsport. I tagged 17 types of events for both teams across all 120 minutes, covering possession, defending, transitions and set pieces. I then wrote down what I saw in the video and went through all eight goals one by one.

What stood out:

- **France had more of the ball in attacking areas.** They had more final third entries (137 vs 76), more shots (29 vs 19) and more attacking corners (12 vs 2).
- **Spain were much more clinical.** They scored five goals from 19 shots. France scored three from 29.
- **Spain defended deeper.** They had 30 low-block phases against France's 10, and I saw them use 4-4-2, 5-4-1 and 5-3-1 shapes at different points in the match.
- **All three French goals came from dead-ball situations:** a corner, a free kick and a penalty.
- **Four of Spain's five goals came from open play:** a patient build-up, a regain followed by a long ball and a cross, a short pass that put a striker into the box against a weak French back line, and a fast counterattack.

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
| **Match source** | Full match from YouTube. I first tried to find it on Ligue 1+, which isn't available in my country, and on beIN Sports, where I couldn't find the full match. |
| **Analyst** | Me, tagging manually |
| **Time reference** | All times in this README are actual match time. I converted my Nacsport clip times using the kickoff (clip 07:03), the start of the second half (clip 61:04) and the start of extra time (clip 115:30). |

**Method**

1. I built a Nacsport code window with 15 buttons in four panels (In Possession, Out of Possession, Transitions and Set Pieces), plus Goal and Transition to Defence tags.
2. I tagged the full match for both teams.
3. I removed duplicate rows from the tag export and counted each tag again.
4. I wrote down my observations for each phase of play and analysed each goal.
5. I built a one-page Tableau dashboard from the cleaned tag data and the list of goals.

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
| Defensive Block | The team organises its defensive shape in a low block, maintaining positional relationships and restricting the opposition's attacking space. Only low-block phases were tagged. |
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
| Goal | The ball fully crosses the goal line legally, including penalties and free-kick goals. Extra time is included. |

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

I used Tableau Public to turn the tagged data into a one-page dashboard. It uses two files: `data/nacsport_tags_france_spain.csv` (my cleaned tag counts) and `data/goals_france_spain.csv` (the eight goals).

The dashboard has four views:

1. **Event comparison.** France and Spain counts for all 17 tags, grouped by the four Nacsport panels.
2. **Efficiency.** Shots against goals for each team (France 29 shots and 3 goals, Spain 19 shots and 5 goals), with the conversion rate.
3. **Goals timeline.** The eight goals by match minute, coloured by how they came about: open play or a dead-ball situation (corner, free kick or penalty).
4. **Territory against defensive structure.** Final Third Entry compared with Defensive Block (low block) for each team.

These are plain counts from one match, not rates. Line Breaking Pass, Final Third Entry and Defensive Block follow my own definitions (Section 5), so please read them as my view of this match and not as official statistics.

---

## 7. Goal-by-Goal Analysis

| # | Minute | Team | Scorer | Score | How it happened |
|---|---|---|---|---|---|
| 1 | 11' | France | Millot | 1–0 | Corner sequence (second phase) |
| 2 | 18' | Spain | F. López | 1–1 | Patient build-up |
| 3 | 25' | Spain | F. López | 1–2 | Regain, long ball, cross |
| 4 | 28' | Spain | Baena | 1–3 | Free kick |
| 5 | 79' | France | Akliouche | 2–3 | Free kick |
| 6 | 90+3' | France | Mateta | 3–3 | Penalty after a corner and a VAR check |
| 7 | 100' | Spain | Camello | 3–4 | Short pass and run into the box against a weak defensive line |
| 8 | 120+1' | Spain | Camello | 3–5 | Fast counterattack from the goalkeeper |

### Goal 1: France, 11' (1–0)
France started from the goalkeeper, who found the right back. From there a long ball went to the central midfield and then to the right-sided midfielder, who was standing slightly ahead of the halfway line. He played it into the final third while Spain's defenders were still sitting in the centre. A Spanish defender stopped the French striker, which gave France a corner. Olise took it, but it didn't go far and came back to him. He struck the ball, a Spanish defender tried to block it and missed, and a French player picked up the loose ball and scored.

### Goal 2: Spain, 18' (1–1)
Spain won the ball with a tackle at 15:40 while France's players were still in Spain's half. The ball went between defenders and moved to the centre of the pitch, where Spain started to build up while other players spread wide in France's half. They tried to enter the final third and couldn't, so they played back to the centre. The centre and the right side were crowded, so they moved to the left, where it was two French players against three Spanish players. When France shifted across to that side, a Spanish midfielder played a quick low pass to a striker, who finished. The whole build-up took about 75 seconds.

### Goal 3: Spain, 25' (1–2)
It started with a line-breaking pass towards a French striker who was already high up the pitch. A Spanish defender, running back towards his own area, cut it out, turned and passed back through his defenders. When the ball reached the centre, the midfield wasn't available and two defenders stayed in the centre, so the ball went back and a defender hit a long, high ball to the right side near the corner. A Spanish midfielder received it and crossed from the corner area into the middle of the penalty area. The first striker tried to finish but didn't score, and another Spanish striker arrived quickly and scored.

### Goal 4: Spain, 28' (1–3)
France started from the goalkeeper, then a centre back, then the right back, whose long ball into the centre was never received because a Spanish midfielder closed down the French midfielder before it landed. The ball bounced, a Spanish player headed it to a teammate, and a French midfielder tackled and won it. As France tried to move forward, a Spanish midfielder pressed and Spain counterattacked, switching direction straight away towards France's half. In the centre of the pitch Spain slowed down and built up. A Spanish striker who was already in France's half moved towards the centre, and that pulled French defenders with him. Spain saw the space he left and played the ball to a nearby striker. Two French defenders rushed to stop him, and one of them fouled him. Spain scored from the free kick.

### Goal 5: France, 79' (2–3)
A Spanish midfielder tried to pass to a nearby teammate, but a French midfielder was covering that teammate, stepped between them and intercepted in Spain's half. As he looked to pass to a striker, Alex Baena fouled him and got a yellow card. France had a free kick, and that free kick led to their goal.

### Goal 6: France, 90+3' (3–3)
France started from the goalkeeper and moved into Spain's final third without much pressure. Spain tried to tackle the French midfield, but Olise got the better of a Spanish striker, won the ball and played a long ball towards Spain's goal. A header sent it out of play for a corner. The corner was hit so long that nobody touched it. Players protested and the referee went to VAR. The decision was a penalty, and Mateta scored it.

### Goal 7: Spain, 100' (3–4)
When Spain got into France's final third, they first tried to score from a corner, but it didn't work. They won the ball back and built up again inside France's half. France kept switching between attacking and defending until one midfielder dropped back into the defensive line and the team ended up in a 5-3-2 shape (98:58, seven seconds before the goal, with the screenshot in Section 8). Even so, the back line was still weak. A Spanish striker took a short pass, ran deep into the penalty box and finished.

### Goal 8: Spain, 120+1' (3–5)
Spain attacked quickly from the goalkeeper, who played the ball towards the centre of the pitch. A Spanish forward picked it up and ran into France's half, using the space behind France's high defensive line. Two French defenders tried to catch him, but one stopped chasing, and the forward carried on and scored. The whole move took about nine seconds.

---

## 8. Tactical Observations by Phase (Match Time)

### France

| Match time | Phase | What I saw |
|---|---|---|
| 0:47 | Build-up | Spain kicked off, and France started building from the centre backs with short passes through central midfield. When Spain pressed harder, France sometimes went forward more directly. |
| 6:09 | Counterattack | After a Spanish throw-in on the right, a French defender challenged the ball carrier, won the ball back and helped France regain control. |
| 12:29 | Defensive intervention | Spain moved the ball through a half-space near France's final third. A French defender challenged the ball carrier and won the ball, but Spain's midfield stopped France's next attempt to move forward. |
| 13:04 | Counterpress | French midfielders pressed the Spanish ball carrier straight away. France won the ball and moved into the final third, and the move ended with the Spanish goalkeeper collecting the ball. |
| 80:55 | Decision-making | A French player received the ball in the penalty area with two Spanish defenders in front of him and a teammate available. He had three options: a direct shot through the right side, a carry or short pass between the defenders, or a pass through the left lane. My view is that the carry or short pass was the best option. |
| 86:57 | Space behind the line | After a French corner that didn't lead to a goal, Spain won the ball and moved forward. French defenders tried to get back, and the Spanish attempt went off target. France had pushed a lot of players forward. |
| 90:40 (extra time) | Decision-making | A French striker passed to a teammate inside the box, but his route to goal was blocked. Another French teammate on the right had more space and was facing the goalkeeper. The receiver shot high over the goal. My view is that passing to the free teammate would have given a better chance. |
| 98:58 (extra time) | Defensive shape | France went into a 5-3-2 defensive shape when a midfielder dropped into the defensive line to make a back five. This was seven seconds before Spain's fourth goal (screenshot below). |

### Spain

| Match time | Phase | What I saw |
|---|---|---|
| 6:46 | Out of possession | Spain marked closely, man to man, when France moved towards the Spanish final third. |
| 7:35 | Counterpress | Spanish midfielders pressed the ball carrier straight after losing the ball, but the French player still got a pass away. |
| 10:02 | Defensive shape | Spain defended in a 4-4-2 shape, about a minute before France's first goal. |
| 15:40 | Tackle | A Spanish player challenged the French ball carrier in Spain's half and won the ball. Spain then moved the ball out of their defensive half. |
| 15:57 | Build-up | Spain started the build-up that led to their first goal at 17:12. |
| 19:46 | Defensive shape | Spain defended in a 5-4-1 shape. |
| 41:18 | Defensive shape | Spain defended in a 5-3-1 shape while leading 3–1. |
| 73:12 | Counterattack | A Spanish midfielder moved forward against France's midfield, the ball reached another player, and Spain moved towards the final third. |
| 73:15 | Shot | The move ended with a shot that went off target. My view is that a more central position before shooting would have given a better angle. |
| About 120:00 | Fast attack | Spain's goalkeeper played the ball out and a forward ran in behind France's line. This was nine seconds before Spain's fifth goal. |

I recorded the 4-4-2, 5-4-1, 5-3-1 and 5-3-2 shapes as temporary defensive structures I saw at those moments. They are not changes to the starting formation.

### Defensive Shape Screenshots

Broadcast screenshots of each defensive shape, with the match time and score.

**Spain 4-4-2, 10:02 (0–0)**

![Spain 4-4-2 defensive shape at 10:02](images/Spain_4-4-2_10-02.jpg)

**Spain 5-4-1, 19:46 (1–1)**

![Spain 5-4-1 defensive shape at 19:46](images/Spain_5-4-1_19-46.jpg)

**Spain 5-3-1, 41:18 (Spain 3–1)**

![Spain 5-3-1 defensive shape at 41:18](images/Spain_5-3-1_41-18.jpg)

**France 5-3-2, 98:58 (extra time, 3–3)**

![France 5-3-2 defensive shape at 98:58](images/France_5-3-2_98-58.jpg)

*A France midfielder has dropped into the defensive line to make a 5-3-2, seven seconds before Spain's fourth goal.*

---

## 9. Key Findings

1. **More attacking numbers didn't mean more goals.** France had 137 final third entries to Spain's 76 and 29 shots to 19, but Spain scored five and France scored three.
2. **Spain defended deep.** They had 30 low-block phases against France's 10, and I saw 4-4-2, 5-4-1 and 5-3-1 shapes.
3. **France's goals all came from dead balls.** The 11' goal came after a corner, the 79' goal from a free kick after a foul, and the 90+3' goal from a penalty after a corner and a VAR check. That fits with France's 12 attacking corners against Spain's 2.
4. **Spain scored from open play in four different ways.** A 75-second patient build-up that used a 3 v 2 on the left (18'), an interception followed by a long ball, a cross and a follow-up finish (25'), a short pass that put a striker into the penalty box against a weak French back line (100'), and a nine-second counterattack from the goalkeeper (120+1').
5. **Spain scored three goals between the 18th and 28th minutes.**
6. **Transitions mattered.** Spain's goals at 25', 28', 100' and 120+1' all started with winning the ball back or a counter. I also noted the space behind France's defensive line at 86:57 and in the build-up to Spain's fifth goal. Seven seconds before Spain's fourth goal, France had dropped a midfielder into the back line to make a 5-3-2 (98:58).
7. **France's decisions in the box.** At 80:55 a French player had three options, and the carry or short pass was the one I liked most. At 90:40 the receiver shot high over the goal under pressure while a teammate on the right had more space and was facing the goalkeeper.

---

## 10. Conclusion

France and Spain went about this final in very different ways. France spent more time attacking and got into the final third more often, with 137 entries and 29 shots against Spain's 76 entries and 19 shots. But all that attacking didn't turn into more goals. Spain scored five times from 19 shots, and France scored three from 29.

Spain also changed their defensive shape depending on the situation. At different points they used 4-4-2, 5-4-1 and 5-3-1 shapes, and they spent more time defending in a low block. They didn't try to match France's attacking volume. They defended deeper and went for chances when they won the ball back.

The goals show the difference even more clearly. All three of France's goals came from dead-ball situations. Spain found different ways to score: a patient build-up, a regain followed by a long ball and a cross, a short pass against a weak back line, and a quick counterattack that used the space behind France's defensive line.

For me, the biggest lesson from this match is that more attacking numbers don't always mean a team is more effective. France had more of the ball in attacking areas and more shots, but Spain made better use of their chances and handled the important moments better. Their defensive adjustments and the way they used space in transitions played a big part in the result.

---

## 11. Recommendations

**1. Keep a better balance between attacking and defending**

France pushed players forward, and that sometimes left space behind their defensive line. It was most costly at 120+1', when Spain attacked that space and scored. When a team pushes forward, it also needs a plan for what happens if it loses the ball.

**2. Make better use of attacking chances**

France had 29 shots and scored three goals, while Spain scored five from 19. It would help to review the decisions made in front of goal, especially when a teammate was in a better position. The moments at 80:55 and 90:40 are good examples from this match.

**3. Prepare for different defensive situations**

Spain didn't stay in one defensive shape. I saw 4-4-2, 5-4-1 and 5-3-1 structures. Players need to be ready to adjust their positions depending on how the opponent attacks and what the match situation is.

**4. Pay more attention to defending set pieces**

France scored all three of their goals from dead-ball situations, so Spain's defending of corners and free kicks is worth reviewing. Teams should look beyond the first delivery to second balls and what happens after the first clearance.

**5. Use video analysis to look at what happens before key moments**

The goals alone don't tell the full story of this match. Looking at the build-up to each goal, the defensive positions, the players' decisions and the transitions before an attack gives much more useful detail. Video analysis can help coaches spot these situations and use them when preparing for future matches.

---

## 12. Limitations

- I tagged the match manually and on my own, so nobody checked my tagging for consistency.
- The footage is a YouTube broadcast, so I couldn't always see players who were outside the camera frame.
- I didn't use fixed time limits when tagging Counterattack and Counterpress.
- Defensive Block only includes low-block phases. I didn't tag mid-block or high-block phases, so these numbers don't cover all of a team's defending.
- I used my own definitions for Line Breaking Pass and Final Third Entry, so these counts reflect how I read the match.
- Ball Recovery can overlap with Interception and Tackle, so these counts shouldn't be added together.
- The man-marking example and each defensive shape are single observations. I didn't track how often they happened across the whole match.

---

## Contact

**Mwanahamisi Juma**
Mwanahamis050@gmail.com

**Tableau dashboards**

- [Event Comparison View](https://public.tableau.com/app/profile/mwanahamisi.juma/viz/EventComparisonView/EventComparisonView?publish=yes)
- [Shooting Efficiency](https://public.tableau.com/app/profile/mwanahamisi.juma/viz/ShootingEfficiency_17933652882070/Sheet2?publish=yes)
- [Goals Timeline](https://public.tableau.com/app/profile/mwanahamisi.juma/viz/GoalsTimeline/Sheet1?publish=yes)
- [Territory Against Defensive Structure](https://public.tableau.com/app/profile/mwanahamisi.juma/viz/TerritoryAgainstDefensiveBlock/TerritoryAgaistDefensiveStructure?publish=yes)

**LinkedIn:** [linkedin.com/in/mwanahamisi-juma-00576b394](https://www.linkedin.com/in/mwanahamisi-juma-00576b394)
