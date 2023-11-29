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

### **1.2 Game Components**
*The game consists of two chess boards aligned to create a 16x8 grid, pieces representing different player types, and markers for tracking fouls and cards.*

### **1.3 Player Types**
- **Attackers (Forwards):** Fast, goal-oriented players.
- **Defenders:** Strong, defense-focused players.
- **Midfielders:** Versatile players adept in both offense and defense.
- **Goal Keepers:** Specialized in defending the goal, with the option to join attacks.
- **Dribblers:** Skilled in evading opponents and maintaining ball control.
- **Goalers:** Focused on scoring and long-range shots.
- **Long Experts:** Specialized in executing uninterceptible long passes and shots.




## **2. Game Setup**
### **2.1 Board Configuration**
*Align two chess boards to form a 16x8 grid, representing an extended soccer field.*

### **2.2 Team Composition**
*Each team consists of 11 players. At the beginning of the game, players select two special pieces from each of the following categories: Dribblers, Goalers, and Long Experts. The remaining five players include the Goal Keeper, along with a combination of Attackers, Defenders, and Midfielders.*

### 2.3 Goal Area
- **Definition:** The Goal Area is a crucial zone on the game board, located at each end of the board, surrounding the goal.
- **Location:** For a 16x8 board, the Goal Area is defined as the squares C1-F1 and C8-F8.
- **Significance:** The Goal Keeper usually occupies this area. If the Goal Keeper is outside of the Goal Area, the goal is considered empty, increasing the chance of scoring.
- **Scoring a Goal:**
  - **Eligibility:** Any piece on the field can attempt a shot towards the Goal Area.
  - **Mechanism:** A goal is scored when the ball successfully crosses any of the four squares of the Goal Area. This is determined by the shooter's ability to outmatch the goalkeeper's defense, based on their respective attributes.
  - **Goalkeeper's Defense:** The Goal Keeper attempts to defend against shots aimed at the Goal Area. The outcome of this defense is determined by comparing the relevant attributes of the shooter and the goalkeeper.
- **Player Awareness:** Players should be acutely aware of the Goal Area on their own board. It is important for attackers to recognize opportunities to score, and for the goalkeeper to be strategically positioned for effective defense.

### 2.4 Penalty Area
- **Definition:** The Penalty Area is a larger zone that includes the Goal Area and additional squares directly in front of the goal.
- **Location:** The Penalty Area extends to squares B1-G1, B2-G2 for one end and B7-G7, B8-G8 for the other end of the board.
- **Importance:** Fouls committed by the defending team in the Penalty Area result in a penalty kick for the attacking team.
- **Player Awareness:** Understanding the boundaries and strategic significance of the Penalty Area is essential for effective gameplay.

### **2.5 Turn Structure**
- **Two Movements per Turn:** In each turn, a player can make two movements. 
- **Mandatory MOVE:** Out of these two movements, at least one must be a MOVE action. The other can be any action, including another MOVE.
- **Strategic Consideration:** This rule encourages players to strategically plan their movements and actions, balancing between advancing their pieces and executing specific actions like Pass, Dribble, or Shoot.

### **2.6 Starting the Game**
*The game starts with a coin toss to decide the starting team. Players should keep in mind the strategic importance of the Goal and Penalty Areas as they begin their play.*


### **2.4 Defining the Winning Style**
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
Attempt to take the ball from an opponent, successful based on Strength and Defense.

### 3.5 Dribble Action
Evade an opponent in an adjacent square, using Speed and Skill.

### 3.6 Sprint Action
- **Description:** Doubles the movement capacity of a piece for one turn.
- **Limit:** Each team can use Sprint 3 times per half.
- **Outcome:** Allows rapid repositioning or advancement towards the goal, crucial for creating scoring opportunities or responding to threats.

### 3.7 Shoot Action

#### Mechanism:
- The outcome of a SHOOT action is determined by comparing a combination of attributes for both the shooter and the goalkeeper.
  - **Shooter's Attributes:** Goal + Strength + Skill.
  - **Goalkeeper's Attributes:** Defense + Speed + Skill.

#### Distance:
- The Shoot action extends up to 2 times the base MOVE range for the piece.
  - **Example:** An Attacker (A), who normally moves 2 squares forward, can shoot from up to 4 squares away from the goal.

#### Outcome:
- **Goal Scored:**
  - If the total of the shooter's Goal, Strength, and Skill is greater than the total of the goalkeeper's Defense, Speed, and Skill.
  - **Notation:** `Goal + Strength + Skill > Defense + Speed + Skill`
- **Saved or Deflected by Goalkeeper:**
  - If the goalkeeper's total of Defense, Speed, and Skill is equal to or greater than the total of the shooter's Goal, Strength, and Skill.
  - **Notation:** `Defense + Speed + Skill ≥ Goal + Strength + Skill`

### Notes:
- The SHOOT action is a critical part of XFutebol gameplay, representing a direct attempt to score a goal.
- The addition of Strength and Skill for the shooter and Speed for the goalkeeper adds depth to the strategy, making the success of shots more nuanced and dependent on a broader range of player attributes.
- Players need to consider the positioning and attributes of their shooters and the opposing goalkeeper to maximize the chances of scoring successfully.


### 3.8 Long Shoot Action
- **Mechanism:** Long Experts can perform a Long Shoot action, using their Goal and Strength. This action includes both straight and curved shots.
  - **Curved Shoot:** Involves choosing an intermediary square for the curve and the final goal square. Enhances the ability to score from angles not directly aligned with the goal.
- **Distance:** The Long Shoot action extends up to 3 times the standard movement range of the piece.
- **Outcome:**
  - If Goal + Strength > Defense + Skill: Goal is scored.
  - If Defense + Skill ≥ Goal + Strength: Goalkeeper saves or deflects the shot.

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

#### 1. **Goal Scoring Attempt (Shot or Penalty):**
- **Mechanism:** The outcome is determined by comparing the shooter's Goal attribute with the goalkeeper's Defense attribute.
- **Attributes:** 
  - Shooter's Goal (Go)
  - Goalkeeper's Defense (De)

#### 2. **Outcome Determination:**
- **Goal Scored:** 
  - If the shooter's Goal attribute is significantly higher than the goalkeeper's Defense.
  - *Example:* `Go >= De + 20` (The shooter's Goal is at least 20 points higher than the goalkeeper's Defense)

- **Save with Rebound:** 
  - If the shooter's Goal attribute is slightly higher or nearly equal to the goalkeeper's Defense.
  - *Example:* `De <= Go < De + 20` (The shooter's Goal is greater than or equal to the goalkeeper's Defense but less than 20 points higher)

- **Goalkeeper Clears:** 
  - If the goalkeeper's Defense attribute is slightly higher than the shooter's Goal.
  - *Example:* `Go + 10 <= De < Go + 20` (The goalkeeper's Defense is up to 20 points higher than the shooter's Goal)

- **Clean Save:** 
  - If the goalkeeper's Defense attribute is significantly higher than the shooter's Goal.
  - *Example:* `Go + 20 <= De` (The goalkeeper's Defense is at least 20 points higher than the shooter's Goal)

### Notes:
- These thresholds (e.g., 20 points difference) are examples and can be adjusted based on gameplay balance needs.
- This system provides a more strategic and predictable approach to determining outcomes, as it is based on the players' attributes rather than the randomness of a dice roll.
- The specific numbers (like 20 points difference) are adjustable to ensure the game remains balanced and enjoyable for all levels of players.


## 6. Fouls and Penalties
### 6.1 Defining a Foul
Occurs when a player's MOVE targets an opponent's square, or an unsuccessful CHALLENGE is made.

### 6.2 Consequences of Fouls
- **Team-Based Fouls Count:** The number of fouls is counted collectively for the whole team, rather than individually for each piece.
- **Yellow Card:** The team receives a yellow card upon accumulating 3 fouls. This serves as a warning and may influence the team's play style.
- **Red Card:** Upon reaching 4 or more fouls, the team is issued a red card. As a result, one of the team's pieces is chosen to be removed from the game. This represents a significant disadvantage and encourages teams to play cautiously to avoid fouls.


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
| Player Type   | Speed | Skill | Strength | Goal | Defense |
|---------------|-------|-------|----------|------|---------|
| Attackers     | 80    | 50    | 40       | 85   | 30      |
| Defenders     | 40    | 40    | 70       | 30   | 80      |
| Midfielders   | 60    | 70    | 50       | 50   | 60      |
| Goal Keeper   | 30    | 40    | 80       | 60   | 90      |
| Dribbler      | 90    | 80    | 30       | 40   | 40      |
| Goaler        | 50    | 50    | 60       | 90   | 50      |
| Long Experts  | 70    | 60    | 50       | 70   | 40      |

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

### 12.1 MOVE Action Analysis in XFutebol

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


### 12.2 PASS Action Analysis in XFutebol

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

### 12.3 LONG PASS Action Analysis in XFutebol

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

### 12.4 SHOOT Action Analysis in XFutebol

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
