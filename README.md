import random

target = [1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16]
current = [14,5,8,6,11,1,13,10,12,3,7,4,9,2,16,15]
temp = [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0]
action = []
finalaction = []

for j in range(5):
    while(target != current):
        run = random.randint(0, 1) #0: back, 1: right
        if run == 0: #0: back
            for i in range (16):
                if i < 12:
                    temp[i+4] = current[i]
                else:
                    temp[i-12] = current[i]
            current = temp.copy()
            action.append(run)
        else: #1: right
            for i in range (16):
                if (i+1) % 4 != 0:
                    temp[i+1] = current[i]
                else:
                    temp[i-3] = current[i]
            current = temp.copy()
        action.append(run)
    if j == 0 or len(action) < len(finalaction):
        finalaction = action.copy()
        
print(len(finalaction))
print(finalaction)
