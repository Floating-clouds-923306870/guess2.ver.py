# guess2.ver.py
#另一个猜数游戏(升级版)

import random
目标 =random.randint (1,1001)
目标=100
i=0
n=0
def 检验(a):
    if a>目标:
        print ("再小点")
        return 0
    elif a<目标:
        print ("再大点")
        return 0
    else:
        print(f"没错 就是{目标}")
        return 1
while i==0:
    选数=int(input("> "))
    i=检验(选数)
    n+=1

w=open("游戏记录录.py")
ww=w.read()
r=ww.split("\n") 
w.close()   
w=open("游戏记录录.py","a")
w.write( "\n"+str(n))
w.close()

z=0
for j in r:
    if n>=int(j):
        z+=1
    else:
        www=1
ss=1000           
for j in r:
     if int(j)<ss:
         ss=j
     else:
         www=1
if z==0:
    print(f"新纪录！只有{n}次")
else:
    exit(f"你没有超越其他玩家\n最高纪录{ss}次")
    
