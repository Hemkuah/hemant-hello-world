# CoronaVirus2019
Data of COVID19 cases at different places

 #Number of corona virus cases per day in India till 10 may

import csv
with open(r'C:\Users\lenovo\Desktop\india.csv')as file:
  a=list(csv.reader(file))
a.pop(0)
def india(case):
    list1=[]
    for i in case:
      i[1]=int(i[1])
      list1.append(i[1])
    return list1
date1=[i[0]for i in a]
case1=india(a)
import matplotlib.pyplot as pls
import numpy as np
pls.figure(figsize=(25,12))
pls.xlabel('Date')
pls.ylabel('Total cases')
pls.bar(date1,case1,width=0.9)
pls.xticks(rotation=90)
pls.show()
