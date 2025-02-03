## Class: COS 598 - Game AI
## Homework 1
## Author: Jacob Lorenzo
## Date: 2/2/2025

## Writeup:

Pretty much my solution uses the assumption of the central limit theorem since every ability score is tied to effectively a die roll.
Currently a glaring issue with the calculations is the multiplier for death. It's effectively a health bar that reduces damage over time, but that's not realistic.
It should ideally be some sort of normal distribution, similar to what I did for the damage. It's a lot harder to calculate the standard deviation of that function because
it could be potentially infinite damage. Even the estimation I did for the average damage isn't super accurate because I would've had to do some summations to figure out the 
accurate value. I didn't optimize towards a specific combination; I wanted to keep it as generalized as possible. 