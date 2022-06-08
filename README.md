# python-question
### create a python game take input from user "snake, water, gun" and computer generate random value  out of it 
### water wins from gun , gun wins from snake , sanke wins from water just count the score and give the result who won computer or user
## its same as rock paper scissor game

import random


items=["snake","water",'gun']

u_result=[0]
c_result=[0]

for i in range(1,5):
    print("turn",i,"of 10")
    user=input("pick one 'snake','water','gun': ")
    comp=random.choice(items)
    print("computer ouput: ",comp)
    
    
    if comp==user:
        u_result.append(0)
        c_result.append(0)
    elif comp=="water" and user=="snake":
        u_result.append(1)
    elif comp=="gun" and user=="snake":
        c_result.append(1)
    elif comp=="snake" and user=="gun":
        u_result.append(1)
    elif comp=="water" and user=="gun":
        c_result.append(1)
    elif comp=="snake" and user=="water":
        c_result.append(1)
    elif comp=="gun" and user=="water":
        u_result.append(1)
    
    final_c_result=sum(c_result)
    print("computer score: ",final_c_result)
    final_u_result=sum(u_result)
    print("user score: ",final_u_result)
    
    print()
    print()
    
    
    

final_c_result=sum(c_result)
print("final computer score: ",final_c_result)
final_u_result=sum(u_result)
print("Final user score: ",final_u_result)
if final_u_result<final_c_result:
    print("opps computer wins")
if final_u_result==final_c_result:
    print("opps computer wins")
else:
    print("hoorey you win")
    
    
   
    
    
    
