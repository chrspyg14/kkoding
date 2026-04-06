

&#x20;  Vending Machine Program



\# Daftar menu

menu = {

&#x20;   1: ("Fanta", 7000),

&#x20;   2: ("Teh Pucuk", 5000),

&#x20;   3: ("Air Aqua", 3000),

&#x20;   4: ("Nescafe", 10000),

&#x20;   5: ("Indomilk", 7500)

}



\# Input saldo

saldo = int(input("35.000,00 (Rp): "))



\# Validasi saldo negatif

if saldo < 0:

&#x20;   print("Error: Saldo tidak boleh negatif!")

&#x20;   exit()



total\_belanja = 0

keranjang = \[]



while True:

&#x20;   print("\\n=== Daftar Minuman ===")

&#x20;   for key, value in menu.items():

&#x20;       print(f"{key}. {value\[0]} - Rp{value\[1]}")



&#x20;   try:

&#x20;       pilihan = int(input("Pilih minuman (1-5): "))

&#x20;   except:

&#x20;       print("Input harus berupa angka!")

&#x20;       continue



&#x20;   # Validasi pilihan

&#x20;   if pilihan not in menu:

&#x20;       print("Menu tidak tersedia!")

&#x20;       continue



&#x20;   nama, harga = menu\[pilihan]

&#x20;   keranjang.append((nama, harga))

&#x20;   total\_belanja += harga



&#x20;   lanjut = input("Tambah minuman lain? (y/n): ").lower()

&#x20;   if lanjut == 'n':

&#x20;       break



\# Final check

print("\\n=== STRUK PEMBELIAN ===")

for item in keranjang:

&#x20;   print(f"- {item\[0]}: Rp{item\[1]}")



print(f"Total Belanja: Rp{total\_belanja}")

print(f"Saldo Awal: Rp{saldo}")



if saldo >= total\_belanja:

&#x20;   kembalian = saldo - total\_belanja

&#x20;   print("Transaksi berhasil!")

&#x20;   print(f"Kembalian: Rp{kembalian}")

else:

&#x20;   kekurangan = total\_belanja - saldo

&#x20;   print("Maaf, saldo tidak cukup.")

&#x20;   print(f"Kekurangan: Rp{kekurangan}")  

