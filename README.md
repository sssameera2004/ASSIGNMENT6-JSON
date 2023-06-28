THE CODE OF ASSIGNMENT 1 WAS IMPLEMENTED IN VS CODE AS THERE WERE JSON FILES AND THAT CODE AND OUTPUT IS COPIED FROM THERE. SO, CODE IS NOT RUNNING IN THIS JUPYTER NOTEBOOK
ASSIGNMENT -1 ---------- QUESTION - 1
import json
class Employee:
    def __init__(self,name,dob,height,city,state):
        self.name = name
        self.dob = dob
        self.height = height
        self.city = city
        self.state = state
        
# with open(r"C:\Users\Hp\OneDrive\Desktop\Edyoda Practice\Edyoda Python Assignment 6\employee.json") as file:
#     data = json.load(file)
file = open(r"C:\Users\Hp\OneDrive\Desktop\Edyoda Practice\Edyoda Python Assignment 6\employee.json")
data = json.load(file)
employees = []
for i in data["employees"]:
    name = i["name"]
    dob = i["DOB"]
    height = i["Height"]
    city = i["city"]
    state = i["state"]

    employee = Employee(name,dob,height,city,state)
    employees.append(employee)

for i in employees:
    print("Name : ",i.name)
    print("DOB : ",i.dob)
    print("Height : ",i.height)
    print("City : ",i.city)
    print("State : ",i.state)
    print()
EMLPOYEE JSON FILE
{"employees" : [{"name": "Ram","DOB":"01/01/1997","Height":"5.8","city":"Noida","state":"Uttar Pradesh"},
{"name": "Raj","DOB":"10/05/1996","Height":"5.1","city":"Bhatinda","state":"Punjab"},
{"name": "Rahul","DOB":"12/01/1998","Height":"6.2","city":"Gurgaon","state":"Haryana"},
{"name": "Rohan","DOB":"01/04/1995","Height":"5.9","city":"Pune","state":"Maharashtra"},
{"name": "Rehan","DOB":"11/01/1999","Height":"6.0","city":"Shimla","state":"Himachal Pradesh"}]}
OUTPUT IN VS CODE
Name : Ram DOB : 01/01/1997
Height : 5.8 City : Noida State : Uttar Pradesh

Name : Raj DOB : 10/05/1996
Height : 5.1 City : Bhatinda
State : Punjab

Name : Rahul DOB : 12/01/1998
Height : 6.2 City : Gurgaon State : Haryana

Name : Rohan DOB : 01/04/1995 Height : 5.9 City : Pune State : Maharashtra

Name : Rehan DOB : 11/01/1999 Height : 6.0 City : Shimla State : Himachal Pradesh

PS C:\Users\Hp\OneDrive\Desktop\Edyoda Practice>

ASSIGNMENT - 1 ----------- QUESTION - 2
import json
dict1 = {'Haryana':'Chandigarh','Maharashtra':'Mumbai','Karnataka':'Bangluru','Rajasthan':'Jaipur','Uttar Pradesh':'Lucknow','Gujarat':'Gandhinagar','Goa':'Panaji'}
file = open(r"C:\Users\Hp\OneDrive\Desktop\Edyoda Practice\Edyoda Python Assignment 6\assignment_7_file.json","w")
json.dump(dict1,file)
OUTPUT IN JSON FILE
{"Haryana": "Chandigarh", "Maharashtra": "Mumbai", "Karnataka": "Bangluru", "Rajasthan": "Jaipur", "Uttar Pradesh": "Lucknow", "Gujarat": "Gandhinagar", "Goa": "Panaji"}

ASSIGNMENT - 2
class Dog:
    def __init__(self,name,age,coat_color):
        self.name = name
        self.age = age
        self.coat_color = coat_color

    def description(self):
        print(f"Name : {self.name} \nAge : {self.age}")
    
    def get_info(self):
        print(f"Coat_color : {self.coat_color}")
    
class JackRussellTerrier(Dog):
    def __init__(self, name, age, coat_color,trained):
        super().__init__(name, age, coat_color)
        self.trained = trained
    
    def owner(self):
        print(f"Owner of {self.name} dog is Mr. John.")
        
    def city(self):
        print(f"{self.name} lives in Los Angeles with his owner.")

class Bulldog(Dog):
    def __init__(self, name, age, coat_color,friendly):
        super().__init__(name, age, coat_color)
        self.friendly = friendly

    def height(self):
        print(f"Height of {self.name} is 2 feet.")
    
    def weight(self):
        print(f"Weight of {self.name} is 50kg.")

dog = Dog("Pablo",4,"Black and White")
dog.description()
dog.get_info()

jack = JackRussellTerrier("Skuby",5,"Black","yes")
jack.description()
jack.get_info()
jack.owner()
jack.city()

bull = Bulldog("Tyson",3,"Brown","Yes")
bull.description()
bull.get_info()
bull.height()
bull.weight()
Name : Pablo 
Age : 4
Coat_color : Black and White
Name : Skuby 
Age : 5
Coat_color : Black
Owner of Skuby dog is Mr. John.
Skuby lives in Los Angeles with his owner.
Name : Tyson 
Age : 3
Coat_color : Brown
Height of Tyson is 2 feet.
Weight of Tyson is 50kg.
