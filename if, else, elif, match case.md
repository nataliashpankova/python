--1 Scrivi un programma in Python che controlli se un numero intero inserito dall'utente è pari o dispari.

num = int(input())

if (num % 2 == 0):
    print("numero è pari")
else:
    print("numero è dispari")


print("numero è pari" if num % 2 == 0 else "numero è dispari")


--2 Si scriva un codice che, dato un intervallo composto da un limite superiore, uno inferiore ed un numero n, individui se il numero n è interno o esterno all’intervallo.

a = eval(input("Inserire un limite: "))
b = eval(input("Inserire secondo limite: "))
n = eval(input("inserire numero"))

if (a < b):
    if ((n > a) and (n < b)):
        print("SI")
    else:
        print("NO")
else:
    if ((n > b) and (n < a)):
        print("SI")
    else:
        print("NO")


a = int(input("Inserire il limite inferiore: "))
b = int(input("Inserire il limite superiore: "))
n = int(input("Inserire il numero: "));

print("YES" if (n > a) and (n < b) else "NO")


--3 Si scriva un programma in Python che controlli se una persona è maggiorenne ed ha la patente. Si preveda un'alternativa per ogni casistica possibile.

nome = input("Inserire il nome")
eta = int(input("Inserire l'eta: "))
driveLicence = input("Hai la patente? (s = si) (n = no) ")

if (eta > 18):
    print(nome)
    print("Puoi guidare in tutte le paesi se hai la patente." if driveLicence == s else "Non puoi guidare perché non hai la patente")
elif (eta < 18):
    print(nome)
    print("Non puoi avere la patente in EU ma puoi guidare in USA." if (eta >= 16) else "Non puoi guidare da nessuna parte.")


nome = input("Inserire il nome")
eta = int(input("Inserire l'eta: "))
driveLicence = input("Hai la patente? (s = si) (n = no) ")

match driveLicence:
    case s:
        if (eta > 18):
            print(nome)
            print("Puoi guidare in tutte le paesi.")
        elif (eta < 18):
            print(nome)
            print("Non puoi avere la patente in EU ma puoi guidare in USA." if eta >= 16 else "Non puoi guidare da nessuna parte.")
    case n:
        if (eta > 18):
            print(nome)
            print("Puoi prendere la patente.")
        elif (eta < 18):
            print(nome)
            print("Puoi prendere la patente in USA ma non in EU." if eta >= 16 else "Non puoi guidare da nessuna parte.")
