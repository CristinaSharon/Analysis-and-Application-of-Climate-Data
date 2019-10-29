# Analysis-and-Application-of-Climate-Data
2019 master degree course

## Download Data
 * Dbar txt file
 * TCCIP csv file

## 2019/10/08 open()、readline()、split()、close()
```py
fo=open('C:\\Users\\薰云\\Dropbox\\氣候python\\466920.txt','r')
print("1:",fo.name)
print("2:",fo.mode)
print("3:",fo.closed)

A=fo.readline()
print("4:",A)
As=A.split(',')
print("5:",As[0])  #[0]是第一個 [1]是第二個
print("6:",As[1])

fo.close()
print("7:",fo.name)
print("8:",fo.mode)
print("9:",fo.closed)
```

## 2019/10/15 for&while loop、if()、1-D plot
### if()
```py
fo=open('C:\\Users\\薰云\\Dropbox\\氣候python\\466920.txt','r')

A=fo.readline()
print(A)
As=A.split(',')
print(As[0])

if (As[5]=="TX01"):
    print('YES')

fo.close()
```

### numpy、matplotlib
```py
import numpy as np   #陣列
import matplotlib.pyplot as plt
x=np.arange(10)
print(x)
y=np.arange(10)
y2=np.zeros(10)
plt.plot(x,y,'y:p')
plt.plot(x,y2,'b:s')
```


## 2019/10/22 matrix, no value
```py
import numpy as np   
import matplotlib.pyplot as plt
#匯入函數庫
#################### 1. 為了畫圖我要矩陣 ############
x=np.arange(50000)
T=np.zeros(50000)
#################### 1. 完成50000的矩陣 #############

fo=open('C:\\Users\\薰云\\Dropbox\\氣候python\\466922.txt','r')

n=0 #角標 n
#開始迴圈，碰到break才停止，小心變成無限迴圈
while True:
    A=fo.readline()
    if A: #假設A有值的狀況下
        As=A.split(',')
        
        if(As[5]!="TX01"):     #如果切到的東西不是TX01
            T[n]=float(As[5])  #字串轉為浮點數，放到T矩陣
        
            if(T[n]==-9999):   #假如值是-9999
                T[n]=None      #把他替換成無效值
                pass           #完成一次
            n=n+1              #邁向下一行
            pass
        pass
    else:               #假如沒有讀到東西 斷
        break

print(n)               #我想看看我做了幾次
plt.plot(x[0:n],T[0:n],'r')  #畫紅圖

fo.close()
```


## 2019/10/29 year average


