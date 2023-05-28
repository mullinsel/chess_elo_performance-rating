import numpy as np

R0 = int(input("Input current rating: "))
Nrounds = int(input("Input number of rounds: "))
N = int(input("Total number of games played ever: "))
S = float(input("Input your score for the tournament: "))
Ri = [int(input("Input player ratings: "))for i in np.arange(0,Nrounds)]

def W(X,Y):
    return 1/(1+np.power(10,-(X-Y)/400))

def bonus(a,b):
    return (a+b+np.abs(a-b))/2

Nstar = round(50/(np.sqrt(0.662+0.00000739*(2569-R0)*(2569-R0))),1)

if Nstar < N:
    Nprime = Nstar
else:
    Nprime = N

K = 800/(Nprime+Nrounds)

E = [W(R0,i) for i in Ri]
Efinal = np.sum(E)

Rs = R0 + K*(S-Efinal)+bonus(0,K*(S-Efinal)-14*np.sqrt(bonus(Nrounds,4)))
print(round(Rs))
