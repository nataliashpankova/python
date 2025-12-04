# python

Il programma dovrebbe produrre 10 volte il testo "Python è fantastico!" (senza virgolette), ciascuna su una riga separata.

for i in range(10):
    print("Python is awesome!")


Un numero naturale viene fornito come input al programma. N( N≥2 )– un cateto di un triangolo rettangolo isoscele.
Scrivere un programma che stampi un triangolo stellato.

n = int(input());

for i in range(n):
    print("*" * (n-i))


Al programma vengono forniti come input tre numeri naturali. M ,P ,N:
M: numero iniziale di organismi;
P: aumento medio giornaliero di %;
N:numero di giorni per la riproduzione.
Scrivi un programma che preveda la dimensione della popolazione degli organismi con 1-esimo di N-esimo giorno (incluso). Il programma dovrebbe restituire il numero del giorno, seguito da uno spazio, e la dimensione della popolazione in quel giorno.

m = int(input());
p = int(input());
n = int(input());

for i in range(1, n+1):
    print(i, m)
    m += m * (p / 100)


Sono dati due numeri interi M e N ( M>N ). Scrivi un programma che stampi tutti gli interi dispari da M a N(incluso) in ordine decrescente.

m = int(input());
n = int(input());

for i in range(m, n - 1, -1):
    if i % 2 != 0:
        print(i)


Sono dati due numeri naturali M e N (M≤N). Scrivi un programma che stampi tutti gli interi da M a N (incluso), che soddisfa almeno una delle condizioni:
il numero è un multiplo di 17
il numero termina in 9
il numero è un multiplo di 3 e 5 simultaneamente

m = int(input());
n = int(input());

for i in range(m, n + 1):
    if (i % 17 == 0) or (i % 10 == 9) or (i % 3 == 0 and i % 5 == 0):
        print(i)


Un numero naturale è dato N. Scrivi un programma che stampi la tabella di moltiplicazione. N (da 1 A 10 incluso).

n = eval(input())

for i in range(1, 11):
    print(n, "x", i, "=", n * i)


Al programma vengono forniti due numeri interi come input N e B (N≤B). Scrivi un programma che conti il ​​numero di numeri nell'intervallo da N a B(incluso), il cui cubo termina in 4 or 9.

a = int(input());
b = int(input());
count = 0;

while a <= b:
    if (((a**3) % 10 == 4) or ((a**3) % 10 == 9)):
        count = count + 1;
    a = a + 1;
print(count);


Un numero naturale viene fornito come input al programma. N scrivi un programma per calcolare una somma alternata.

n = eval(input())
s = 0

for i in range(n + 1):
    s = s + (-1)**(i + 1) * i

print(s)
