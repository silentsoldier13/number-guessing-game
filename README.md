# number-guessing-game
Enter a value between 1 and 100. Have fun.
import random
import time

print("""***************************************************
SAYI TAHMİN OYUNU OYNAYALIM
1 ile 100 arasında sayıyı tahmin et!

****************************************************""")

rastgele_sayı=random.randint(1,100)
tahmin_hakkı=7

while True:


    tahmin=int(input("Tahmininizi giriniz:"))

    if  (tahmin<rastgele_sayı):
        print("Bilgiler sorgulanıyor....")
        time.sleep(1)
        print("Sayınız küçük geldi.yükseltin")
        tahmin_hakkı-=1

    elif (tahmin>rastgele_sayı):
         print("Bilgiler sorgulanıyor....")
         time.sleep(1)
         print("Sayınız büyük geldi.Düşürün")
         tahmin_hakkı-=1


    else:
         print("Bilgiler sorgulanıyor....")
         time.sleep(1)
         print("KAZANDINIZ",rastgele_sayı)
         break

    if   (tahmin_hakkı==0):
         print("Tahmin hakkınız sona ermiştir")
         break
