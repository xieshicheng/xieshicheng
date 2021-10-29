def table():
    #在这里写下您的乘法口诀表代码吧！
    for i in range (1,9):
        for j in range(1,i+1):
            print(j,'*',i,'=',i*j,' ',end="");
            if i==j:
                print();
    

if __name__ == '__main__':
    table()
    
    
    
    
 #导入OS模块
import os
#待搜索的目录路径
path = "Day1-homework"
#待搜索的名称
filename = "2020"
#定义保存结果的数组
result = []

def findfiles():
    #在这里写下您的查找文件代码吧！
    count=1
    for root,dirs,files in os.walk(path):
        for filename in files:
            if "2020" in filename:
                result.append([count,root+"/"+filename])
                count+=1
    for i in result:
        print (i)
    

    

if __name__ == '__main__':
    findfiles()
