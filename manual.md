# XFutebol: a Chess-like board Game Manual.

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
   5. [Starting the Game](#25-starting-the-game)
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
    1. [Substitutions](#101-substitutions)
    2. [Half-Time and Game Duration](#102-half-time-and-game-duration)
    3. [Simplified Version: Specific Attribute Values](#103-simplified-version-specific-attribute-values)
11. [Final Thoughts and Future Developments](#11-final-thoughts-and-future-developments)

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
- **Player Awareness:** Players should be acutely aware of the Goal Area on their own board, as it greatly influences defensive and offensive strategies.

### 2.4 Penalty Area
- **Definition:** The Penalty Area is a larger zone that includes the Goal Area and additional squares directly in front of the goal.
- **Location:** The Penalty Area extends to squares B1-G1, B2-G2 for one end and B7-G7, B8-G8 for the other end of the board.
- **Importance:** Fouls committed by the defending team in the Penalty Area result in a penalty kick for the attacking team.
- **Player Awareness:** Understanding the boundaries and strategic significance of the Penalty Area is essential for effective gameplay.

### **2.5 Starting the Game**
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

### 3.3 Long Pass Action (Exclusive to Long Experts)
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
- **Mechanism:** Shooter's Goal vs. goalkeeper's Defense.
- **Distance:** The Shoot action extends up to 2 times the base MOVE range for the piece. For instance, an attacker can shoot from up to 4 squares away.
- **Outcome:**
  - If Goal > Defense: Goal is scored.
  - If Defense ≥ Goal: Goalkeeper saves or deflects the shot.

### 3.8 Long Shoot Action (Exclusive to Long Experts)
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

## Final Thoughts and Future Developments

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

