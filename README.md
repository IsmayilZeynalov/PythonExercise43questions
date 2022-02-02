# PythonExercise43questions
#(1)Düzbucaqlı üçbucağın sahəsini hesablayan funksiya yazın

a = float(input("a-i daxil edin: "))
h = float(input("h-i daxil edin: "))
S = 0.5*a*h

print(S)

#(2)Sözdən təkrarlanan hərfləri silən funksiya yazın

a = input("Enter a string: ")
s = ""
for i in a:
    if s == "" or i != s[len(s) - 1]:
        s = s + i
print(s)

#(3)Verilmiş ədədin içində bütün rəqəmlərin olub olmamasını yoxlayan funksiya yazın

my_int = input("Eded = ")
my_list = ["0","1","2","3","4","5","6","7","8","9"]
olmayan = ""

for n in my_list:
    if not n in my_int:
        olmayan += n + " "

if len(olmayan) != 0:
    print(f"Ededin icinde olmayan reqem: {olmayan}")
else:
    print("Ededin icinde butun reqemler var")
    
    
 #(4)Nömrələrin qiymətlərini yoxlayan funksiya yazın

nomre , emsal = input("Nomre: ").strip(), 0
if nomre[0:2] == "10" or nomre[0:2] == "77" or nomre[0:2] == 90:
    emsal += 3
if nomre[3].lower() == nomre[4].lower():
    emsal += 4
if nomre[6] == nomre[7] and nomre[7] == nomre[8]:
    emsal += 5
if nomre[6] != nomre[7] and nomre[6] == nomre[8]:
    emsal += 4

nomrenin_qiymeti = emsal * 60

print(nomrenin_qiymeti)



    
    
    
