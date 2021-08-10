import random

temp = [0,1,1,1,1,1,1,1,1,1]
target = [0,3,3,3,3,3,3,3,3,3]
action = []

while temp != target:
    run = random.randint(1, 9) 
    action.append(run)
    if run == 1:
        temp[1] += 1 if temp[1] != 3 else -2
        temp[2] += 1 if temp[2] != 3 else -2
        temp[4] += 1 if temp[4] != 3 else -2
    elif run == 2:
        temp[1] += 1 if temp[1] != 3 else -2
        temp[2] += 1 if temp[2] != 3 else -2
        temp[3] += 1 if temp[3] != 3 else -2
        temp[5] += 1 if temp[5] != 3 else -2
    elif run == 3:
        temp[2] += 1 if temp[2] != 3 else -2
        temp[3] += 1 if temp[3] != 3 else -2
        temp[6] += 1 if temp[6] != 3 else -2
    elif run == 4:
        temp[1] += 1 if temp[1] != 3 else -2
        temp[4] += 1 if temp[4] != 3 else -2
        temp[5] += 1 if temp[5] != 3 else -2
        temp[7] += 1 if temp[7] != 3 else -2
    elif run == 5:
        temp[2] += 1 if temp[2] != 3 else -2
        temp[4] += 1 if temp[4] != 3 else -2
        temp[5] += 1 if temp[5] != 3 else -2
        temp[6] += 1 if temp[6] != 3 else -2
        temp[7] += 1 if temp[7] != 3 else -2
    elif run == 6:
        temp[3] += 1 if temp[3] != 3 else -2
        temp[5] += 1 if temp[5] != 3 else -2
        temp[6] += 1 if temp[6] != 3 else -2
        temp[9] += 1 if temp[9] != 3 else -2
    elif run == 7:
        temp[1] += 1 if temp[1] != 3 else -2
        temp[4] += 1 if temp[4] != 3 else -2
        temp[5] += 1 if temp[5] != 3 else -2
        temp[7] += 1 if temp[7] != 3 else -2
    elif run == 8:
        temp[5] += 1 if temp[5] != 3 else -2
        temp[7] += 1 if temp[7] != 3 else -2
        temp[8] += 1 if temp[8] != 3 else -2
        temp[9] += 1 if temp[9] != 3 else -2
    else:
        temp[6] += 1 if temp[6] != 3 else -2
        temp[8] += 1 if temp[8] != 3 else -2
        temp[9] += 1 if temp[9] != 3 else -2
        
print(action)
