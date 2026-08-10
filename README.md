# Ch. 3 Challenge 4: Astronaut Scoring

We need to figure out who is going to captain the ship, and the best way to do that is through scoring. We have figured out the scoring system, but we want software that ranks the astronauts once we enter their scores.

## What You're Building

Write a program that asks for the names of three astronauts and their scores (whole numbers from 0-100) on the astronaut exam. The program should then display the three astronaut names ranked from highest score to lowest score.

## Concepts You'll Use

- `Scanner` for reading keyboard input
- `String` and `int` variables
- `if` / `else if` / `else` statements to compare the three scores

## Requirements

Your program must print these prompts, in this order, exactly as written:

1. `Enter the first astronaut's name: `
2. `Enter the first astronaut's score: `
3. `Enter the second astronaut's name: `
4. `Enter the second astronaut's score: `
5. `Enter the third astronaut's name: `
6. `Enter the third astronaut's score: `

After reading all three names and scores, your program must display the astronauts in order from highest score to lowest score, using this exact format:

```
Highest score: [name]
Second highest score: [name]
Third highest score: [name]
```

Replace `[name]` with the actual astronaut name entered for that rank.

The test scores used to grade this challenge will never contain a tie, so you do not need to handle equal scores.

## Example Run

```
Enter the first astronaut's name: Nova
Enter the first astronaut's score: 88
Enter the second astronaut's name: Kai
Enter the second astronaut's score: 95
Enter the third astronaut's name: Zara
Enter the third astronaut's score: 72
Highest score: Kai
Second highest score: Nova
Third highest score: Zara
```

## Notes

- Use the values entered by the user in your comparisons and output. Do not hard-code the ranking.
- The astronaut names and scores can be entered in any order; your program needs to figure out the correct ranking regardless of the order they were entered in.
