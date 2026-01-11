Scrivi un programma che stampi il seguente elenco: ['a', 'bb', 'ccc', 'dddd', 'eeeee', 'ffffff', ...]

VERSIONE 1
# put your python code here
words = []

for i in range(26):
    words.append(chr(ord('a') + i) * (i + 1))

print(words)

VERSIONE 2
# put your python code here
print([chr(97 + i) * (i + 1) for i in range(26)])

------------------------------------------------------------------------------------------------------------------------------------------------------------------
Al programma viene fornito come input un numero naturale. N, poi N numeri interi. Scrivi un programma che crei un elenco di cubi a partire dai numeri forniti e poi lo stampi.

# put your python code here
n = eval(input())
list = []

for i in range(n):
    list.append(int(input())**3)
    
print(list)

----------------------------------------------------------------------------------------------------------------------------------------------------------------
Un numero naturale viene fornito come input al programma. N Scrivi un programma che crei un elenco dei divisori del numero di input in ordine crescente e poi stampi questo elenco.

# put your python code here
n = int(input())
list_n = []
for i in range(1, n + 1):
    if n % i == 0:
        list_n.append(i)

print(list_n)

----------------------------------------------------------------------------------------------------------------------------------------------------------
Un numero naturale viene fornito come input al programma. N( N≥2 )Poi entrano loro N numeri interi. Scrivi un programma che crei un elenco dei numeri dati, costituito dalle somme dei numeri adiacenti (0 e 1, 1 e 2, 2 e 3 e cosi via).

# put your python code here
n, a = eval(input()), eval(input())

list_sum = []
for i in range(1, n):
    b = int(input())
    list_sum.append(a + b)
    a = b

print(list_sum)

----------------------------------------------------------------------------------------------------------------------------------------------------------
Al programma viene fornito come input un numero naturale. N, poi N numeri interi. Scrivi un programma che crei un elenco dai numeri forniti, quindi rimuova tutti gli elementi con indici dispari e infine stampi l'elenco risultante.

# put your python code here
n = int(input())
list_senza_dispari = []

for i in range(n):
    numero = int(input())
    if i % 2 == 0:
        list_senza_dispari.append(numero)

print(list_senza_dispari)

# put your python code here
n = int(input())
list_senza_dispari = []

for i in range(n):
    numero = int(input())
    list_senza_dispari.append(numero)

del list_senza_dispari[1::2]
print(list_senza_dispari)

-------------------------------------------------------------------------------------------------------------------




-------------------------------


























