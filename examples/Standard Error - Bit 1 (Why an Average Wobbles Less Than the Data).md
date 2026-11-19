# Standard Error - Bit 1 (Why an Average Wobbles Less Than the Data)

> This is a made-up example that shows what a saved bit looks like. It is not from a real learner's vault.

## The bit

Five people report their commute in minutes: **20, 30, 25, 35, 40**.

The mean is (20 + 30 + 25 + 35 + 40) / 5 = 150 / 5 = **30 minutes**.

Single people range from 20 to 40. If we asked five *different* people we would get a different mean, but the mean would move much less than any one person does. The **standard error** says how much the mean wobbles from one sample to the next.

**SE = s / √n**

*Read it out loud: "standard error equals s over the square root of n."*

- **s** is the sample standard deviation, the typical distance of one person from the mean. Here the distances are -10, 0, -5, 5, 10. Squared they are 100, 0, 25, 25, 100, which sum to 250. Divide by n - 1 = 4 to get 62.5, and take the square root: s ≈ 7.9.
- **n** is the number of people, 5. Its square root is about 2.24.

SE ≈ 7.9 / 2.24 ≈ **3.5 minutes**.

## The question

Keep the same spread, s = 7.9, but ask 20 people instead of 5. What is the standard error now?

## My answer

√20 ≈ 4.47, so SE ≈ 7.9 / 4.47 ≈ 1.8 minutes. Four times as many people cut the wobble in half, not to a quarter.

## Links

- Topic: [[Standard Error]]
- Builds on: [[Sampling - Bit 2 (Sample vs Population)]]
- Leads to: [[Confidence Intervals - Bit 1 (A Range Around the Mean)]]

## Source

Example textbook, section 7.2.
