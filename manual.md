# XFutebol: a Chess-like board Game.

## Table of Contents
1. [Game Overview](#1-game-overview)
   1. [Objective](#11-objective)
   2. [Game Components](#12-game-components)
   3. [Player Types](#13-player-types)
2. [Game Setup](#2-game-setup)
   1. [Board Configuration](#21-board-configuration)
   2. [Team Composition](#22-team-composition)
   3. [Goal Area](#23-goal-area)
   4. [Penalty Area](#24-penalty-area)
   5. [Turn Structure](#25-turn-structure)
   6. [Starting the Game](#26-starting-the-game)
3. [Player Movement and Actions](#3-player-movement-and-actions)
   1. [Move Action](#31-move-action)
   2. [Pass Action](#32-pass-action)
   3. [Long Pass Action](#33-long-pass-action)
   4. [Challenge Action](#34-challenge-action)
   5. [Dribble Action](#35-dribble-action)
   6. [Sprint Action](#36-sprint-action)
   7. [Shoot Action](#37-shoot-action)
   8. [Long Shoot Action](#38-long-shoot-action)
4. [Special Player Roles](#4-special-player-roles)
   1. [Goaler](#41-goaler)
   2. [Dribbler](#42-dribbler)
   3. [Long Experts](#43-long-experts)
5. [Scoring and Goalkeeping](#5-scoring-and-goalkeeping)
   1. [Scoring Mechanism](#51-scoring-mechanism)
   2. [Goalkeeper's Role](#52-goalkeepers-role)
6. [Fouls and Penalties](#6-fouls-and-penalties)
   1. [Defining a Foul](#61-defining-a-foul)
   2. [Consequences of Fouls](#62-consequences-of-fouls)
   3. [Free Kick Rules](#63-free-kick-rules)
   4. [Penalty Kick Rules](#64-penalty-kick-rules)
7. [Special Game Scenarios](#7-special-game-scenarios)
   1. [Empty Goal Scenario](#71-empty-goal-scenario)
   2. [Barrier Formation and Challenges](#72-barrier-formation-and-challenges)
8. [Game Dynamics and Balance](#8-game-dynamics-and-balance)
   1. [Team Limits on SPRINT and LONG Actions](#81-team-limits-on-sprint-and-long-actions)
   2. [Energy and Stamina System](#82-energy-and-stamina-system)
9. [Winning the Game](#9-winning-the-game)
   1. [Golden Goal](#91-golden-goal)
   2. [Two Halves with Total Score](#92-two-halves-with-total-score)
   3. [Number of Goals](#93-number-of-games)
   4. [Movement Count Rule](#94-movement-count-rule)
10. [Miscellaneous Rules](#10-miscellaneous-rules)
    1. [Simplified Version: Specific Attribute Values](#101-simplified-version-specific-attribute-values-for-player-types)
11. [Final Thoughts and Future Developments](#11-final-thoughts-and-future-developments)
12. [Further Analysis](#12-further-analysis)
    1. [MOVE Action](#121-move-action)
    2. [PASS Action](#122-pass-action)
    3. [LONG PASS Action](#123-long-pass-action)
    4. [SHOOT Action](#124-shoot-action)
    5. [LONG SHOOT Action](#125-long-shoot-action)
    6. [DRIBBLE Action](#126-dribble-action)
    7. [CHALLENGE Action](#127-challenge-action)
    8. [SPRINT Action](#128-sprint-action)

## **1. Game Overview**
### **1.1 Objective**
*Players compete to score goals by strategically moving pieces on a chessboard-like soccer field. The game combines elements of chess and soccer, requiring tactical thinking and careful planning.*

### 1.2 Game Components

The game components are designed to facilitate clear and effective gameplay. They include:

- **Two Chess Boards:** Aligned side-by-side to create a 16x8 grid. This forms the playing field.
- **Pieces:** Representing different player types, each with unique abilities and roles in the game.
- **Ball:** Serves as the primary game object and is also used to mark the position of fouls on the field.
- **Markers:** 
  - **Foul Markers:** The ball is used to indicate the location of fouls.
  - **Card Markers:** The number of fouls and subsequent cards (yellow and red) can be tracked on the match record form using a pen. Alternatively, yellow and red pawns from a Ludo game can be used to visually represent accumulated cards.
  - **Area Markers:** Blue pawns from a Ludo game can be used to denote the penalty area limits, and green pawns for the goal area.
  - **Sprint Markers:** Sprints used by each team can be tracked on the match record form with a pen.
- **Forms:** For setting up the game, recording match events during play, and summarizing post-match information.
- **Erasable Pen:** For marking point boosts in penalty and goal areas, drawing areas on the board, and filling out forms.

These components collectively enhance the strategic and interactive elements of the game, offering a comprehensive and engaging gameplay experience.

### **1.3 Player Types**
- **Attackers (Forwards):** Fast, goal-oriented players.
- **Defenders:** Strong, defense-focused players.
- **Midfielders:** Versatile players adept in both offense and defense.
- **Goal Keepers:** Specialized in defending the goal, with the option to join attacks.
- **Dribblers:** Skilled in evading opponents and maintaining ball control.
- **Goalers:** Focused on scoring and long-range shots.
- **Long Experts:** Specialized in executing uninterceptible long passes and shots.




## 2. Game Setup

### 2.1 Board Configuration
*Align two chess boards to form a 16x8 grid, representing an extended soccer field.*

### 2.2 Team Composition
*Each team consists of 11 players. At the beginning of the game, players select two special pieces from each of the following categories: Dribblers, Goalers, and Long Experts. The remaining five players include the Goal Keeper, along with a combination of Attackers, Defenders, and Midfielders.*

#### 4-3-3 Formation
For a 4-3-3 formation on a 16x8 board, excluding the Goal Keeper (01):

| Number | Player Type | Starting Position |
|--------|-------------|-------------------|
| 02     | Defender    | C2                |
| 03     | Defender    | F2                |
| 04     | Defender    | D3                |
| 05     | Defender    | G3                |
| 06     | Midfielder  | E4                |
| 08     | Midfielder  | B5                |
| 10     | Midfielder  | H5                |
| 07     | Attacker    | D7                |
| 09     | Attacker    | F7                |
| 11     | Attacker    | E8                |

#### 5-3-2 Formation
Alternatively, for a 5-3-2 formation:

| Number | Player Type | Starting Position |
|--------|-------------|-------------------|
| 02     | Defender    | B2                |
| 03     | Defender    | C3                |
| 04     | Defender    | F3                |
| 05     | Defender    | G2                |
| 06     | Defender    | E2                |
| 08     | Midfielder  | D4                |
| 10     | Midfielder  | E5                |
| 07     | Midfielder  | F6                |
| 09     | Attacker    | C7                |
| 11     | Attacker    | H7                |

These formations strategically position players across rows 2 to 8, with defenders in rows 2 and 3, midfielders in rows 4 to 6, and attackers in rows 7 and 8. The placement of players is varied to avoid perfect alignment, creating a more dynamic and realistic setup for the game.

### 2.3 Goal Area
- **Definition:** The Goal Area is a crucial zone on the game board, located at each end of the board, surrounding the goal.
- **Location:** For a 16x8 board, the Goal Area is defined as the squares C1-F1, C2-F2, of both boards.
- **Significance:** The Goal Keeper usually occupies this area. If the Goal Keeper is outside of the Goal Area, the goal is considered empty, increasing the chance of scoring.

### Scoring a Goal:

- **Eligibility:** Any piece on the field can attempt a shot towards the Goal Area.
- **Mechanism:** A goal is scored when the ball successfully crosses any of the squares designated as the goal. For the 16x8 board, these are squares D1-E1 fo both boards. This is determined by the shooter's ability to outmatch the goalkeeper's defense, based on their respective attributes.
- **Goalkeeper's Defense:** The Goal Keeper attempts to defend against shots aimed at these specific goal squares. The outcome of this defense is determined by comparing the relevant attributes of the shooter and the goalkeeper.
- **Player Awareness:** Players should be acutely aware of the Goal Area on their own board. It is important for attackers to recognize opportunities to score, and for the goalkeeper to be strategically positioned for effective defense.

### 2.4 Penalty Area
- **Definition:** The Penalty Area is a larger zone that includes the Goal Area and additional squares directly in front of the goal.
- **Location:** The Penalty Area extends to squares B1-G1, B4-G4 for the both boards.
- **Importance:** Fouls committed by the defending team in the Penalty Area result in a penalty kick for the attacking team.
- **Player Awareness:** Understanding the boundaries and strategic significance of the Penalty Area is essential for effective gameplay.

### 2.5 Turn Structure
- **Two Movements per Turn:** In each turn, a player can make two movements.
- **Mandatory MOVE:** Out of these two movements, at least one must be a MOVE action. The other can be any action, including another MOVE.
- **Strategic Consideration:** This rule encourages players to strategically plan their movements and actions, balancing between advancing their pieces and executing specific actions like Pass, Dribble, or Shoot.

### 2.6 Starting the Game
*The game starts with a coin toss to decide the starting team.*

### 2.7 Preparation of Markers

- Follow the instructions in section 1.2 to prepare the markers for the game. The primary method involves:
  - **Using an Erasable Pen:** 
    - For drawing area markers directly on the board, including the penalty and goal areas.
    - For marking the center of the board to indicate the initial position of the ball.
  - **Using the Match Record Form:** 
    - To keep track of the number of fouls, cards (yellow and red), and sprints during the match. 

- **Alternative Using Ludo Pawns:** 
  - If available, Ludo game pawns can be used as an alternative method for visual markers:
    - **Yellow and Red Pawns:** To represent accumulated yellow and red cards.
    - **Blue and Green Pawns:** For marking the penalty and goal areas on the board.

### 2.8 Defining the Winning Style
*Before beginning the game, players must agree on the winning style.* They can choose between the following options:
- **Golden Goal:** The game ends immediately when the first goal is scored.
- **Two Halves with Total Score:** The winner is determined by the highest total score at the end of both halves, with a penalty shootout as a tiebreaker in case of a draw.
- **Number of Goals:** The game continues until a team reaches a predetermined number of goals.
- **Movement Count Rule:** If no goals are scored within a set number of movements, the winner is decided by a penalty shootout.

Selecting the winning style is crucial as it sets the tone and strategy for the entire game. Players should consider their team's strengths and preferred tactics when choosing the winning style.

## 3. Player Movement and Actions
### 3.1 Move Action

*Players move their pieces according to the type's movement ability.* 
- **Attackers:** Move 2 squares forward, 1 backward, 1 to the sides.
- **Defenders:** Move 1 square in any direction.
- **Midfielders:** Move 2 squares to the sides, 1 forward, 1 backward.
- **Goal Keeper:** Move 1 square in any direction; moving out of the goal area risks leaving the goal unguarded.
- **Dribbler:** Move 2 squares forward, 1 backward, 1 to the sides, with enhanced dribbling capability.
- **Goaler:** Move 2 squares forward, 1 backward, 1 to the sides, focused on advancing towards the opponent's goal.
- **Long Experts:** Their MOVE action follows the movement pattern of their original position as defenders, attackers, or midfielders. This categorization determines their standard movement range.

### 3.2 Pass Action
- **Mechanism:** Transfer the ball to a teammate within line of sight following the square distance rules for the movements of each piece.
- **Distance:** A simple pass extends up to 2 times the standard movement range of the piece. For example, an attacker can pass the ball up to 4 squares forward.
- **Outcome:** Successful pass if the ball reaches a teammate; otherwise, potential interception by an opponent.

### 3.3 Long Pass Action
- **Mechanism:** Long Experts can send the ball to a distant teammate. They have the unique ability to perform both straight and curved long passes.
  - **Curved Pass:** Requires selecting an intermediary square where the curve starts and a final target square. Allows bypassing obstacles and reaching targets not in direct line of sight.
- **Distance:** A long pass extends up to 3 times the standard movement range of the piece.
- **Outcome:** Successful long pass if the ball reaches a teammate; risk of interception or misdirection increases with distance and complexity of the trajectory.

### 3.4 Challenge Action

#### Mechanism:
- The outcome of a CHALLENGE action is determined by comparing a combination of attributes for the challenging piece and the opponent who has the ball or is the intended recipient of the ball.
  - **Challenger's Attributes:** Speed + Strength + Defense.
  - **Opponent's Attributes (Ball Holder or Target):** Speed + Strength + Skill.

#### Conditions for CHALLENGE:
- A CHALLENGE can be attempted in the following scenarios:
  - To intercept the ball coming from a SHOOT action.
  - To intercept the ball coming from a PASS action.
  - To intercept the ball coming from a LONG SHOOT action.
- **Exception:** LONG PASS actions cannot be intercepted by a CHALLENGE.

#### Distance:
- The CHALLENGE action can be attempted on an adjacent square where the opponent with the ball is located or in the path of the ball during a SHOOT, PASS, or LONG SHOOT action.
  - **Example:** A Defender (D) next to an Attacker (A) who has the ball, or in the path of a shot, can attempt to take the ball with a CHALLENGE.

#### Outcome:
- **Successful Challenge:**
  - If the total of the challenger's Speed, Strength, and Defense is greater than the total of the ball holder's Speed, Strength, and Skill.
  - **Notation:** `Speed + Strength + Defense > Speed + Strength + Skill`
- **Failed Challenge:**
  - If the ball holder's total of Speed, Strength, and Skill is equal to or greater than the total of the challenger's Speed, Strength, and Defense.
  - **Notation:** `Speed + Strength + Skill ≥ Speed + Strength + Defense`
- **Tie:**
  - If there is a tie, the play continues normally, with the ball following its intended path.

### Notes:
- The CHALLENGE action is a critical defensive tactic in XFutebol, enabling players to intervene in key moments to regain possession or prevent scoring.
- The ability to challenge SHOOT, PASS, and LONG SHOOT actions introduces a layer of strategic defense and quick decision-making.
- The rule for a tie, allowing the play to continue, adds a dynamic element to the game, ensuring that the action remains fluid and unpredictable.

### 3.5 Dribble Action

#### Mechanism:
- The outcome of a DRIBBLE action is determined by comparing a combination of attributes for the dribbling piece and the adjacent opponent.
  - **Dribbler's Attributes:** Speed + Skill.
  - **Opponent's Attributes:** Speed + Defense.

#### Conditions for DRIBBLE:
- A DRIBBLE can be attempted when an opposing player is in an adjacent square.
- The action is used to evade the opponent and maintain possession of the ball.

#### Distance:
- The DRIBBLE action is executed within an adjacent square to the dribbling piece.
  - **Example:** A Midfielder (M) with the ball can attempt to dribble past an adjacent Defender (D).

#### Outcome:
- **Successful Dribble:**
  - If the dribbler's combined Speed and Skill is greater than the opponent's combined Speed and Defense.
  - **Notation:** `Speed + Skill > Speed + Defense`
- **Failed Dribble:**
  - If the opponent's combined Speed and Defense is equal to or greater than the dribbler's combined Speed and Skill.
  - **Notation:** `Speed + Defense ≥ Speed + Skill`
- **Tie:**
  - If there is a tie, the dribbling piece maintains possession but fails to advance past the opponent.

### Notes:
- The DRIBBLE action is a crucial maneuver in XFutebol for players to advance the ball and evade opponents, especially in tightly contested areas.
- This action highlights the importance of individual player attributes, particularly Speed and Skill, in successful ball control and evasion.
- Executing effective DRIBBLE actions requires strategic consideration of both the dribbler's and the adjacent opponent's strengths and weaknesses.

### 3.6 Sprint Action

#### Mechanism:
- The SPRINT action doubles the movement capacity of a piece for one turn.
  - **Effect on Piece:** Increases the range of movement, allowing the piece to cover more ground on the field.

#### Conditions for SPRINT:
- SPRINT can be used in any situation where rapid movement or repositioning is desired.
- **Strategic Application:** Ideal for advancing towards the goal, retreating for defense, or moving to a key position on the field.

#### Distance:
- The SPRINT action allows a piece to move up to double its standard movement range in a single turn.
  - **Example:** A Midfielder (M) who normally moves 2 squares in any direction can move up to 4 squares in any direction with a SPRINT.

#### Outcome:
- **Effective Sprint:** Successfully covers the intended distance, allowing for rapid repositioning or advancement.
- **Limitation and Recovery Period:**
  - **Initial Limit:** Each team can use SPRINT 3 times per half without penalties.
  - **Additional SPRINTs:** Teams can opt to use more than 3 SPRINTs. However, for each SPRINT beyond the third, the piece used will be temporarily removed from the field for a 90-second recovery period to simulate fatigue.

### Notes:
- The SPRINT action adds a dynamic and fast-paced element to XFutebol, reflecting the agility and speed found in actual soccer.
- The ability to use additional SPRINTs beyond the initial limit introduces a trade-off between immediate tactical gain and short-term player unavailability, requiring careful strategic planning.
- Effective use of SPRINTs can significantly influence the game's momentum, making it a potent tool in a team's tactical arsenal.

### 3.7 Shoot Action

#### Mechanism:
- The outcome of a SHOOT action is determined by comparing the shooter's attributes against the goalkeeper's attributes.
  - **Shooter's Attributes:** Goal + Skill.
  - **Goalkeeper's Attributes:** Defense + Skill.

#### Distance:
- The Shoot action extends up to the standard movement range of the piece.
  - **Example:** An Attacker (A), who normally moves 2 squares forward, can shoot from up to 2 squares away from the goal.

#### Scoring Boosts:
  - **Penalty Area Boost:** Shooting from the penalty area adds +15 points to the base shoot score.
  - **Goal Area Boost:** Shooting from the goal area adds +25 points to the base shoot score.

#### Outcome:
- **Goal Scored:**
  - If the total of the shooter's Goal and Skill (plus any applicable boosts) is greater than the total of the goalkeeper's Defense and Skill.
  - **Notation:** `(Goal + Skill + Boosts) > (Defense + Skill)`
- **Saved or Deflected by Goalkeeper:**
  - If the goalkeeper's total of Defense and Skill is equal to or greater than the total of the shooter's Goal and Skill (plus any boosts).
  - **Notation:** `(Defense + Skill) ≥ (Goal + Skill + Boosts)`


## Scoring Table for Regular Shoot Action

| Feature             | Description                                          | Points Scheme                             |
|---------------------|------------------------------------------------------|-------------------------------------------|
| **Base Shoot**      | Using Goal + Skill of the player.                    | Base points: Player's Goal + Skill        |
| **Penalty Area Boost**| Shooting from the penalty area.                      | +15 points to base shoot                  |
| **Goal Area Boost** | Shooting from the goal area.                         | +25 points to base shoot                  |
| **Scoring Condition** | Comparing total points against GK's Defense + Skill. | Goal if Shooter's total > GK's total      |
| **Save Condition**  | If GK's total points are equal to or higher.         | Save or deflection by the GK              |

### Notes:
- The SHOOT action is a critical part of XFutebol gameplay, representing a direct attempt to score a goal.
- The addition of Strength and Skill for the shooter and Speed for the goalkeeper adds depth to the strategy, making the success of shots more nuanced and dependent on a broader range of player attributes.
- Players need to consider the positioning and attributes of their shooters and the opposing goalkeeper to maximize the chances of scoring successfully.


### 3.8 Long Shoot Action

- **Mechanism:** Long Experts can perform a Long Shoot action, using their Goal, Skill, and Strength. This action includes both straight and curved shots.
  - **Curved Shoot:** Involves choosing an intermediary square for the curve and the final goal square. Enhances the ability to score from angles not directly aligned with the goal. Adds a boost of +20 points to the base long shoot score.
- **Distance:** The Long Shoot action extends up to 3 times the standard movement range of the piece.
- **Scoring Boosts:**
  - **Penalty Area Boost:** Shooting from the penalty area adds +15 points to the base or curved long shoot score.
  - **Goal Area Boost:** Shooting from the goal area adds +25 points to the base or curved long shoot score.
- **Outcome:**
  - **Scoring Condition:** If the total score (Goal + Skill + Strength + applicable boosts) is greater than the Goalkeeper's (Defense + Skill + Speed), a goal is scored.
  - **Save Condition:** If the Goalkeeper's total points (Defense + Skill + Speed) are equal to or higher than the shooter's total score, the goalkeeper saves or deflects the shot.


## Scoring Table for Long Shoot Action

| Feature               | Description                                          | Points Scheme                                   |
|-----------------------|------------------------------------------------------|-------------------------------------------------|
| **Base Long Shoot**   | Using Goal + Skill + Strength of the player.         | Base points: Player's Goal + Skill + Strength   |
| **Curved Shot Boost** | Adding a curve to the shot.                          | +20 points to base long shoot                   |
| **Penalty Area Boost**| Shooting from the penalty area.                      | +15 points to base or curved long shoot         |
| **Goal Area Boost**   | Shooting from the goal area.                         | +25 points to base or curved long shoot         |
| **Scoring Condition** | Comparing total points against GK's Defense + Skill + Speed. | Goal if Shooter's total > GK's total       |
| **Save Condition**    | If GK's total points are equal to or higher.         | Save or deflection by the GK                    |

## 4. Special Player Roles
### 4.1 Goaler
Enhanced shooting abilities, beneficial for scoring.

### 4.2 Dribbler
Superior in evading opponents, ideal for advancing the ball.

### 4.3 Long Experts
Specialized in executing uninterceptible long-range passes and shots. Their role is crucial for strategic positioning and creating unexpected scoring opportunities.

## 5. Scoring and Goalkeeping
### 5.1 Scoring Mechanism
Goals are scored by successfully executing a Shoot action against the opponent's goal.

### 5.2 Goalkeeper's Role
Key in defending the goal. Can move out of the goal area but risks leaving the goal unguarded.

#### 1. Goal Scoring Attempt (Shot or Penalty):
- **Mechanism:** The outcome is determined by comparing the shooter's and the goalkeeper's attributes, with additional boosts for shots from specific areas.
- **Attributes:** 
  - **Shooter's Attributes:** Goal + Skill (plus any applicable boosts for shots from the penalty or goal area).
  - **Goalkeeper's Attributes:** Defense + Skill.

#### 2. Outcome Determination:
- **Goal Scored:**
  - Occurs if the shooter's combined attributes (Goal + Skill + Boosts) significantly exceed the goalkeeper's (Defense + Skill).
  - *Example:* `(Goal + Skill + Boosts) > (Defense + Skill + 20)`

- **Save with Rebound:**
  - Happens if the shooter's attributes slightly exceed or are nearly equal to the goalkeeper's, resulting in the goalkeeper deflecting the ball, but not securing it.
  - *Example:* `(Defense + Skill) ≤ (Goal + Skill + Boosts) ≤ (Defense + Skill + 20)`

- **Clean Save:**
  - Occurs if the goalkeeper's attributes are significantly higher than the shooter's, allowing the goalkeeper to secure the ball without a rebound.
  - *Example:* `(Goal + Skill + Boosts) < (Defense + Skill)`

### Notes:
This updated section now includes a clear framework for determining whether a goal attempt results in a Score, a Save with Rebound, or a Clean Save. The examples provide a straightforward way to calculate the outcome based on the shooter's and the goalkeeper's attributes, including any additional boosts for shots taken from specific areas of the field. This should enhance the game's strategic depth and the importance of positioning and player selection in goal attempts.

## 6. Fouls and Penalties
### 6.1 Defining a Foul
Occurs when a player's MOVE targets an opponent's square, or an unsuccessful CHALLENGE is made.

### 6.2 Consequences of Fouls

- **Team-Based Fouls Count:** Fouls are counted collectively for the entire team rather than individually for each piece.
- **Yellow Card:** The team receives a yellow card upon accumulating 3 fouls. This acts as a warning and may influence the team's strategic play.
- **Red Card:** If a team accumulates 4 or more fouls, they are issued a red card. Consequently, the team must choose one of their pieces to be removed from the game, representing a significant strategic disadvantage.

### 6.3 Free Kick Rules
- **Mechanism:** Shooter's Skill and Goal vs. highest Defense in defender's barrier.
- **Outcome:**
  - If Skill + Goal > Defense: Successful kick.
  - If Defense ≥ Skill + Goal: Defenders block or deflect the kick.


### 6.4 Penalty Kick Rules
- **Mechanism:** Shooter's Goal feature vs. goalkeeper's Defense.
- **Outcome:**
  - If Goal > Defense: Goal is scored.
  - If Defense ≥ Goal: Goalkeeper saves the penalty.

## 7. Special Game Scenarios
### 7.1 Empty Goal Scenario
If the goalkeeper is not in the goal area and a goal is attempted, it's likely to succeed.

### 7.2 Barrier Formation and Challenges
Defenders can form a barrier and challenge LONG actions after a free kick.

## 8. Game Dynamics and Balance
### 8.1 Team Limits on SPRINT and LONG Actions
Restrictions to prevent overuse and maintain strategic depth. Maximum of 3 Sprints per half. For the time being, no restrictions for LONG actions.

## 9. Winning the Game
### 9.1 Golden Goal
First goal wins the game. The length is 15 minutes, with a penalty shootout as a tiebreaker.

### 9.2 Two Halves with Total Score
The highest score after two halves wins, with a penalty shootout as a tiebreaker. The length of each half is 15 min each.

### 9.3 Number of Goals
The first team to reach a predetermined number of goals wins.

### 9.4 Movement Count Rule
If no goals are scored within a set number of movements, 50 by default, the winner is decided by a penalty shootout.

## 10. Miscellaneous Rules
The following table defines the feature values of each of the Player Piece types.

### 10.1 Simplified Version: Specific Attribute Values for Player Types

| Player Type  | Speed | Skill | Strength | Goal | Defense |
|--------------|-------|-------|----------|------|---------|
| **Attackers**    | 70    | 80    | 60       | 90   | 40      |
| **Defenders**    | 50    | 60    | 80       | 40   | 85      |
| **Midfielders**  | 70    | 75    | 65       | 75   | 70      |
| **Goal Keeper**  | 50    | 70    | 60       | 50   | 90      |
| **Dribbler**     | 85    | 85    | 55       | 80   | 45      |
| **Goaler**       | 60    | 70    | 70       | 85   | 60      |
| **Long Experts** | 75    | 80    | 70       | 85   | 50      |



This manual provides a comprehensive guide to playing Futebol Chess, covering all aspects of the game from setup to gameplay mechanics. The inclusion of special player types like Long Experts adds strategic depth, and the specific attribute values for the simplified version make it accessible for beginners.

## 11. Final Thoughts and Future Developments

This manual provides a comprehensive guide to Futebol Chess, a game that combines the strategic elements of chess with the dynamic gameplay of soccer. Whether you are a seasoned strategist or a casual player, Futebol Chess offers a unique and engaging experience. Enjoy the game, and may the best strategist win!

### Future Developments
As Futebol Chess evolves, there is potential for the game to incorporate individual scores for each piece, rather than generalized scores for piece types. This advancement could lead to the introduction of unique characters or players, each with their distinct set of attributes. For example:

- **Action Heroes or Iconic Soccer Players:** Future versions of the game might feature individual characters, such as famous soccer players or action heroes, each with unique abilities and scores. This would add a layer of personalization and depth to the game, allowing players to build teams based on individual strengths and strategies.

- **Customizable Player Abilities:** This development could also open the door to more customizable gameplay, where players can adjust the attributes of their pieces according to their playing style or strategy preferences.

These potential developments aim to enhance player engagement and add a new dimension to the strategic planning in Futebol Chess, making each game an even more unique and personalized experience.

### Sample Table of Individualized Fictional Pieces
Just for food for thought:

| Name             | Type        | Speed | Skill | Strength | Goal | Defense |
|------------------|-------------|-------|-------|----------|------|---------|
| Leo the Swift    | Attacker    | 85    | 55    | 45       | 90   | 35      |
| Isabel the Wall  | Defender    | 45    | 45    | 75       | 35   | 85      |
| Midas the Maestro| Midfielder  | 65    | 75    | 55       | 55   | 65      |
| Guardian Grace   | Goal Keeper | 35    | 45    | 85       | 65   | 95      |
| Zigzag Zoe       | Dribbler    | 95    | 85    | 35       | 45   | 45      |
| Hawk-Eye Hector  | Goaler      | 55    | 55    | 65       | 95   | 55      |
| Curveball Callie | Long Expert | 75    | 65    | 55       | 75   | 45      |

**Note:** This table presents a conceptual view of individualized pieces in Futebol Chess. Each character has unique attributes that slightly exceed the standard ranges of their respective types. These variations exemplify how characters could be tailored in future versions of the game for specific strategies or playstyles.

## 12. Further analysis

### 12.1 MOVE Action

#### 1. Eligible Pieces for MOVE Action:
- **All pieces**, including special types (Dribblers, Goalers, Long Experts), perform a MOVE action based on the movement pattern of the regular player type they represent.

#### 2. Target Squares for MOVE Action Based on Original Player Types:
- **Defenders (D) and Long Experts (L):** Move 1 square in any direction.
- **Midfielders (M):** Move 2 squares to the sides, 1 forward, 1 backward.
- **Attackers (A), Dribblers (R), and Goalers (G):** Move 2 squares forward, 1 backward, 1 to the sides.
- **Goal Keeper (K):** Move 1 square in any direction.

#### 3. State of Origin and Target Squares:
- **Origin Square:** Contains the moving piece; becomes empty after the move.
- **Target Square:** Can be empty, contain a teammate (blocking the move), an opponent (resulting in a foul), or the ball.
- **Field Markers:** Target square may have field markers indicating specific zones (goal area, penalty area).

#### 4. Possible Results of MOVE Action:
- **Successful Move:** Executed if the target square is empty or contains the ball.
- **Blocked Move:** Cannot be completed if the target square contains a teammate.
- **Foul:** Occurs if the target square has an opponent's piece; may lead to a free kick or other penalty.
- **Ball Possession:** The moving piece takes possession if the target square contains the ball.

### Notes:
- The MOVE action is the primary means for players to reposition their pieces on the board.
- The special player types' movement is determined by the regular player type they represent, adding strategic depth to the selection process.
- Players must consider both the target square's status and the potential consequences of their move, including the possibility of committing a foul.


### 12.2 PASS Action

#### 1. Eligible Pieces for PASS Action:
- **All pieces** are eligible to perform a PASS action. This includes Dribblers (R), Goalers (G), Long Experts (L), Midfielders (M), Attackers (A), Defenders (D), and the Goal Keeper (K).

#### 2. Target Squares for PASS Action:
- The target square for a PASS must be within line of sight and within the passing range of the piece, typically extending up to 2 times the standard movement range of the piece.
- **Example:** An Attacker (A) who moves 2 squares forward can pass the ball up to 4 squares forward.

#### 3. State of Origin and Target Squares:
- **Origin Square:** Initially contains the piece performing the PASS action along with the ball. After the pass, the piece remains, but the ball moves to the target square.
- **Target Square:** Must be empty or contain a teammate to receive the pass. Cannot contain an opponent's piece.

#### 4. Possible Results of PASS Action:
- **Successful Pass:** Completed if the target square is empty or contains a teammate who then receives the ball.
- **Interception:** If an opponent's piece is in a position to challenge the pass (except for LONG PASS), the pass may be intercepted.
- **Blocked Pass:** The pass is blocked if the target square contains an opponent's piece or if there is no clear line of sight due to obstructions.

### Notes:
- The PASS action is crucial for advancing the ball towards the opponent's goal and strategically positioning teammates.
- Accurate assessment of the field and opponent's positioning is essential to avoid interceptions and make effective passes.
- This action requires players to think ahead, considering both the immediate action and potential subsequent moves by opponents.

### 12.3 LONG PASS Action

#### 1. Eligible Pieces for LONG PASS Action:
- **Long Experts (L):** Long Experts, regardless of their original type (Defender, Midfielder, Attacker, etc.), have the unique ability to perform a LONG PASS action.

#### 2. Target Squares for LONG PASS Action:
- The target square for a LONG PASS must be within the extended range of the Long Expert, typically extending up to 3 times the standard movement range of the piece.
- **Range Based on Original Type:**
  - If originally a Defender: Can cover up to 3 squares.
  - If originally a Midfielder: Can cover up to 3 squares (since Midfielders can move 1 square forward, backward, or to the sides).
  - If originally an Attacker: Can cover up to 6 squares forward (as Attackers can move 2 squares forward).

#### 3. State of Origin and Target Squares:
- **Origin Square:** Contains the Long Expert performing the LONG PASS along with the ball. After the pass, the piece remains, but the ball moves to the target square.
- **Target Square:** Must be empty or contain a teammate to receive the pass. Cannot contain an opponent's piece.

#### 4. Possible Results of LONG PASS Action:
- **Successful Long Pass:** Completed if the target square is empty or contains a teammate who then receives the ball. LONG PASS actions are not interceptable.
- **Blocked Long Pass:** The pass is blocked if the target square contains an opponent's piece or if there is no clear line of sight due to obstructions.

### Notes:
- The LONG PASS action enables Long Experts to send the ball over longer distances, crucial for bypassing crowded areas or rapidly changing the field's dynamic.
- Players must strategically use LONG PASS, considering the original type of the Long Expert for determining the pass range and potential strategies.
- The uninterceptible nature of LONG PASS makes it a key tactical action in XFutebol, allowing for unexpected and swift repositioning of the ball.

### 12.4 SHOOT Action

#### 1. Eligible Pieces for SHOOT Action:
- **All pieces** are eligible to perform a SHOOT action. This includes Dribblers (R), Goalers (G), Long Experts (L), Midfielders (M), Attackers (A), Defenders (D), and the Goal Keeper (K).

#### 2. Target Squares for SHOOT Action:
- The target for a SHOOT action is the opponent's goal area.
- The range of the SHOOT action is typically up to 2 times the standard movement range of the piece.
   - **Example:** An Attacker (A), who normally moves 2 squares forward, can shoot from up to 4 squares away from the goal.

#### 3. State of Origin and Target Squares:
- **Origin Square:** Initially contains the piece performing the SHOOT action. After the shot, the piece remains, but the ball is directed towards the goal.
- **Target Square:** The goal area squares where the shot is aimed.

#### 4. Possible Results of SHOOT Action:
- **Goal Scored:** If the SHOOT action successfully outmatches the goalkeeper's defense, based on the shooter's and goalkeeper's respective attributes.
- **Saved by Goalkeeper:** If the goalkeeper's defense attribute is equal to or higher than the shooter's goal attribute.
- **Missed Shot:** If the shot does not reach the goal area or goes off-target.

### Notes:
- The SHOOT action is a critical component of XFutebol, offering a direct attempt to score a goal.
- Accuracy and the strategic use of shooters based on their attributes are key to maximizing the effectiveness of SHOOT actions.
- Players need to position their pieces effectively, taking into account the distance and angle of the shot to increase the chances of scoring.

### 12.5 LONG SHOOT Action

#### 1. Eligible Pieces for LONG SHOOT Action:
- **All pieces** are eligible to perform a LONG SHOOT action. This includes Dribblers (R), Goalers (G), Long Experts (L), Midfielders (M), Attackers (A), Defenders (D), and the Goal Keeper (K).

#### 2. Target Squares for LONG SHOOT Action:
- The target for a LONG SHOOT action is the opponent's goal area.
- The range of the LONG SHOOT action is typically up to 3 times the standard movement range of the piece.
   - **Example:** An Attacker (A), who normally moves 2 squares forward, can attempt a long shoot from up to 6 squares away from the goal.

#### 3. State of Origin and Target Squares:
- **Origin Square:** Initially contains the piece performing the LONG SHOOT action. After the shot, the piece remains, but the ball is directed towards the goal.
- **Target Square:** The goal area squares where the long shot is aimed.

#### 4. Possible Results of LONG SHOOT Action:
- **Goal Scored:** If the LONG SHOOT action successfully outmatches the goalkeeper's defense, based on the shooter's and goalkeeper's respective attributes.
- **Saved by Goalkeeper:** If the goalkeeper's defense attribute is equal to or higher than the shooter's goal attribute.
- **Missed Shot:** If the long shot does not reach the goal area or goes off-target.
- **Intercepted in CHALLENGE:** The LONG SHOOT can be intercepted if there is an opponent's piece in one of the squares along the trajectory of the shot. The interception is determined by a CHALLENGE action, where the opposing piece attempts to block or take control of the ball.

### Notes:
- The LONG SHOOT action adds a strategic layer to the game, enabling players to attempt scoring from a distance.
- The interception possibility via a CHALLENGE adds an element of risk, making the decision to perform a LONG SHOOT more tactical.
- Players need to assess the field for potential interceptors and weigh the risk of interception against the chance of scoring.


### Notes:
- The LONG SHOOT action allows players to attempt to score from greater distances, adding a dynamic element to the game.
- The increased range requires precise judgment and strategic positioning, as well as consideration of the shooter's attributes.
- Successfully executing a LONG SHOOT depends on the shooter's skill and the goalkeeper's ability to defend, making it a high-risk, high-reward action.

- This action requires players to consider the risk and reward of attempting a goal from a distance, factoring in both the shooter's and the goalkeeper's capabilities.

### 12.6 Dribble Action

#### 1. Eligible Pieces for DRIBBLE Action:
- **All pieces** are eligible to perform a DRIBBLE action. This includes Dribblers (R), Goalers (G), Long Experts (L), Midfielders (M), Attackers (A), Defenders (D), and the Goal Keeper (K).

#### 2. Target Squares for DRIBBLE Action:
- The target for a DRIBBLE action is typically an adjacent square in any direction.
- The DRIBBLE action is used to evade an opponent piece in an adjacent square while maintaining possession of the ball.

#### 3. State of Origin and Target Squares:
- **Origin Square:** Initially contains the piece performing the DRIBBLE action along with the ball.
- **Target Square:** Can be adjacent in any direction, ideally empty or containing an opponent's piece to be dribbled past.

#### 4. Possible Results of DRIBBLE Action:
- **Successful Dribble:** If the dribbling piece's Speed and Skill successfully outmatch the adjacent opponent's Speed and Defense.
- **Failed Dribble:** If the adjacent opponent's Speed and Defense are equal to or greater than the dribbling piece's Speed and Skill.
- **Tie:** In case of a tie, the dribbling piece maintains possession, but the DRIBBLE action fails to advance the ball.

### Notes:
- The DRIBBLE action is essential in XFutebol for advancing the ball and evading opponents, particularly in crowded areas of the field.
- Dribblers (R) might have an advantage in this action due to their likely higher Speed and Skill attributes.
- Successful DRIBBLE maneuvers require strategic decision-making, considering both the dribbler's and the opponent's attributes.
- The action adds a layer of tactical play, emphasizing the importance of individual skill in ball control and evasion.

### 12.7 Challenge Action

#### 1. Eligible Pieces for CHALLENGE Action:
- **All pieces** are eligible to perform a CHALLENGE action. This includes Dribblers (R), Goalers (G), Long Experts (L), Midfielders (M), Attackers (A), Defenders (D), and the Goal Keeper (K).

#### 2. Target Squares for CHALLENGE Action:
- The target for a CHALLENGE action is the square occupied by an opponent's piece who has the ball or is the intended recipient of a ball in motion (during SHOOT, PASS, or LONG SHOOT actions).
- CHALLENGE actions are typically executed in adjacent squares to the challenging piece.

#### 3. State of Origin and Target Squares:
- **Origin Square:** Initially contains the piece performing the CHALLENGE action.
- **Target Square:** Occupied by the opponent's piece with the ball or the intended recipient of the ball.

#### 4. Possible Results of CHALLENGE Action:
- **Successful Challenge:** If the total of the challenger's Speed, Strength, and Defense is greater than the total of the opponent's Speed, Strength, and Skill.
- **Failed Challenge:** If the opponent's total of Speed, Strength, and Skill is equal to or greater than the total of the challenger's Speed, Strength, and Defense.
- **Tie:** If there is a tie in the total attributes, the ball continues its intended path; the CHALLENGE action neither gains possession of the ball nor disrupts its course.

### Notes:
- The CHALLENGE action is a fundamental defensive tactic in XFutebol, enabling players to counter opponents' offensive moves and potentially regain possession.
- It introduces a critical decision-making aspect to the game, where players must assess the risk and opportunity of challenging an opponent's action.
- The ability to CHALLENGE various actions like SHOOT, PASS, and LONG SHOOT (excluding LONG PASS) adds strategic depth and dynamic interactions between players on the field.

### 12.8 Sprint Action

#### 1. Eligible Pieces for SPRINT Action:
- **All pieces** are eligible to perform a SPRINT action. This includes Dribblers (R), Goalers (G), Long Experts (L), Midfielders (M), Attackers (A), Defenders (D), and the Goal Keeper (K).

#### 2. Target Squares for SPRINT Action:
- The target for a SPRINT action is any square within the double movement range of the piece.
- The SPRINT action is used to rapidly advance or reposition the piece on the field, typically for strategic positioning or responding to threats.

#### 3. State of Origin and Target Squares:
- **Origin Square:** Initially contains the piece performing the SPRINT action.
- **Target Square:** Can be any square within the double movement range of the piece, ideally positioning the piece advantageously on the field.

#### 4. Possible Results of SPRINT Action:
- **Successful Sprint:** The piece successfully moves to the target square, covering a greater distance than usual in a single turn.
- **Failed Sprint:** The SPRINT action fails if the target square is not within the permissible range or is occupied by another piece (either teammate or opponent).
- **Tie:** Not applicable as SPRINT does not involve a direct contest with another piece.

#### 5. Limitation and Recovery Period for SPRINTs:
- **Team Limit:** A team can perform up to 3 SPRINTs per half without any penalty.
- **Additional SPRINTs:** Teams can decide to use more than 3 SPRINTs. However, for each SPRINT beyond the third, the piece used will be temporarily removed from the field for a 90-second recovery period.
- **Recovery Mechanism:** The recovery period simulates fatigue and recovery, reflecting the physical demands of an actual sprint. The piece is sidelined and cannot participate in the game during this time.
- **Strategic Consideration:** This rule requires teams to weigh the benefits of additional SPRINTs against the cost of temporarily losing a piece from the field, adding a layer of depth to tactical decisions.

### Notes:
- The SPRINT action, with its limitation and recovery period, mirrors real-life athletic constraints, bringing an element of realism to XFutebol.
- The decision to use additional SPRINTs becomes a significant strategic choice, balancing immediate tactical gain against short-term numerical disadvantage.
- Managing the use of SPRINTs effectively becomes crucial, especially in critical phases of the game or when planning for specific strategies.
