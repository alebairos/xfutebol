# Futebol Chess Game Manual
# Futebol Chess Game Manual

## Table of Contents
1. [Game Overview](#1-game-overview)
   1. [Objective](#11-objective)
   2. [Game Components](#12-game-components)
   3. [Player Types](#13-player-types)
2. [Game Setup](#2-game-setup)
   1. [Board Configuration](#21-board-configuration)
   2. [Team Composition](#22-team-composition)
   3. [Starting the Game](#23-starting-the-game)
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

## 1. Game Overview
### 1.1 Objective
Players compete to score goals by strategically moving pieces on a chessboard-like soccer field. The game combines elements of chess and soccer, requiring tactical thinking and careful planning.

### 1.2 Game Components
The game consists of two chess boards aligned to create a 16x8 grid, pieces representing different player types, and markers for tracking fouls and cards.

### 1.3 Player Types
- **Attackers (Forwards):** Fast, goal-oriented players.
- **Defenders:** Strong, defense-focused players.
- **Midfielders:** Versatile players adept in both offense and defense.
- **Goal Keepers:** Specialized in defending the goal, with the option to join attacks.
- **Dribblers:** Skilled in evading opponents and maintaining ball control.
- **Goalers:** Focused on scoring and long-range shots.
- **Long Experts:** Specialized in executing uninterceptible long passes and shots.

## 2. Game Setup
### 2.1 Board Configuration
Align two chess boards to form a 16x8 grid, representing an extended soccer field.

### 2.2 Team Composition
Each team consists of 11 players. At the beginning of the game, players select two special pieces from each of the following categories: Dribblers, Goalers, and Long Experts. The remaining five players include the Goal Keeper, along with a combination of Attackers, Defenders, and Midfielders. This selection forms the basis of the team's strategy, influencing their approach to both offense and defense throughout the game.

- **Special Pieces Selection:**
  - Choose 2 Dribblers: Skilled in evading opponents and maintaining ball control.
  - Choose 2 Goalers: Focused on scoring, especially effective in shoot actions.
  - Choose 2 Long Experts: Specialized in executing uninterceptible long-range passes and shots, with the ability to perform both straight and curved actions.
- **Regular Players:**
  - The remaining players, including the Goal Keeper, are chosen to balance the team composition, focusing on defense, midfield control, and attack strategies.

### 2.3 Starting the Game
The game starts with a coin toss to decide the starting team.


## 3. Player Movement and Actions
### 3.1 Move Action
Players move their pieces according to the type's movement ability. 
- **Attackers:** Move 2 squares forward, 1 backward, 1 to the sides.
- **Defenders:** Move 1 square in any direction.
- **Midfielders:** Move 2 squares to the sides, 1 forward, 1 backward.
- **Goal Keeper:** Move 1 square in any direction; moving out of the small area risks leaving the goal unguarded.
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
Key in defending the goal. Can move out of the small area but risks leaving the goal unguarded.

## 6. Fouls and Penalties
### 6.1 Defining a Foul
Occurs when a player's MOVE targets an opponent's square, or an unsuccessful CHALLENGE is made.

### 6.2 Consequences of Fouls
Accumulating 3 fouls results in a yellow card, 4 or more in a red card and the removal of a piece from the game.

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
If the goalkeeper is not in the small area and a goal is attempted, it's likely to succeed.

### 7.2 Barrier Formation and Challenges
Defenders can form a barrier and challenge LONG actions after a free kick.

## 8. Game Dynamics and Balance
### 8.1 Team Limits on SPRINT and LONG Actions
Restrictions to prevent overuse and maintain strategic depth.

### 8.2 Energy and Stamina System
Affects player performance and limits the frequency of certain actions.

## 9. Winning the Game
### 9.1 Golden Goal
First goal wins the game.

### 9.2 Two Halves with Total Score
The highest score after two halves wins, with a penalty shootout as a tiebreaker.

### 9.3 Number of Goals
The first team to reach a predetermined number of goals wins.

### 9.4 Movement Count Rule
If no goals are scored within a set number of movements, the winner is decided by a penalty shootout.

## 10. Miscellaneous Rules
### 10.1 Substitutions
Rules for changing player types during the game (if applicable).

### 10.2 Half-Time and Game Duration
The length of each half and total game time.

### 10.3 Simplified Version: Specific Attribute Values for Player Types
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
