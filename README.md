import random
import string 
import time 



def genrate(length = 4):
    letters = string.ascii_letters
    return ''.join(random.choice(letters) for i in range(length))

Length = input('Enter word Len : ')
count = input('Enter How many word to Gen :')

with open('list.txt' , 'w') as file:
    starttime = time.time()
    for x in range(int(count)):
        file.write(genrate(int(Length)) + '\n')

endtime = time.time() - starttime
print(endtime)
print("Done")
