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





