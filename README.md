# file-write-read
to py
# coding=utf-8

"""
File read and write operations
     Have a file holding student notes
"""

# Yazmak için dosya oluştur

dosya = open('notlar.text', 'w')

notlar = {
    "ali": 45,
    "ahmet": 90,
    "veli": 75,
    "mehmet": 60,
    "serdar": 85,
    "ayse": 40
}

for item in notlar.items():
    dosya.write(str(item))
    dosya.write('\n')

dosya.close()

# Reopen the file for reading
dosya = open('notlar.text', 'r')
for i in dosya.readlines():
    print(i)

dosya.close()
