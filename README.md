# Project001
# ThaiPASS task1
import math
N_max=int(1000)
print('Maximum number is set to', N_max)
getnum=int(input('Type an integer '))

if getnum<0 or getnum>N_max:
    print('The given number is out of the allowed range. Please try again')
else:
    print('The number you typed is',getnum)

#is the value odd or even?
if math.modf(getnum/2)[0]!=0:
    print(getnum,'is an odd number')
else:
    print(getnum,'is an even number')
    

#is the value prime?
primecheck=0
for n in range(2,getnum,1):
    if math.modf(getnum/n)[0]!=0:
        primecheck=primecheck
    else:
        primecheck=primecheck+1

if primecheck==0:
    print(getnum,'is a prime number')
else:
    print(getnum,'is not a prime number')

    
#is the value a square factor?
sqcheck=0
for m in range(2,getnum,1):
    if m**2==getnum:
        sqcheck=sqcheck+1
    else:
        sqcheck=sqcheck

if sqcheck==0:
    print(getnum,'is not a square factor')
else:
    print(getnum,'is a square factor')


#Is the value on the Fibonacci sequence?
fibo1=0
fibo2=1
fiboseq=[]
fibotemp=1
fibocheck=0
while fibo1<=N_max:
    fiboseq.append(fibo1)
    fibotemp=fibo1
    fibo1=fibo2+fibo1
    fibo2=fibotemp
    
print('Fibonacci sequence in the range of 0 to',N_max, 'is',fiboseq)
    
for p in fiboseq:    
    if p-getnum==0:
        fibocheck=fibocheck+1 
    else:
        fibocheck=fibocheck
   
if fibocheck!=0:
    print(getnum,'is IN Fibonacci sequence')
else:
    print(getnum,'is NOT IN Fibonacci sequence')

