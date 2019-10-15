# Analysis-and-Application-of-Climate-Data
2019 master degree course

## Download Data
 * Dbar txt file
 * TCCIP csv file

## 2019/10/08 開關檔、讀取、分割資料
ˋˋˋpy
fo=open('C:\\Users\\薰云\\Dropbox\\氣候python\\466920.txt','r')
print("1:",fo.name)
print("2:",fo.mode)
print("3:",fo.closed)

A=fo.readline()
print("4:",A)
As=A.split(',')
print("5:",As[0])#[0]是第一個 [1]是第二個
print("6:",As[1])

fo.close()
print("7:",fo.name)
print("8:",fo.mode)
print("9:",fo.closed)
ˋˋˋ


