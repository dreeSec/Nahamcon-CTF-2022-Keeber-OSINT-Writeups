# Challenges: Keeber
Category: **OSINT**  
Difficulty: **Medium**  
Points: **---**  
Solves: **---**

## Keeber 1
Points: **---**  
Solves: **---**

Challenge Description: 


### Files
```
from Crypto.Util.number import getPrime, bytes_to_long, long_to_bytes


[RSA_Frustration output](https://github.com/drewd314/WolvSec-CTF-2022-Writeups/files/8358502/RSA_Frustration_-_output.2.txt)
```
### Approach

https://www.whois.com/whois/keebersecuritygroup.com![ca561a0dc02967e2676d08697aaedaca]

![ca561a0dc02967e2676d08697aaedaca](https://user-images.githubusercontent.com/74334127/166116672-db875f99-f941-4bd1-b14f-b03eeb9c9abc.png)



```
from Crypto.Util.number import long_to_bytes

```

flag: `wsc{s4g3m4th_i5_5up3r_co0l!}`



### Notes

The initial idea was to make the optimization needed to find the flag, however this would likely lead to people with very great computing power to be able to still use the sole DFS algorithm without the e optimization. Therefore, the optimization is just a bonus idea. It is most useful when trying to replicate the results of the challenge. Sage remembers factors, so when running the scripts a second time the non-optimized one takes a minute whereas the optimized one takes 5 seconds on my machine. Maybe someone could force this optimization in a challenge of their own! If 10 bits were added instead of 9 then we would not even need a DFS, and could do it linear with the smallest candidate decryption each time. However, the idea for this challenge was to incorporate a DFS but to be able to use the optimization as assistance.

Will add more mathmatical explinations for this algorithm soon!
