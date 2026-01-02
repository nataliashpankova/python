Al programma viene fornita una stringa di testo contenente la lettera "h" almeno due volte come input. Scrivere un programma che restituisca la stringa originale e inverta la sequenza di caratteri tra la prima e l'ultima occorrenza della lettera "h".

text = str(input())
text_updated = ''

first_h_index = text.find('h')
last_h_index = text.rfind('h')

for i in range(0, first_h_index):
    text_updated += text[i]

for i in range(last_h_index, first_h_index, -1):
    text_updated += text[i]

for i in range(last_h_index, len(text)):
    text_updated += text[i]
    
print(text_updated)

----------------------------------------------------------

s = input()

first_h = s.find("h")
last_h = s.rfind("h")

res = s[: first_h + 1] + s[first_h + 1 : last_h][::-1] + s[last_h:]

print(res)

----------------------------------------------------------

s = input()
print(s[:s.find('h')] + s[s.rfind('h'):s.find('h'):-1] + s[s.rfind('h'):])
