rate_1 = float(input('Enter rate of interest for Bank 1: '))
compound_1 = int(input('Enter number of compounding periods for Bank 1: '))
rate_2 = float(input('Enter rate of interest for Bank 2: '))
compound_2 = int(input('Enter number of compounding periods for Bank 2: '))
rate_3 = float(input('Enter rate of interest for Bank 3: '))
compound_3 = int(input('Enter number of compounding periods for Bank 3: '))

print("")
print("")
print("")

comp_1 = (rate_1 / compound_1) / 100
comp_2 = (rate_2 / compound_2) / 100
comp_3 = (rate_3 / compound_3) / 100
K_1 = (1 + comp_1) ** compound_1
K_2 = (1 + comp_2) ** compound_2
K_3 = (1 + comp_3) ** compound_3
apy_1 = (K_1 - 1) * 100
apy_2 = (K_2 - 1) * 100
apy_3 = (K_3 - 1) * 100
apy_1_str = str(round(apy_1, 3))
apy_2_str = str(round(apy_2, 3))
apy_3_str = str(round(apy_3, 3))

apy_list = ["apy_1", "apy_2", "apy_3"]
for x in apy_list:
    print(x)



for x in apy_list:
    balanace_1 = ((apy_1 / 100) * 1000) + 1000
    balanace_2 = ((apy_2 / 100) * 1000) + 1000
    balanace_3 = ((apy_3 / 100) * 1000) + 1000

print('APY for Bank 1 is ' + apy_1_str + '%.')
print('APY for Bank 2 is ' + apy_2_str + '%.')
print('APY for Bank 3 is ' + apy_3_str + '%.')

print("")
print("")

if apy_1 > apy_2 and apy_1 > apy_3:
    print("Bank 1 is better than Bank 2 and Bank 3")
elif apy_2 > apy_1 and apy_2 > apy_3:
    print("Bank 2 is better than Bank 1 and Bank 3")
elif apy_3 > apy_1 and apy_3 > apy_2:
    print("Bank 3 is better than Bank 1 and Bank 2")
else:
    print("Inputs are Invalid")

print("")
print("")

print(balanace_1)
print(balanace_2)
print(balanace_3)

print("")
print("")

bank_comp_1 = apy_1 > apy_2
bank_comp_2 = apy_2 > apy_3
bank_comp_3 = apy_1 > apy_3

while bank_comp_1 or bank_comp_2 or bank_comp_3:
    if bank_comp_1:
        print(apy_1)
        break
    if bank_comp_2:
        print(apy_2)
        break
    if bank_comp_3:
        print(apy_3)
        break

if (bank_comp_1 and bank_comp_2 and bank_comp_3) == False:
    print("false")
