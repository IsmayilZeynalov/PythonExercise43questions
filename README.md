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


#(5)Ədədin onu təşkil edən rəqəmlərin cəminə qalıqsız bölündüyünü müəyyən edən funksiya yazın
eded, yeni_eded = input("Ədəd = "), 0

if eded.isdigit():
	for i in eded:
		yeni_eded += int(i)

	if int(eded) % yeni_eded == 0:
		print(f"Bəli, {eded} ədədi {yeni_eded} ədədinə bölünür.")
	else:
		print(f"Xeyr, {eded} ədədi {yeni_eded} ədədinə bölünmür.")

else:
	print("Error")
    
#(6)Ədədin rəqəmlərinin hasilinin rəqəm olması üçün neçə dövr getməli olduğunu bildirən funksiya yazın.

a = input("Ededi daxil edin: ")
i = 0
while not len(a) == 1:
    c = 1
    for x in list(a):
        c = c * int(x)
    i += 1
    a = str(c)
print(i)

#(7)3-ə və 5-ə tam bölünən 100-dən kiçik ədədlərin siyahısını çap edən proqram yazın.
for i in range(0, 101):
    if i // 15 == i / 15:
        print(i)
        
        
#(8)Daxil edilmiş ədədə qədər olan cüt ədədlərin sayını tapın

eded = int(input("Ədəd = "))
cut_ededler = 0

for i in range(1, eded+1):
	if i % 2 == 0:
		cut_ededler += 1

print(f"Cüt ədədlərin sayı: {cut_ededler}")

#(9)Verilmiş siyahıda 3-dən böyük ədədləri silmək.[2,2,4,3,6,9,6,1,5,1]

my_list = [2,2,4,3,6,9,6,1,5,1]
my_new_list = []

for i in my_list:
	if i <= 3:
		my_new_list.append(i)

print(my_new_list)

#(10)Trade şirkətində məhsulun 12 aylıq qiymətləri var. Hansı ayda məhsulu alıb digər ayda satsaq daha çox
qazanc əldə etmiş olarıq?
[136,151,125,119,146,133,118,106,138,136,127,101]

qiymet_list = [136, 151, 125, 119, 146, 133, 118, 106, 138, 136, 127, 101]
ucuz_al = qiymet_list.index(min(qiymet_list))
baha_sat = qiymet_list.index(max(qiymet_list))

print(f"Məhsul 01.{ucuz_al + 1}.2022-ci ildə alınıb 01.{baha_sat + 1}.2023-cü ildə satılsa daha çox qazanc əldə olunar.")

#(11)Çıxışda
1 2
2
3 3 3
4 4 4 4
5 5 5 5 5
yazılacaq proqram yazın.

num = int(5)
num2 = 1
for i in range(0, num):
    for j in range(0, num - i - 1):
        print(end=" ")
    for j in range(0, i + 1):
        print(num2, end=" ")
    num2 += 1
    print()
    
#(12)Çıxışda 100-ə qədər olan Fibonaçi ədədlərini göstərən proqram yazın.

fibon_nums = [1, 1]
n = 1

while 100 > fibon_nums[-1]:
    fibon_nums.append(fibon_nums[n] + fibon_nums[n - 1])
    n += 1

if 100 < fibon_nums[-1]:
    fibon_nums.remove(fibon_nums[-1])

print(fibon_nums)

#(13)Girişdə verilmiş istənilən sayda ədədin cəmini çıxışda göstərən proqram yazın.

ededler = input("Ededler: ")
ededler = ededler.split(",")
cem = 0
for eded in ededler:
    cem += int(eded)
print(cem)

#(14)Girişdə verilmiş cümlənin son sözünü çıxışda göstərən proqram yazın.

cumle = input("Cumle: ")
cumle = list(cumle.split(" "))
son_soz = len(cumle) - 1
print(cumle[son_soz])

#(15)Girişdə verilmiş ədədlərin çıxışda kvadratını yazın.

ededler = input("Ededler: ")
ededler = ededler.split(",")
for eded in ededler:
    print(int(eded) ** 2)
    
#(16)100-dən 200-ə qədər 3ə bölünüb 5ə bölünməyən ədələrin sayını tapın

araliq = range(100, 201)
say = 0

for i in araliq:
	if i % 3 == 0 and i % 5 != 0:
		say += 1

print(f"100-dən 200-ə qədər {say} dənə 3-ə bölünüb 5-ə bölünməyən ədəd vardır.")

#(17)Daxil edilmiş cümlədə olan saitlərin sayını tapan proqram yazın.

cumle = input("Cümlə: ")
sait_say = 0
sait_list = "aıoueəiöü"

for i in cumle:
    if i.lower() in sait_list:
        sait_say += 1

print(f"Cümlədə {sait_say} ədəd sait vardır.")


#(18)Verilmiş rəqəmləri muxtəlif olan 9 rəqəmli ədəddə iştirak etməyən rəqəmi çıxışa verən funksiya yazın

my_int = input("Ədəd = ")
my_list = ["0", "1", "2", "3", "4", "5", "6", "7", "8", "9"]
olmayan = ""

for n in my_list:
    if not n in my_int:
        olmayan += n + " "

if len(olmayan) != 0:
    print(f"Ədədin içində olmayan rəqəm(-lər): {olmayan}")
else:
    print("Ədədin içində bütün rəqəmlər vardır.")
    
    
#(19)Verilmiş cümlədəki sözləri əks ardıcıllıqla çıxışa verən funksiya yazın

def reverse_word(s, start, end):
    while start < end:
        s[start], s[end] = s[end], s[start]
        start = start + 1
        end -= 1

s = "Tələbə dərslərə mütləq Tələbə kabineti vasitəsilə daxil olmalıdırlar"
s = list(s)
start = 0
while True:
    try:
        end = s.index(' ', start)
        reverse_word(s, start, end - 1)
        start = end + 1
    except ValueError:
        reverse_word(s, start, len(s) - 1)
        break
s.reverse()
s = "".join(s)
print(s)


#(20)Verilmiş cümlədəki ən qısa sözün çıxışa verən funksiya yazın.

str=input("Enter a line:")
word=str.split()
small=word[0]
for i in range(0,len(word)):
    if len(small)>len(word[i]):
        small=word[i]
print(small)

#(21)Verilmiş cümlədəki ən uzun sözün çıxışa verən proqram yazın

str=input("Enter a line:")
word=str.split()
largest=word[0]
for i in range(0,len(word)):
    if len(largest)<len(word[i]):
        largest=word[i]
print(largest)


#(22)Verilmiş cümlədəki sozlərin sayını çıxışa verən proqram yazın

cumle = input("Cumle daxil edin: ")
space_count = 0
for character in cumle:
    if character == " ":
        space_count = space_count + 1
number_of_words = space_count + 1
print("Cumlede sozlerin sayi: ", number_of_words, sep=" ")

#(23)Daxil edilmiş cümlədə 4 hərifli sozlərin sayını çıxışa verən proqram yazın

cumle = input("Cumle daxil edin: ").strip().split()
dord_herfli_sozler = 0

for i in cumle:
    if len(i) == 4:
        dord_herfli_sozler += 1
    else:
        continue

print("Dord herfli sozlerin sayi: " + str(dord_herfli_sozler))

#(24)Daxil edilmiş cümlədə 'a' hərifi ilə başlayan və sonu 'm' ilə bitən sozləri çıxışa verən proqram yazın.

cumle = input("Cumle daxil edin: ")
herf = "a"
herf1 = "m"
words = cumle.split(" ")
for word in words:
    if word[0] == herf:
        if word[-1] == herf1:
            print(word)
            
#(25)Daxil edilmiş cümlədə sonu 'lar' ilə bitən sozlərin sayını çıxışa verən proqram yazın.

my_str = input("Cümlə: ").strip().split()
say = 0

for i in my_str:
    if i[-3:].lower() == "lar":
        say += 1

print("Cümlədə 'lar' ilə bitən sözlərin sayı:", say)


#(26)Verilmiş cümlədəki sozlərin sayını çıxışa verən proqram yazın

my_str = input("Cümlə: ").strip().split()

print("Cümlədə olan sözlərin sayı:", len(my_str))

#(27)Arqument kimi tək bir sətri götürən və sətirdəki bütün böyük hərflərin indekslərin olduğu sıralanmış
siyahı(list) qaytaran funksiya yaradın. myFunction(“HeLlo WorD”) → [0,2,6,9]

my_str = input("Cümlə ya söz: ")
my_list = []

for i in my_str:
    if i.isupper():
        my_list.append(my_str.index(i))

print(my_list)


#(28)isogram dublikat hərfləri olmayan sözdür. Sətir götürən və "isogram" olub-olmamasından asılı olaraq True və ya
False qaytaran funksiya yaradın.

word = input("enter the word:")


def isogram(word):
    clean_word = word.lower()
    letter_list = []
    for letter in clean_word:
        if letter.isalpha():
            if letter in letter_list:
                return False
            letter_list.append(letter)
    return True


if _name_ == '_main_':
    print(isogram(word))
    
#(29)Bir sətri tamamilə böyük hərflərə və ya tamamilə kiçik hərflərə çevirmək üçün lazım olan ən kiçik addımları (
hansının ən az sayda addım atmasından asılı olaraq) qaytaran funksiya yaradın. Addım bir simvolun kiçik hərfdən böyük
hərfə və ya əksinə dəyişdirilməsindən ibarətdir.


str1 = input("enter the word:")
newStr = ""
for i in range(0, len(str1)):
    if str1[i].islower():
        newStr += str1[i].upper()
    elif str1[i].isupper():
        newStr += str1[i].lower()
    else:
        newStr += str1[i]
print(newStr)

#(30)Üçrəqəmli natural ədəd verilib. Onun Armstronq ədədi olub-olmadığını müəyyən edin. (Armstronq ədədində
rəqəmlərin 3-cü qüvvətinin cəmi həmin ədədə bərabərdir

C = input()
a = int(C[0])
b = int(C[1])
c = int(C[2])
pow(a, 3)
pow(b, 3)
pow(c, 3)
if ((pow(a, 3) + pow(b, 3) + pow(c, 3) == C)):
    print("bu eded amstronq ededidir")
else:
    print("bu eded amstronq ededi deyil")
    
#(31) 4 rəqəmli natural ədəd verilmişdir. Onun palindrom ədəd olduğunu təyin edin

a = int(input())
# xxxx=bczd
b = a // 1000
c = (a // 100) % 10
z = (a % 100) // 10
d = a % 10
if b == d and c == z:
    print("palindrom ədəddir")
else:
    print("bu eded palindrom deyil")
    
#(32). Beşrəqəmli natural ədəd verilmişdir. Ən solda yerləşən rəqəmdən başlayaraq bütün rəqəmlərin artma sırası ilə
yerləşdiyini müəyyən etmək lazımdı

n = int(input())
# abcde
a = n // 10000
b = (n // 1000) % 10
c = (n // 100) % 10
d = (n % 100) // 10
e = n % 10
if a < b < c < d < e:
    print("reqemler artma sirasi ile yerlesib")
else:
    print("reqemler artma sirasi ile yerlesmeyib")
    
#(33)4-rəqəmli tam müsbət ədəd verilmişdir. Bu ədədin öz rəqəmlərin hamısına bölün düyünü təyin edin

n = int(input())
# xxxx=abcd
a = n // 1000
b = (n // 100) % 10
c = (n % 100) // 10
d = n % 10
if n % a == 0 and n % b == 0 and n % c == 0 and n % d == 0:
    print("ədəd öz reqemlerinin hamisina bölünür")
else:
    print("ədəd öz reqemlerinin hamisina bölünmür")
    
    
#34. 4-rəqəmli natural ədədi verilmişdir. Bu ədədin yazılışından cüt rəqəmləri silin (0 - cüt rəqəm kimi qəbul edin).

eded, yeni_eded = input("Ədəd = "), ""
if len(eded) == 4:
	for i in eded:
		if int(i) % 2 != 0:
			yeni_eded += i
else:
	print("Error")

print(yeni_eded)

#35. Dördrəqəmli natural ədəd verilib. Onun rəqəmlərinin bir birindən fərqli olduğunu müəyyən edin. Əgər fərqlidirsə,
"YES" çıxışa verin, əks halda - "NO".

import math


def eyni_reqem(N):
    length = int(math.log10(N)) + 1
    M = (int(math.pow(10, length)) - 1) // (10 - 1)
    M *= N % 10

    if (M == N):
        return "Yes"

    return "No"


N = int(input("Ədəd = "))

print(eyni_reqem(N))

#36. Bir siyahının(list) dayaq nöqtəsi solundakı bütün elementlər ve sağındakı bütün elementlərin cəmi eyni olan bir
ədəddir. Bir siyahının(list) dayaq nöqtəsini tapan funksiya yazın

list1 = [1,2,4,9,10,-10,-9,3]
a = 0
b = 0
for i in range(0, len(list1)):
    for j in range(0,i):
        a += list1[j]
    for j in range(i+ 1, len(list1)):
        b += list1[j]

    if a == b:
        print("dayaq noqtesi: ", list1[i])
    a = 0
    b = 0
    
#37. Verilmiş ədədə qədər olan Fibonaççi ədədlərini çap eden funksiya yazın

fibon_numbers = [1,1]
my_int = 0
n = int(input('Eded: '))

try:
    while n >= fibon_numbers[-1]:
        fibon_numbers.append(fibon_numbers[my_int] + fibon_numbers[my_int + 1])
        my_int += 1
        if fibon_numbers[-1] > n:
            fibon_numbers.remove(fibon_numbers[-1])
except IndexError:
    pass

print(fibon_numbers)

#38.Bir cümələ (və ya söz) və həriflər siyahısı verilmişdir. Cümələdə olan sözərdə siyahıda olmayan hərifləri "-" əvəz
edən funksiya yazın

def replaceWithK(my_str, K):
    replace_ = input("Herfler: ")
    for i in replace_.lower():
        my_str = my_str.lower().replace(i, K)
    return my_str


my_str = input("Cumle: ")

K = "-"
print("Verilmiş cümlə:", my_str)
print("verilmiş spesefik simvol:", K)
print("dəyişdikdən sonra:", replaceWithK(my_str, K))

#39. Daxil edilmiş (input funlsiyasi ilə) ədədə qədər olan 7-yə bölünən ədədlərin hasilini hesablayan funksiya yazin

my_integer = int(input("Eded: "))
my_new_integer = 1

while not my_integer % 7 == 0:
	my_integer -= 1

for i in range(1, int(my_integer / 7) + 1):
	my_new_integer *= i*7

print(my_new_integer)

#40. Yeni siyahı(list) yaradın və daxil edilmiş (input funlsiyasi ilə) ədədə qədər olan və 3 rəqəmi ilə bitən ədədləri
həmin siyahiya əlavə edin

number = int((input('Enter number: ')))
number_list = []
for num in range(0,number):
    if num % 10 == 3:
        number_list.append(num)
print(f"List of numbers ending in 3: {number_list}")

#41. Yeni siyahı(list) yaradın və daxil edilmiş (input funlsiyasi ilə) x ədədindən y ədədinə qədər olan və və 6 - ə
bölunməyən ədədləri həmin siyahiya əlavə edin

number_x = int(input("Select number X: "))
number_y = int(input("Select number Y: "))
number_list = []
for num in range(number_x, number_y):
    if num % 6 != 0:
      number_list.append(num)
print(f"List of numbers that are not divisible by six:{number_list}")

#42. Daxil edilmiş cümlədə 4 hərifli sozlərin sayını çıxışa verən proqram yazın.,

cumle = input("Cümlə: ").strip().split()
soz = 0

for i in cumle:
	if len(i) == 4:
		soz += 1

print(f"Cümlədə {soz} dördhərfli söz var.")

#43. Daxil edilmiş cümlədə sonu 'lar' ilə bitən sozlərin sayını çıxışa verən proqram yazın.

my_str, say = input("Cümlə: ").strip().split(), 0

for i in my_str:
    if i[-3:].lower() == "lar":
        say += 1

print("Cümlədə 'lar' ilə bitən sözlərin sayı:", say)


    
    
    
