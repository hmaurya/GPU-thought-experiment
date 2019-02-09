# GPU-thought-experiment
A note from CMU course offered by Kayvon F
## Slide from Lecture 1 
![Thought experiment](https://github.com/hmaurya/GPU-thought-experiment/blob/master/thought_experiment.png)

Take nvidia 480 gpu which has 
> 480 ALU's which means it can do 480 MUL/clock and 
> Clock rate of 1.4 Ghz (means 1.4 * 10^9 operations per sec)

which means the above GPU can (1.4Gig * 480) ~ 700 Multiplications per second
We need 12 bytes of data (A * B = C) for each multiplication in the array. Which means we need (TB) 700 * 12 * 10^9 = 8.4 TB / sec of bandwidth.

But the above GPU supports only (AB =)177 GB/ Sec of bandwidth. Which means we can achieve only AB/TB * 100 =  2.1%, which means we can only achieve ~ 2% of maximum possible speedup in actual GPU. 

In conclusion we are very much limited by the bandwidth in parallelizing the problem domain.
