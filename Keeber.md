# Challenges: Keeber
Category: **OSINT**  
Difficulty: **Medium**  
Points: **---**  
Solves: **---**

## Keeber 1

Challenge Description: 


### Files
```
from Crypto.Util.number import getPrime, bytes_to_long, long_to_bytes


[RSA_Frustration output](https://github.com/drewd314/WolvSec-CTF-2022-Writeups/files/8358502/RSA_Frustration_-_output.2.txt)

### Approach

**Step 1:**
We need all p and q values of the Ns. This can take a long time to generate since the largest N is 199 digits long. To accommodate for this, I uploaded the factors to [FactorDB](http://factordb.com/). An algorithm that fetches the primes from factor DB can be used, or just manually doing it since there are only 27 Ns to factor.

**Step 2:**
We are given the encrypted ciphertext after 27 encryptions, so we have to start by using the largest N's p and q values and the nth root algorithm to get possible p and q roots. We use the Chinese remainder theorem with the p and q roots to give us possible candidate decryptions, for which there will be e^2 of (12769 in this case). 

**Step 3:**
We are then going to have to construct an algorithm to keep recursing through the possible candidate decryptions, using the correct p and q values based on the depth of the recursion. A depth first search (DFS) is most useful here to get the flag quicker. Using [OPz qt's](https://github.com/christheyankee) DFS Sage Script we can get the flag!

```
from Crypto.Util.number import long_to_bytes

```

flag: `wsc{s4g3m4th_i5_5up3r_co0l!}`



### Notes

The initial idea was to make the optimization needed to find the flag, however this would likely lead to people with very great computing power to be able to still use the sole DFS algorithm without the e optimization. Therefore, the optimization is just a bonus idea. It is most useful when trying to replicate the results of the challenge. Sage remembers factors, so when running the scripts a second time the non-optimized one takes a minute whereas the optimized one takes 5 seconds on my machine. Maybe someone could force this optimization in a challenge of their own! If 10 bits were added instead of 9 then we would not even need a DFS, and could do it linear with the smallest candidate decryption each time. However, the idea for this challenge was to incorporate a DFS but to be able to use the optimization as assistance.

Will add more mathmatical explinations for this algorithm soon!
