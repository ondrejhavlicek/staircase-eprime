# staircase-eprime
Customized staircase procedure in E-Prime 2

How to create a staircase procedure that can find a threshold value for some stimulus (e.g., duration of a display, loudness of a sound..)?

I have found a nice basic solution by Hairston and Maldjian (2009) [http://www.sciencedirect.com/science/article/pii/S016926070800206X] and further worked on it to allow the kind of adaptive staircase procedures as described in the nice paper Garcı́a-Pérez, M. A. (1998). Forced-choice staircases with fixed step sizes: asymptotic and small-sample properties. Vision research, 38(12), 1861-1881. I have generalized it to allow combining various up-down rules with step-up/step-down ratios (e.g. I am using a 3-down/1-up rule with a 3/4 delta-down/delta-up ratio to achieve ca. 84% accuracy; it works very well), and fixed what I think was an error in determining the occurrence of a reversal in sequences longer than 1. It is quite likely the original authors have made some improvements on their code before they published it, but I wasn’t able to get my hands on the new code.

My reading notes from García-Pérez describe, how to set the parameters of the staircase procedure to achieve some given accuracy threshold. There are many interesting tips in the paper, such as recommendation to use large and unequal step sizes, and I recommend reading it. (Also, the code could be improved based on some of the recommendations.. Perhaps someone could do it?;-))

The staircase combines transformed and weighted methods to achieve the most reliable convergence. You can use this formula for calculating the accuracy limit to which it should converge in 2AFC (two-alternatives forced-choice task):

Acc = (StepUpSize/(StepUpSize+StepDownSize))^(1/NumOfConsecutiveCorrectResponsesForDown)

E.g. transformed 3-in-a-row-correct=down/1-incorrect=up staircase with the weight of 4 steps up and 3 steps down gives: (4/7)^(1/3) = 83 %

Currently the E-Prime "experiment" involves a simple visual search task and the staircase is finding a threshold stimulus presentation duration, but you can modify it for other types of tasks. How to do that is beyond the scope of this description:-)

Feel free to email me (ohavlicek at gmail) if you like it or dislike it or want to suggest some changes;-)

