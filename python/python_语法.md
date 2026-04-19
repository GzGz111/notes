# 基本知识
## 字符串
### title
修改字符串首字母的大小写
```python
name="ada lovelace"
print(name.title())
```
## input
```python
message = input("Tell me something ,and I will repeat it back to you:")
print(message)
```

## format
用于替换花括号的值
```python
first_name="ada"
last_name="loverlace"
full_name="{first_name}{last_name}"
print(full_name)
```
## 添加空白
### 制表符    \t
```python
print("\thellow world")
```
### 换行符    \n
```python
print("hellow\nworld")
```
## 删除空白
### 删除右端空白-rstrip
```python
favorite_language='python    '
favorite_language.rstrip()
```
### 删除左端空白-lstrip
```python
favorite_language='    python'
favorite_language.lstrip()
```
### 删除两侧空白-strip
```python
favorite_language="    python    "
favorite_language.strip()
```
### 删除前缀-removeprefix
```python
nostrach_url='https://nostracth.com'
nostrach_url.removeprefix('https://')
```
## 数
常量要用大写
### 下划线
```python
universe_age=14_000_000_000
```
python不会打印_   而是直接显示14000000000
### 注释
用#作为注释，#后面的内容会被忽视
```python
#无效内容
```
****
****
# 列表
## 列表
用\[]表示列表
```python
fruits=['apple','watermelon','pear','cherry']
print(fruits)
```
result
```
['apple','watermelon','pear','cherry']
```
### 访问列表
列表元素从0开始
```python
fruits=['apple','watermelon','pear','cherry']
print(fruits[0])
```
result:
```
apple
```
特殊情况
```python
fruits=['apple','watermelon','pear','cherry']
print(fruits[-1])
```
result:
```
cherry
```
### 修改，添加和删除元素
#### 修改
```python
fruits=['apple','watermelon','pear','cherry']
print(fruits)
fruits[0]='grape'
print(fruits)
```
result:
```
['apple','watermelon','pear','cherry']
['grape','watermelon','pear','cherry']
```
#### 添加
##### 末尾添加
用append追加列表末尾
```python
fruits=['apple','watermelon','pear','cherry']
print(fruits)
fruits.append('orange')
print(fruits)
```
result:
```
['apple','watermelon','pear','cherry']
['apple','watermelon','pear','cherry','orange']
```
##### 插入元素
可以在任意位置添加新元素，需要特定的索引与值
```python
fruits=['apple','watermelon','pear','cherry']
print(fruits)
fruits.insert(0,'blueberry')
print(fruits)
```
result:
```
['apple','watermelon','pear','cherry']
['blueberry','apple','watermelon','pear','cherry']
```
#### 删除
##### del语句
```python
fruits=['apple','watermelon','pear','cherry']
print(fruits)
del fruits[0]
print(fruits)
```
result:
```
['apple','watermelon','pear','cherry']
['watermelon','pear','cherry']
```
##### pop语句
删除末尾后继续使用，相当于‘弹出’
```python
fruits=['apple','watermelon','pear','cherry']
print(fruits)
popped_fruits=fruits.pop()
print(fruits)
print(popped_fruits)
```
result:
```
['apple','watermelon','pear','cherry']
['apple','watermelon','pear']
cherry
```
pop语句加上索引也可用于删除任意位置的语句
```python
fruits=['apple','watermelon','pear','cherry']
print(fruits)
popped_fruits=fruits.pop(0)
print(fruits)
print(popped_fruits)
```
result:
```
['apple','watermelon','pear','cherry']
['watermelon','pear','cherry']
apple
```
##### remove语句
根据值删除元素
```python
fruits=['apple','watermelon','pear','cherry']
print(fruits)
fruits.remove('pear')
print(fruits)
```
result:
```
['apple','watermelon','pear','cherry']
['apple','watermelon','cherry']
```
## 管理列表
### sort()方法
对列表按字母顺序永久排序
```python
cars=['bmw','audi','toyota','subaru']
cars.sort()
print(cars)
```
result:
```
['audi','bmw','toyoru','subaru']
```
也可以按字母顺序相反的顺序排序
```python
cars=['bmw','audi','toyota','subaru']
cars.sort(reverse=True)
print(cars)
```
result:
```
['subaru','toyota','bmw','audi']
```
### sorted()函数
不改变列表顺序进行排序
```python
cars=['bmw','audi','toyota','subaru']
print(cars)
print(sorted(cars))
print(cars)
```
result:
```
['bmw','audi','toyota','subaru']
['audi','bmw','toyoru','subaru']
['bmw','audi','toyota','subaru']
```
### reverse()方法
反向打印列表，反转列表元素排列顺序。reverse()会永久改变顺序，可以再用一次变回来
```python
cars=['bmw','audi','toyota','subaru']
print(cars)
cars.reverse()
print(cars)
```
result:
```
['bmw','audi','toyota','subaru']
['subaru','toyora','audi','bmw']
```
### len()函数
```python
cars=['bmw','audi','toyota','subaru']
print(len(cars))
```
result:4
## 数值列表
### range
#### 使用range函数
range末尾不会显示
```python
for value in range(1,5):
	print(value)
```
result:
```
1
2
3
4
```
也可以用range(6)代替，直接从0开始
#### 用range创建列表
```python
numbers=list(range(1,6))
print(numbers)
```
result:
```
[1,2,3,4,5]
```

确定步长的方法,在range()的第三个位置即为步长
```python
even_numbers=list(range(2,11,2))
print(even_numbers)
```
result:
```
[2,4,6,8,10]
```

特殊用法，打印列表平方
```python
squares=[]
for value in range(1,11):
	squares.append(value**2)
print(squares)
```
result:
```
[1,4,9,16,25,36,49,64,81,100]
```
### 数值计算
列表推导式
```python
squares=[value**2 for value in range(1,11)]
print(squares)
```
result:
```
[1,4,9,16,25,36,49,64,81,100]
```
### 列表的部分使用
#### 切片
```python
players=['charles','martina','michael','florence','eli']
print(players[1:4])
```
result:
```
['martina','michael','florence']
```

省略索引
```python
players=['charles','martina','michael','florence','eli']
print(players[2:])
```
result:
```
['michael','florence','eli']
```

输出末尾
```python
players=['charles','martina','michael','florence','eli']
print(players[-3:])
```
result:
```
['michael', 'florence', 'eli']
```
### 复制列表
用\[:]
```python
my_food=['pizza','falafel','carrot cake']
friends_food=my_food[:]
print(my_food)
print(friends_food)
```
result:
```
['pizza', 'falafel', 'carrot cake']
['pizza', 'falafel', 'carrot cake']
```
#### 特殊用法
```python
my_food=['pizza','falafel','carrot cake']
friends_food=my_food[:]

my_food.append('cannoli')
friends_food.append('ice cream')

print(my_food)
print(friends_food)
```
result:
```
['pizza', 'falafel', 'carrot cake', 'cannoli']
['pizza', 'falafel', 'carrot cake', 'ice cream']
```
#### 错误示例
重复添加
```python
my_food=['pizza','falafel','carrot cake']
friends_food=my_food

my_food.append('cannoli')
friends_food.append('ice cream')

print(my_food)
print(friends_food)
```
result:
```
['pizza', 'falafel', 'carrot cake', 'cannoli', 'ice cream'] 
['pizza', 'falafel', 'carrot cake', 'cannoli', 'ice cream']
```
# 元组
相当于不可修改的列表,不可以修改元组的元素
```python
dimensions=(200,50)
print(dimensions[0])
print(dimensions[1])
```
result:
```
200 
50
```

可以重新给元组赋值
```python
dimensions=[200,50]
print("Original dimension:")
for dimension in dimensions:
	print(dimension)

dimensions=[600,200]
print("\nModified dimensions")
for dimension in dimensions:
	print(dimension)
```
result:
```
Original dimension: 
200 
50 
Modified dimensions 
600 
200
```
# if语句
```python
cars=["audi","bmw","subaru","toyota"]
for car in cars:
	if car=="bmw":
		print(car.upper())
	else:
		print(car.title())
```
result:
```
Audi 
BMW 
Subaru 
Toyota
```
条件测试：检查是否相等（\==），是否不相等(!=)，数值比较(<,>)，多个条件判断(and)，是否在列表中
```python
banned_users=['andrew','carolina','david']
user="marie"

if user not in banned_users:
	print(f"{user.title()},you can post a respone if you wish.")
```
result:
```
Marie,you can post a respone if you wish.
```
## elif
```python
age = 12
if age < 4:
	price = 0
elif age < 18:
	price = 25
elif age < 65:
	price = 40
else:
	price = 20
print(f"Your admission cost is ${price}.")
```
result:
```
Your admission cost is $25.
```
可以用elif替代最后一个else
# 字典
核心为键值对
##  访问值
```python
alien_0={'color':'green','point':5}

print(alien_0['color'])
print(alien_0['point'])
```
result:
```
green
5
```
## 添加键值对
```python
alien_0={'color':'green','point':5}
print(alien_0)
alien_0['x_position']=0
alien_0['y_position']=25
print(alien_0)
```
result:
```
{'color': 'green', 'point': 5} 
{'color': 'green', 'point': 5, 'x_position': 0, 'y_position': 25}
```
## 创建新字典
```python
alien_0={}
alien_0['color']='green'
alien_0['points']=5
print(alien_0)
```
result:
```
{'color': 'green', 'points': 5}
```
## 修改值
```python
alien_0={'x_position':0,'y_position':25,'speed':'medium'}
print(f"Original position:{alien_0['x_position']}")

if alien_0['speed']=='slow':
	x_increment=1
elif alien_0['speed']=='medium':
	x_increment=2
else:
	x_increment=3
alien_0['x_position']=alien_0['x_position']+x_increment
print(f"New position:{alien_0['x_position']}")
```
result:
```
Original position:0 
New position:2
```
## 删除键值对
```python
alien_0={'color':'green','point':5}
print(alien_0)
del alien_0['point']
print(alien_0)
```
result:
```
{'color': 'green', 'point': 5} 
{'color': 'green'}
```
## get访问值
```python
alien_0={'color':'green','speed':'slow'}
point_value=alien_0.get('point','No point value assigned.')
print(point_value)
```
result:
```
No point value assigned.
```
如果字典中存在get中的键，则获得该值。如果不存在，则获得指定的值。
## 遍历键值对
```python
user_0={'username':'efermi','first':'enrico','last':'fermi'}
for key,value in user_0.items():
	print(f"\nKey:{key}")
	print(f"Value:{value}")
```
result:
```
Key:username 
Value:efermi 

Key:first 
Value:enrico 

Key:last 
Value:fermi
```
key,value可以用其他代替
## 遍历键
```python
favorite_language={'mike':'python','joke':'c','ethan':'java'}
for name in favorite_language.keys():
	print(name.title())
```
result:
```
Mike 
Joke 
Ethan
```
## 遍历值
```python
favorite_language={'mike':'python','joke':'c','ethan':'java'}
for language in favorite_language.values():
	print(language.title())
```
result:
```
Python 
C 
Java
```
## 嵌套
### 字典 in 列表
```python
alien_0={'color':'green','point':5}
alien_1={'color':'yellow','point':10}
alien_2={'color':'red','point':15}

aliens=[alien_0,alien_1,alien_2]

for alien in aliens:
	print(alien)
```
result:
```
{'color': 'green', 'point': 5} 
{'color': 'yellow', 'point': 10} 
{'color': 'red', 'point': 15}
```
### 列表 in 字典
```python
pizza={'crust':'thick','toppings':['mushroom','extra cheese']}
print(f"Your orderd a {pizza['crust']}-crust pizza whith the following toppings:")
for topping in pizza['toppings']:
	print(f"\t{topping}")
```
result:
```
Your orderd a thick-crust pizza whith the following toppings: 
	mushroom 
	extra cheese
```
### 字典储存字典
```python
user={'aeinstein':{'first':'albert','last':'einstein','location':'priceton'},
'mcurie':{'first':'marie','last':'curie','location':'paris'}}
for username,user_info in user.items():
	print(f"\nUsername:{username}")
	full_name=f"{user_info['first']}{user_info['last']}"
	location=user_info['location']
	print(f"\nFull name :{full_name.title()}")
	print(f"\tlocation:{location.title()}")
```
result:
```
Username:aeinstein 
Full name :Alberteinstein 
location:Priceton 
Username:mcurie
Full name :Mariecurie 
location:Paris
```
# while
```python
prompt="\nPlease enter the name of a city you have visited:"
prompt+="\n(Ener 'quit' when you are finished.)"
while True:
	city=input(prompt)
	if city=='quit':
		break
	else:
		print(f"I'd love to go to {city.title()}")
```
result（先输入beijing ，后输入quit）:
```python
Please enter the name of a city you have visited: 
(Ener 'quit' when you are finished.)beijing 
I'd love to go to Beijing 
Please enter the name of a city you have visited: 
(Ener 'quit' when you are finished.)quit
```
## 循环while
要注意避免无限循环
```python
current_number=0
while current_number<10:
	current_number+=1
	if current_number%2==0:
		continue
	print(current_number)
```
result:
```
1 
3 
5 
7 
9
```
## 循环处理列表和字典
### 移动列表元素
```python
unconfirmed_users=['alice','brain','candace']
confirmed_users=[]
while unconfirmed_users:
	current_user=unconfirmed_users.pop()
	print(f"Verifying user: {current_user.title()}")
	confirmed_users.append(current_user)
print("\nThe following users have been confirmed:")
for confirmed_user in confirmed_users:
	print(confirmed_user.title())
```
result:
```
Verifying user: Candace 
Verifying user: Brain 
Verifying user: Alice 

The following users have been confirmed: 
Candace 
Brain 
Alice
```
### 删除列表元素
```python
pets=['dog','cat','dog','goldfish','cat','rabbit','cat']
print(pets)
while 'cat' in pets:
	pets.remove('cat')
print(pets)
```
result:
```
['dog', 'cat', 'dog', 'goldfish', 'cat', 'rabbit', 'cat'] 
['dog', 'dog', 'goldfish', 'rabbit']
```
### 填充字典
```python
responses={}
polling_active=True
while polling_active:
	name=input("\nwhat is your name?")
	response=input("which mountain would you like to climb someday")
	responses[name]=response
	repeat=input("would you like to let another person respond?(yes/no)")
	if repeat=="no":
		polling_active=False
print("\n--- Poll Results ---")
for name,response in responses.items():
	print(f"{name} would like to climb {response}.")
```
result:
```
what is your name?gz 
which mountain would you like to climb somedayQomolangma 
would you like to let another person respond?(yes/no)yes 

what is your name?zg 
which mountain would you like to climb somedaythe alps 
would you like to let another person respond?(yes/no)no 
--- Poll Results --- 
gz would like to climb Qomolangma. 
zg would like to climb the alps.
```
# 函数
形参
```python
def greet_user():
	print("Hello!")
greet_user()
```
result:
```
Hello!
```
实参
```python
def greet_user(username):
	print(f"Hello,{username.title()}!")
greet_user('gz')
```
result:
```
Hello,Gz!
```
## 关键字实参
```python
def describe_pet(animal_type,pet_name):
	print(f"\nI have a {animal_type}.")
	print(f"My {animal_type}'s name is {pet_name.title()}.")
describe_pet(animal_type='hamster',pet_name='harry')
describe_pet(pet_name='harry',animal_type='hamster')
```
request:
```
I have a hamster. 
My hamster's name is Harry. 

I have a hamster. 
My hamster's name is Harry.
```
describe_pet(animal_type='hamster',pet_name='harry')
describe_pet(pet_name='harry',animal_type='hamster')两种写法等效
## 默认值
可以给形参指定默认值。如果在调用函数中给形参提供实参就使用指定的实参值，如果没有就使用形参默认值
```python
def describe_pet(pet_name,animal_type='dog'):
	print(f"\nI have a {animal_type}.")
	print(f"My {animal_type}'s name is {pet_name.title()}.")
describe_pet(pet_name='willie')
```
result:
```
I have a dog. 
My dog's name is Willie.
```
## 返回值
函数不仅可以显示输出，还可以处理数据返回一个或一组词
### 返回简单的值
```python
def get_formatted_name(first_name,last_name):
	full_name=f"{first_name} {last_name}"
	return full_name.title()
musician=get_formatted_name('jimi','hendrix')
print(musician)
```
result:
```
Jimi Hendrix
```
### 可选实参
python会将非空字符串解读成True
```python
def get_formatted_name(first_name,last_name,middle_name=""):
	if middle_name:
		full_name=f"{first_name} {middle_name} {last_name}"
	else:
		full_name=f"{first_name} {last_name}"
	return full_name.title()

musician=get_formatted_name('jimi','hendrix')
print(musician)

musician=get_formatted_name('john','hooker','lee')
print(musician)
```
result:
```
Jimi Hendrix 
John Lee Hooker
```
### 返回字典
函数可以返回任意类型的值
```python
def build_person(first_name,last_name,age=None):
	person={'first':first_name,'last':last_name}
	if age:
		person['age']=age
	return person
musician=build_person('jimi','hendrix',27)
print(musician)
```
result:
```
{'first': 'jimi', 'last': 'hendrix', 'age': 27}
```
### while与函数
```python
def get_formatted_name(first_name,last_name):
	full_name=f"{first_name} {last_name}"
	return full_name.title()
while True:
	print("\nPlease tell me your name")
	print("(enter 'q' to any time to quit)")
	
	f_name=input("First_name:")
	if f_name=='q':
		break
	l_name=input("Last_name:")
	if l_name=='q':
		break
	formatted_name=get_formatted_name(f_name,l_name)
	print(f"\nHellow,{formatted_name}!")
```
result:
```
Please tell me your name 
(enter 'q' to any time to quit) 
First_name:g 
Last_name:z 

Hellow,G Z! 

Please tell me your name 
(enter 'q' to any time to quit) 
First_name:q
```
## 传递列表
```python
def greet_users(names):
	for name in names:
		msg=f"Hello,{name.title()}"
		print(msg)
		
usernames=['hannah','ty','margot']
greet_users(usernames)
```
result:
```
Hello,Hannah 
Hello,Ty 
Hello,Margot
```
### 修改列表
```python
def print_models(unprinted_designs, completed_models):
	while unprinted_designs: 
		current_design = unprinted_designs.pop()
		print("Printing model: " + current_design)
		completed_models.append(current_design)
def show_completed_models(completed_models):
	print("\nThe following models have been printed:")
	for completed_model in completed_models:
		print(completed_model)
unprinted_designs = ['iphone case', 'robot pendant', 'dodecahedron']
completed_models = []
print_models(unprinted_designs, completed_models)
show_completed_models(completed_models)
```
result:
```
Printing model: dodecahedron 
Printing model: robot pendant 
Printing model: iphone case 

The following models have been printed: 
dodecahedron 
robot pendant 
iphone case
```
### 禁止修改列表
可以使用list\[:],用于传递列表副本
```
function_name(list[:])
```
## 任意数量实参
用\*放于实参前，不管语句有多少实参都会被形参收入
```python
def make_pizza(*toppings):
	print(toppings)
make_pizza('pepperoni')
make_pizza('mushroom','green peppers','extra cheese')
```
result:
```
('pepperoni',) 
('mushroom', 'green peppers', 'extra cheese')
```
用\*创建名为toppings的一个元组，使得该元组包含函数收到的所有值。将所有输入的值封装为一个元组
### 任意位置实参和任意数量实参
```python
def make_pizza(size,*toppings):
	print(f"\nMaking a {size}-inch pizza with the following toppings:")
	for topping in toppings:
		print(f"-{topping}")
make_pizza(16, 'pepperoni')
make_pizza(12, 'mushroom','green peppers','extra cheese')
```
result:
```
Making a 16-inch pizza with the following toppings: 
-pepperoni 

Making a 12-inch pizza with the following toppings: 
-mushroom 
-green peppers 
-extra cheese
```
第一个值赋给size，其余值储存在元组
> 通用形参名\*args
### 任意数量关键字实参
```python
def build_profile(first,last,**user_info):
	user_info['firsy_name']=first
	user_info['last_name']=last
	return user_info
	
user_profile=build_profile('albert','einstein',
                           location='princeton',field='physics')
print(user_profile)
```
result:
```
{'location': 'princeton', 'field': 'physics', 'firsy_name': 'albert', 'last_name': 'einstein'}
```
用\*\*user_info创建字典
## 函数储存模块中
1. 导入整个模块
   - 模块是扩展名为.py的文件，包含要导入到程序中的代码。用import导入整个模块
2. 导入特定函数
    - from 模块 import 特定函数1，特定函数2
    - 可以有多个特定函数，用逗号分隔
3. as指定别名
    - from 模块 import 函数 as 别名   
    - import 模块 as 别名
4. 导入所有函数
	- from 模块 import *

# 类
## 创建与使用
```python
class Dog:
	def __init__(self,name,age):
		self.name=name
		self.age=age
		
	def sit(self):
		print(f"{self.name} is now sitting.")
		
	def roll_over(self):
		print(f"{self.name} rolled over!")
my_dog=Dog('willie',6)
your_dog=Dog('Lucy',3)

my_dog.sit()
your_dog.roll_over()
```
类中函数被称为方法。\_\_init_\_()是特殊的一种方法，每当使用该类都会自动运行此方法。其中的形参self必须位于其他形参之前。我们只用给后两个形参提供值
result:
```
willie is now sitting. 
Lucy rolled over!
```
### 属性
#### 设置默认值
```python
class Car:
	def __init__(self,make,model,year):
		self.make=make
		self.model=model
		self.year=year
		self.odometer_reading=0
	
	def get_descriptive_name(self):
		long_name=f"{self.year} {self.make} {self.model}"
		return long_name.title()
		
	def read_odometer(self):
		print(f"This car has {self.odometer_reading} miles on it.")
		
my_new_car=Car('audi','a4',2024)
print(my_new_car.get_descriptive_name())
my_new_car.read_odometer()
```
result:
```
2024 Audi A4 
This car has 0 miles on it.
```
#### 直接修改属性的值
```python
class Car:
	def __init__(self,make,model,year):
		self.make=make
		self.model=model
		self.year=year
		self.odometer_reading=0
	
	def get_descriptive_name(self):
		long_name=f"{self.year} {self.make} {self.model}"
		return long_name.title()
		
	def read_odometer(self):
		print(f"This car has {self.odometer_reading} miles on it.")
		
my_new_car=Car('audi','a4',2024)
print(my_new_car.get_descriptive_name())
my_new_car.odometer_reading=23
my_new_car.read_odometer()
```
result:
```
2024 Audi A4 
This car has 23 miles on it.
```
#### 通过方法修改属性的值
```python
class Car:
	def __init__(self,make,model,year):
		self.make=make
		self.model=model
		self.year=year
		self.odometer_reading=0
	
	def get_descriptive_name(self):
		long_name=f"{self.year} {self.make} {self.model}"
		return long_name.title()
		
	def read_odometer(self):
		print(f"This car has {self.odometer_reading} miles on it.")
		
	def update_odometer(self,mileage):
		self.odometer_reading=mileage
		
my_new_car=Car('audi','a4',2024)
print(my_new_car.get_descriptive_name())
my_new_car.update_odometer(23)
my_new_car.read_odometer()

```
result:
```
2024 Audi A4 
This car has 23 miles on it.
```
#### 通过方法让属性递增
```python
class Car:
	def __init__(self,make,model,year):
		self.make=make
		self.model=model
		self.year=year
		self.odometer_reading=0
	
	def get_descriptive_name(self):
		long_name=f"{self.year} {self.make} {self.model}"
		return long_name.title()
		
	def read_odometer(self):
		print(f"This car has {self.odometer_reading} miles on it.")
		
	def update_odometer(self,mileage):
		self.odometer_reading=mileage
		
	def increment_odometer(self,miles):
		self.odometer_reading+=miles
	
my_new_car=Car('subaru','outback',2019)
print(my_new_car.get_descriptive_name())
my_new_car.update_odometer(23_500)
my_new_car.read_odometer()
my_new_car.increment_odometer(100)
my_new_car.read_odometer()
```
result:
```
2019 Subaru Outback 
This car has 23500 miles on it. 
This car has 23600 miles on it.
```
## 继承
### 子类
super()是一种特殊函数可以调用父类方法，一个类继承另一个类后就可以添加新的属性和方法。子类父类有相同方法时会忽略父类的方法
```python
class Car:
	def __init__(self,make,model,year):
		self.make=make
		self.model=model
		self.year=year
		self.odometer_reading=0
	
	def get_descriptive_name(self):
		long_name=f"{self.year} {self.make} {self.model}"
		return long_name.title()
		
	def read_odometer(self):
		print(f"This car has {self.odometer_reading} miles on it.")
		
	def update_odometer(self,mileage):
		self.odometer_reading=mileage
		
	def increment_odometer(self,miles):
		self.odometer_reading+=miles
	
class ElectricCar(Car):
	def __init__(self,make,model,year):
		super().__init__(make,model,year)
		self.battery_size=40
		
	def describe_battery(self):
		print(f"This car has a {self.battery_size}-kWh battery.")

my_leaf=ElectricCar('nissan','leaf',2024)
print(my_leaf.get_descriptive_name())
my_leaf.describe_battery()
```
result:
```
2024 Nissan Leaf 
This car has a 40-kWh battery.
```
## 导入
1. 导入单个类
- from 模块 import 类
1. 导入多个类
- import 模块
1. 导入所有类
- from 模块 import \*
1. 在一个模块导入另一个模块
- from 模块 import 类
1. 使用别名
- from 模块 import 类 as 别名

# 文件
1. 相对路径以当前程序所在目录的指定位置去查找
2. 绝对路径以系统的根文件夹为起点
## 读取文件
pi.txt为
```txt
3.1415926535
  8979323846
  2643383279
```
部分代码可能无法运行
```python
from pathlib import Path
path=Path('pi.txt')
contents=path.read_text()
print(contents)
```
result:
```
3.1415926535
  8979323846
  2643383279
```
### 访问文件各行
使用splitlines()方法将冗长的字符串转换为多行
```python
from pathlib import Path
path=Path('pi.txt')
contents=path.read_text()
lines = contents.splitlines()
for line in lines:
	print(line)
```
result:
```
3.1415926535
  8979323846
  2643383279
```
### 使用文件内容
```python
from pathlib import Path
path=Path('pi.txt')
contents=path.read_text()
lines = contents.splitlines()
pi_string=''
for line in lines:
	pi_string+=line
print(pi_string)
print(len(pi_string))
```
result:
```
3.1415926535  8979323846  2643383279
36
```
## 写入文件
使用write_text()将数据写入文件
```python
from pathlib import Path

path=Path('programmering.txt')
path.write_text("I love programmering.")
```
result:
```
I love programmering.
```
python只能将字符串写入文本文件，对于数值数据要先用函数str()转换为字符串格式
#### 写入多行
先创建字符串再再传递给write_text()
```python
from pathlib import Path

contents="I love progemmering.\n"
contents+="I love creating new games.\n"
contents+="I also love working with data.\n"

path=Path('programering.txt')
path.write_text(contents)
```
result:
```
I love programmering.
I love creating new games.
I also love working with data.
```
## 异常
1. 0不可以做除数
### try_except
```python
try:
	print(5/0)
except ZeroDivsionError:
	print("you can't divide by zero!")
```
result:
```
you can't divide by zero!
```
### else代码块
```python
print("Give me two numbers,and I'll divide them.")
print("Enter 'q' to quit.")

while True:
	first_number= input("\nFirst number:")
	if first_number=='q':
		break
	second_number=input("\nSecond number:")
	if second_number=='q':
		break
	try:
		answer=int(first_number)/int(second_number)
	except ZeroDivisionError:
		print("Your can't divide by 0!")
	else:
		print(answer)
```
result:
```
Give me two numbers,and I'll divide them. 
Enter 'q' to quit. 

First number:2 

Second number:6 
0.3333333333333333 

First number:q
```
## FileNotFoundError异常
如果系统的默认编码与要读取的文件编码不一致，参数encoding必不可少。encoding就是指定用什么字符编码打开/保存文件
```python
from pathlib import Path

path=Path('alice.txt')
try:
	contents=path.read_text(encoding='utf-8')
except FileNotFoundError:
	print(f"Sorry,the file {path} dose not exist.")
```
result:
```
Sorry,the file alice.txt dose not exist.
```
## 分析文本
调用split()生成列表,再用len()计算个数
```python
from pathlib import Path

path=Path('alice.txt')
try:
	contents=path.read_text(encoding='utf-8')
except FileNotFoundError:
	print(f"Sorry,the file {path} dose not exist.")
else:
	words=contents.split()
	num_words=len(words)
	print(f"The file {path} has about {num_words} words.")
```
代码用于演示，此文本不存在
result:
```
The file alice.txt has about 29594 words.
```
### 使用多个文件
用循环处理
```python
from pathlib import Path

def count_words(path):
	try:
		contents=path.read_text(encoding='utf-8')
	except FileNotFoundError:
		print(f"Sorry,the file {path} dose not exist.")
	else:
		words=contents.split()
		num_words=len(words)
		print(f"The file {path} has about {num_words} words.")
filenames=['alice.txt','siddhartha.txt','moby_dick.txt','little_women.txt']
for filename in filenames:
	path=Path(filename)
	count_words(path)
```
显示代码
result:
```
The file alice.txt has about 29594 words.
Sorry,the file siddhartha.txt dose not exist.
The file moby_dick.txt has about 215864 words.
The file little_women.txt has about 189142 words.
```
### 静默失败
except FileNotFoundError: 这一部分后接pass跳过报错部分
```python
from pathlib import Path

def count_words(path):
	try:
		contents=path.read_text(encoding='utf-8')
	except FileNotFoundError:
		pass
	else:
		words=contents.split()
		num_words=len(words)
		print(f"The file {path} has about {num_words} words.")
filenames=['alice.txt','siddhartha.txt','moby_dick.txt','little_women.txt']
for filename in filenames:
	path=Path(filename)
	count_words(path)
```
result:
```
The file alice.txt has about 29594 words.
The file moby_dick.txt has about 215864 words.
The file little_women.txt has about 189142 words.
```
## 储存数据
JSON是一种轻量的数据结构利于共享数据。常用模块json保存信息，储存数据
### json.dumps()
存储数据
```python
from pathlib import Path
import json

number=[2,3,5,7,11,13]

path=Path('number.json')
contents=json.dumps(numbers)
path.write_text(contents)
```
result:
```
[2,3,5,7,11,13]
```
### json.loads()
读取到内存
```python
from pathlib import Path
import json

path=Path('number.json')
contents=path.read_text()
numbers=json.loads(contents)

print(numbers)
```
result:
```
[2,3,5,7,11,13]
```
