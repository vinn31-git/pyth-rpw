# pyth-rpw
import string
import random

s1=list(string.ascii_lowercase)
s2=list(string.ascii_uppercase)
s3=list(string.digits)
s4=list(string.punctuation)
print("Enter the length of password: ")

user = int(input())

while True:
    
   if user<8:
       print("Your password should be atleast 8 digits")
       user = int(input("Enter the length of your password again: "))
       
   else:
         break
     
     
 
random.shuffle(s1)
random.shuffle(s2)
random.shuffle(s3)
random.shuffle(s4)

part1= round(user * 0.3)
part2= round(user * 0.2)

result = []

for x in range(part1):
    result.append(s1[x])
    result.append(s2[x])
    
for x in range(part2):
    result.append(s3[x])
    result.append(s4[x])   
    
random.shuffle(result)


password = "".join(result) 
print("Strong Password:  ", password)     
      
       
    
    

