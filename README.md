


#
c = int(C[2])
pow(a, 3)

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


    
    
    
