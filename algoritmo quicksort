import itertools
import time
from random import randint
import timeit
import matplotlib as mpl
import matplotlib.pyplot as plt
  
  
def desenhaGrafico(x,y,xl = "Entradas", yl = "Saídas"):
    fig = plt.figure(figsize=(10, 8))
    ax = fig.add_subplot(111)
    ax.plot(x,y, label = "Tempo no caso qualquer")
    
    ax.legend(bbox_to_anchor=(1, 1),bbox_transform=plt.gcf().transFigure)
    plt.ylabel(yl)
    plt.xlabel(xl)
    plt.show()


def geraLista2(tam):
    lista = []
    for i in range(tam,1,-1):
        lista.append(i)       
    
    return lista
  

x2 = [100000,200000,300000,400000,500000,1000000,2000000]
y = []
y2= []
z = []
z2 = []


def partition(arr,l,h): 
    i = ( l - 1 ) 
    x = arr[h] 
  
    for j in range(l , h): 
        if   arr[j] <= x: 
  
            
            i = i+1
            arr[i],arr[j] = arr[j],arr[i] 
  
    arr[i+1],arr[h] = arr[h],arr[i+1] 
    return (i+1) 
  

def quickSortIterative(arr,l,h): 
  
 
    size = h - l + 1
    stack = [0] * (size) 
  
   
    top = -1
  
    
    top = top + 1
    stack[top] = l 
    top = top + 1
    stack[top] = h 
  
   
    while top >= 0: 
  
      
        h = stack[top] 
        top = top - 1
        l = stack[top] 
        top = top - 1
  
       
        p = partition( arr, l, h ) 
  
       
        if p-1 > l: 
            top = top + 1
            stack[top] = l 
            top = top + 1
            stack[top] = p - 1
  
        
        if p+1 < h: 
            top = top + 1
            stack[top] = p + 1
            top = top + 1
            stack[top] = h 
  

arr = [4, 3, 5, 2, 1, 3, 2, 3] 
n = len(arr) 
quickSortIterative(arr, 0, n-1) 
print ("Sorted array is:") 
for i in range(n): 
    print ("%d" %arr[i]), 
  

for i in range(len(x2)):
    
    array = geraLista2(x2[i])
    inicio = timeit.default_timer()

    quickSortIterative(array,0,len(array)-1)
    fim = timeit.default_timer()
    y.append('%f' %(fim - inicio))
    
    print(y)
    
    
    
    
  desenhaGrafico(x2,y)
  
  
  
  
