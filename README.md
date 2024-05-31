# Coordinate-Game

Boy is standing at coordinate A while girl is standing at coordinate B. In one step, boy can increase or decrease his coordinate by at most  K. Determine the minimum number of steps required by boy to reach girl.

Input
The only line of input contains three integers N, Y and K denoting the initial coordinate of boy, the initial coordinate of girl and the maximum number of coordinates boy can move in one step.

Constraints:
1 ≤ X, Y ≤ 100
1 ≤ K ≤ 100
Output
Return the minimum number of steps required by boy to reach girl.

def minimum_steps(X, Y, K):
    distance = abs(Y - X)
    
    steps = distance // K
    
    if distance % K != 0:
        steps += 1
    
    return steps

X, Y, K = map(int, input().split())

print(minimum_steps(X, Y, K))
