# Input nama dan tentukan target nilai
nama = input("Masukkan nama (Andi/Budi/Citra): ")

if nama == "Andi":
    target = 70
elif nama == "Budi":
    target = 75
else:
    target = 80

print("Target nilai", nama, "adalah", target)
print()

# Siapkan variabel
percobaan = 0      # menghitung sudah berapa kali ujian
lulus = False      # False = belum lulus, True = sudah lulus

# Ulangi ujian maksimal 3 kali (while)
while percobaan < 3 and lulus == False:
    percobaan = percobaan + 1                      # tambah 1 percobaan
    nilai = int(input("Nilai " + str(percobaan) + " : "))

    # Cek apakah nilai sudah mencapai target
    if nilai >= target:
        lulus = True                               # berhasil, perulangan berhenti
    else:
        print("Belum mencapai target, ulangi!")

# Tampilkan hasil akhir
print()
if lulus == True:
    print(nama, "berhasil lulus setelah", percobaan, "kali percobaan!")
else:
    print(nama, "tidak lulus setelah", percobaan, "kali percobaan!")
