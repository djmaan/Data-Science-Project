Build an AI to minimize the engery consumption in a server with Deep Q-Learning
Minimizing the energy consumption in a server will minimize the cost

Parameters:
• the average atmospheric temperature over a month
• the optimal range of temperatures of the server, which will be [18◦C, 24◦C]
• the minimum temperature of the server below which it fails to operate, which will be −20◦C
• the maximum temperature of the server above which it fails to operate, which will be 80◦C
• the minimum number of users in the server, which will be 10
• the maximum number of users in the server, which will be 100
• the maximum number of users in the server that can go up or down per minute, which will be 5
• the minimum rate of data transmission in the server, which will be 20
• the maximum rate of data transmission in the server, which will be 300
• the maximum rate of data transmission that can go up or down per minute, which will be 10

Variables:
• the temperature of the server at any minute
• the number of users in the server at any minute
• the rate of data transmission at any minute
• the energy spent by the AI onto the server (to cool it down or heat it up) at any minute
• the energy spent by the server’s integrated cooling system that automatically brings the server’s temperature back to the optimal range whenever the server’s temperature goes outside this optimal range

Assumption 1:
server temperature = b0 +b1 ×atmospheric temperature+b2 ×number of users+b3 ×data transmission rate

Assumption 2:
Et = α|∆Tt| + β = α|Tt+1 − Tt| + β

Et is the energy spent by the system onto the server between times t and t + 1 minute
∆Tt is the change of the server’s temperature caused by the system between times t and t + 1 minute
Tt is the temperature of the server at time t
Tt+1 is the temperature of the server at time t + 1 minute
α > 0
β ∈ R

Defining the states.
The input state st at time t is composed of the following three elements:
1. The temperature of the server at time t.
2. The number of users in the server at time t.
3. The rate of data transmission in the server at time t

Defining the actions.
The AI cools down the server by 3◦C
The AI cools down the server by 1.5◦C
The AI does not transfer any heat to the server (no temperature change)
The AI heats up the server by 1.5◦C
The AI heats up the server by 3◦C

Defining the rewards.
Rewardt = Energy saved by the AI between t and t + 1
= Et^noAI − Et^AI
= |∆TnoAIt| − |∆TAIt|
