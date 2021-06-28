# PIG GAME

###### \*PIG GAME is one project I learned from [Jonas Schmedtmann](https://www.udemy.com/share/101WfeAEYbdllRRHQH/).

## BRIEF

A dice game | [**DEMO**](https://howiework.github.io/Pig-game/)

## KEYWORDS

DOM, JavaScript, Events

## FEATURES

### How To Play

1. Click ROLL DICE button to randomly generate a dice number between 1-6;
2. You can keep rolling the dice unless the dice number is 1 (see 4 to understand what would happen if the dice number is 1). All the dice numbers will add to your CURRENT score;
3. You can choose either HOLD, which will add your CURRENT score to your PLAYER 1/2 score (your final score) and then switch to the other player, or ROLL DICE unless the dice number is 1 (taking own risk :).
4. If the dice number is 1, you will automatically lose your CURRENT score and switch to the other player.

### About Scores

Whosever final score reaches 100 will win the game!

### Flowchart

![Pig-game flowchart](./Pig-game-flowchart.svg 'Pig-game flowchart')

```mermaid
graph TD
A([User: roll dice]) --> A1[Generate a random dice]
    A1 --> A2[Display dice]
    A2 --> A3{Is dice 1?}
    A3 -->|No|A4[Add dice to current score]
    A3 -->|Yes|D[Switch player]
    A4 --> A5[Display new score]

    B([User: hold score])--> B1[Add current score to total score]
    B1 --> B2{Score >= 100?}
    B2 -->|No|D
    B2 -->|Yes|B3[Current player wins!]


    C([User: reset game])--> C1[Set all scores to 0]
    C1 --> C2[Set player 1 as starting player]
```
