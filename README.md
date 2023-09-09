# python-AI-7-
python+AI笔记(7)
# 一阶-四章-while循环案例-九九乘法表
#在python中，print语句是会自动换行的，不换行需要如下格式
print("Hello",end='')
print("world",end='')
#此时输出就不会换行
#在字符串中，有一个特殊符号:\t，效果等于键盘中的tab键，它可以让我们多行字符串进行对齐
print("Hello\tWorld")
print("bala\tbest")
#这个代码输出的World和best是会对齐的
#定义外层循环变量
i=1
while i<=9:
    #定义内存循环的控制变量
    j=1
    while j<=i:
    
        print(f"{j}*{i}={j*i}\t",end='')
        j+=1
    i+=1
    print() #print空内容就是输出一个换行

# 一阶-四章-for循环的基础语法
name="bala"
for x in name:
    #将name的内容挨个取出，赋予x临时变量
    #就可以在循环体内对x进行处理
    print(x)
#注：1.无法定义循环条件，只能被动的取出数据
#2.循环内的语句，需要有空格缩进

# 一阶-四章-for循环案例-数一数有多少字母a讲解
count=0
name="bala"
for  x in name:
    if x=="a"
        count++
print("被统计的字符串中有{count}个a")

# 一阶-四章-range语句
#for循环语句，本质是遍历序列类型
#range语法
range(5)  #语法1:输出会是[0,1,2,3,4]，不含5本身
range(2,5)  #语法2:输出的结果是[2,3,4] 输出包含num1，不包含num2
range(3,8,2)  #语法3:输出为[3,5,7]  num3是step

#大多数range都是配合for使用的
for x in range(10):  #in后面的部分叫做待处理的数据集
    print(x)

for x in range(10):
    print("送玫瑰花")
#用range来锁定for循环的循环次数，来达到特殊的目的

# 一阶-四章-for循环临时变量作用域
for i in range(5):
    print(i)
print(i)
#这种写法可编译，但是不规范，需要在循环外面访问临时变量，需要在循环前面提前声明一个临时变量，这样才能完美的输出
i=0
for i in range(5):
    print(i)
print(i)
#这种代码可行
