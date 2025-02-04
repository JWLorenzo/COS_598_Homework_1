## Class: COS 598 - Game AI
## Homework 1
## Author: Jacob Lorenzo
## Date: 2/2/2025

## Writeup:

I decided to use a monte carlo simulation for determining accuracy, it will have a degree of randomness to it, but I think that it works out better for larger attack values.

One major issue with the current calculations is the death multiplier. Right now, it's functioning more like a health bar that gradually reduces damage over time, which isn't realistic. Ideally, it should follow a normal distribution, similar to how I handled damage. However, calculating the standard deviation for that function is significantly more challenging because the potential damage range is theoretically infinite. Even my estimation for average damage isn’t entirely precise; I would have needed to perform summations to determine the exact value.

I didn’t optimize for a specific combination; instead, I aimed to keep the approach as generalized as possible. Interestingly, when I switched from a dynamic multiplier to a static one, the error rate dropped significantly. I suspect the issue was an overestimation of the number of units that died.

Oddly enough, the average error decreased sharply (by more than 0.2) when I simply returned 0 for the fitness outcome. I figured out that it was due to not clamping the percentages to be between 0 and 1. I also forgot to incorporate armor reductions in the initial version, but after incorporating that adjustment, the calculations became noticeably more accurate.