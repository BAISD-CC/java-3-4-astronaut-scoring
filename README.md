# Ch. 3 Challenge 4: Astronaut Scoring

## Mission Briefing

We need to figure out who is going to captain the ship, and the best way to do that is through scoring. Your program reads three astronauts' names and exam scores, checks that every score is valid, ranks the astronauts from highest to lowest score, and reports the crew's average score.

## What You'll Practice

- `Scanner` input of `String` and `int` values, including the leftover newline (Chapter 2)
- Comparing values with `&&`, `||`, or nested ifs (Day 1 and Day 2 notes)
- An if-else-if chain with a trailing else (Day 1 notes, E1-C)
- Floating-point division and `printf` with `%.2f` (Chapter 2; Day 1 notes, E1-D; Day 3 Foundations)

## Starter Code

Edit `src/AstronautScoring.java`. The class is named `AstronautScoring`. Do not rename the file or the class.

The comments in `main` list the steps in order. You may follow them or solve the problem your own way.

## Inputs

Read all six values, in this order, before deciding anything.

| Order | Input | Type |
|---|---|---|
| 1 | First astronaut's name | `String` |
| 2 | First astronaut's score | `int` |
| 3 | Second astronaut's name | `String` |
| 4 | Second astronaut's score | `int` |
| 5 | Third astronaut's name | `String` |
| 6 | Third astronaut's score | `int` |

## Rules

### 1. Check the scores

A valid score is from 0 to 100.

| Score | Result |
|---|---|
| **below** 0 | invalid |
| 0 **through** 100 | valid |
| **above** 100 | invalid |

If **any** of the three scores is invalid, print the invalid message only. Do not print the ranking or the average.

### 2. Rank the astronauts

Display the three names from highest score to lowest. The test scores never contain a tie, so you do not need to handle equal scores.

### 3. Report the crew average

```text
average = (score1 + score2 + score3) / 3.0
```

Display it to two decimal places. Dividing by `3` instead of `3.0` uses integer division and drops the decimals.

## What to Use

These tools fit this problem. They are suggestions: any approach that produces the correct output earns full credit.

- `||` to check whether any score is outside 0 to 100, or one check per score.
- `&&` to test whether one score is greater than both of the others, or nested ifs.
- `printf` with `%.2f` for the average.

## Exact Output

Spelling, capitalization, and punctuation must match exactly. Each prompt ends with one space, and the user types on the same line.

Prompts, in this order:

```text
Enter the first astronaut's name: 
Enter the first astronaut's score: 
Enter the second astronaut's name: 
Enter the second astronaut's score: 
Enter the third astronaut's name: 
Enter the third astronaut's score: 
```

Then either the ranking and the average, where `[average]` is shown to **two decimal places**:

```text
Highest score: [name]
Second highest score: [name]
Third highest score: [name]
Crew average: [average]
```

or, if any score is invalid, only this line:

```text
Invalid score. Scores must be from 0 to 100.
```

## Sample Runs

```text
Enter the first astronaut's name: Nova
Enter the first astronaut's score: 88
Enter the second astronaut's name: Kai
Enter the second astronaut's score: 95
Enter the third astronaut's name: Zara
Enter the third astronaut's score: 72
Highest score: Kai
Second highest score: Nova
Third highest score: Zara
Crew average: 85.00
```

```text
Enter the first astronaut's name: Nova
Enter the first astronaut's score: 88
Enter the second astronaut's name: Kai
Enter the second astronaut's score: 105
Enter the third astronaut's name: Zara
Enter the third astronaut's score: 72
Invalid score. Scores must be from 0 to 100.
```

## Test Your Program

Run every row before you submit. The autograder uses these values and others. Put the highest score first, second, and third so you know your comparisons work in every position.

| Scores entered | Expected ranking (highest to lowest) | Crew average |
|---|---|---|
| Alice 90, Ben 80, Cara 70 | Alice, Ben, Cara | 80.00 |
| Dax 60, Elin 75, Fox 88 | Fox, Elin, Dax | 74.33 |
| Gus 82, Hana 95, Ivy 40 | Hana, Gus, Ivy | 72.33 |
| Jett 91, Kira 55, Leo 70 | Jett, Leo, Kira | 72.00 |
| a score of 105 or -5 | Invalid score. Scores must be from 0 to 100. | (none) |

## How It's Checked

| Category | Points |
|---|---|
| Prompts (6 tests) | 6 |
| Rankings (4 tests) | 17 |
| Crew averages (4 tests) | 8 |
| Invalid scores rejected (2 tests) | 6 |
| **Total** | **37** |

Grading is by output only. Any approach that prints the correct lines earns full credit. Your results must come from the values the user types; a program that prints fixed answers will fail the tests that use other values.

## Where to Look

- Day 2 notes, Logical Operators section: inside and outside a range, and combining two comparisons with `&&`.
- Day 1 notes, E1-C: an if-else-if chain with a trailing else.
- Day 1 notes, E1-D and Day 3 Foundations: `printf` with `%.2f`.
- Day 3 notes, E3-C: throwing away the leftover newline before reading a name.
