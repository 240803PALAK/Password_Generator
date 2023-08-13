#Password Generator


    import random

    def passwordgenerator(type):
           a=""
           list1=["A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O", "P", "Q", "R", "S", "T", "U", "V", "W",
                  "X", "Y", "Z", "a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", 
                  "v", "w", "x", "y", "z"]
           list2=[0,1,2,3,4,5,6,7,8,9,0]
           list3= ["~","!","@","$","%","^","&","*","_","-","+","="]
           if type==3:
                  random_number=[]
                  random_number.append(random.sample(list1,2))
                  random_number.append(random.sample(list3,1))
                  random_number.append(random.sample(list2,2))
           if type==2:
                  random_number=[]
                  random_number.append(random.sample(list1,3))
                  random_number.append(random.sample(list2,3))
                  random_number.append(random.sample(list3,1))
           if type==1:
                  random_number=[]
                  random_number.append(random.sample(list1,3))
                  random_number.append(random.sample(list3,2))
                  random_number.append(random.sample(list2,4))
           for i in random_number:
                  for j in i:
                         a=a+str(j)
           print(''.join(random.sample(a,len(a))))
    print("Enter type of password")
    choice=int(input("1.Strong\n2.Normal\n3.Easy\n"))
    passwordgenerator(choice)






