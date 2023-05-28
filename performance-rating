import numpy as np

numberPlayers = int(input("Enter number of rounds: "))
yourScore = float(input("Enter your tournament score: "))
playerRatings = []
for i in np.arange(0,numberPlayers):
    inputRating = int(input("Enter player post evemt rating: "))
    playerRatings = np.append(playerRatings,inputRating)

normLevels=[1200,1400,1600,1800,2000,2200,2400]

delta = [normLevels-playerRatings[i] for i in np.arange(0,len(playerRatings))]
CT=np.zeros((numberPlayers,7))
for i in np.arange(0,7):
    for j in np.arange(0,numberPlayers):
        if delta[j][i]<=-400:
            CT[j][i]=0
        elif -400<delta[j][i]<=0:
            CT[j][i]=0.5+delta[j][i]/800
        elif 0<delta[j][i]<=200:
            CT[j][i]=0.5+delta[j][i]/400
        elif 200<delta[j][i]:
            CT[j][i]=1
STCT=yourScore-np.sum(CT,axis=0)
locations=np.where(STCT>1)[0]
norm=locations[-1]
if norm == 0:
    print("4th category norm")
elif norm == 1:
    print("3rd category norm")
elif norm == 2:
    print("2rd category norm")
elif norm == 3:
    print("1st category norm")
elif norm == 4:
    print("CM norm")
elif norm == 5:
    print("LM norm")
elif norm == 6:
    print("LSM norm")
