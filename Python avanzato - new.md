Si crei un software per un archivio segreto che contiene informazioni sui supereroi e supercattivi di un universo a fumetti. Tutti i personaggi condividono alcune caratteristiche comuni, ma ogni categoria ha anche delle proprietà specifiche.
Creare una classe base PersonaggioFumetto che contenga:
•	Nome reale
•	Nome in codice
•	Età (incapsulata)
•	Città
Implementare:
•	Un metodo scheda() che restituisca una rappresentazione testuale delle informazioni.
•	Un codice che impedisca di inserire età negative.
Creare due sottoclassi:
•	Supereroe: con un attributo aggiuntivo potere_principale
•	Supercattivo: con un attributo aggiuntivo livello_pericolo (da 1 a 5)
Personalizzare il metodo scheda() in entrambe le sottoclassi per aggiungere le informazioni specifiche.
Creare infine alcuni oggetti delle due classi, modificare le proprietà usando e stampare le schede.

#Creare una classe base PersonaggioFumetto
#che contenga;
class PersonaggioFumetto:
    def __init__(self, nomeReale, nomeInCodice, eta, citta):
        self.nomeReale = nomeReale
        self.nomeInCodice = nomeInCodice
        self._eta = eta
        self.citta = citta

    @property
    def eta(self):
        return self._eta
#Un codice che impedisca di inserire età negative.
    @eta.setter
    def eta(self, etaPersonaggio):
        if etaPersonaggio < 0:
            raise ValueError("Eta non valida")
        self._eta = etaPersonaggio

    def scheda(self, informazioni):
        self.informazioni = informazioni
        return (f' Anagrafica di {self.nomeReale} con un sopranome {self.nomeInCodice} ha {self._eta} appartene a {self.citta} preso dall {self.informazioni} ')

#Supereroe: con un attributo aggiuntivo potere_principale
#class SuperEroe eredità da class PersonaggioFumetto
class SuperEroe(PersonaggioFumetto):
    def __init__(self, nomeReale, nomeInCodice, eta, citta, potere_principale, informazioni):
        PersonaggioFumetto.__init__(self, nomeReale, nomeInCodice, eta, citta)
        self.potere_principale = potere_principale
        self.informazioni = informazioni

    def scheda(self):
        return(f'Informazioni {self.informazioni}')

#Supercattivo: con un attributo aggiuntivo livello_pericolo (da 1 a 5)
class SuperCattivo(PersonaggioFumetto):
    def __init__(self, nomeReale, nomeInCodice, eta, citta, livello_pericoloso, informazioni):
        PersonaggioFumetto.__init__(self, nomeReale, nomeInCodice, eta, citta)
        self.livello_pericoloso = livello_pericoloso
        self.informazioni=informazioni

    def scheda(self):
        return(f'Informazioni {self.informazioni}')

supererroe_uno = SuperEroe("Havan Flores", "Chapa", 14, "Roma", "eletro", "Ha perso il suo telefono")
supererroe_due = SuperEroe("Dana Heath", "Mika", 13, "Napoli", "voce", "E' intelegente")
supererroe_tre = SuperEroe("Luca Luhan", "Bose", 12, "Milano", "gravitazione", "E' bello")
supererroe_quatro = SuperEroe("Terrence Little Gardenhigh", "Miles", 13, "Torino", "teletrasport", "Ha una gemella")

supercattivo_uno = SuperCattivo("Frankie Grande", "Frankini", 25, "Roma", 3, "Ama ballare")
supercattivo_due = SuperCattivo("Zoran Korach", "Goomer", 20, "Pisa", 1, "Non è furbo")
supercattivo_tre = SuperCattivo("Ben Giroux", "Bambino", 40, "Roma", 4, "Basso di alteza")

print(supererroe_uno.nomeReale, supererroe_uno.nomeInCodice, supererroe_uno.eta, supererroe_uno.citta, supererroe_uno.potere_principale, supererroe_uno.scheda(), sep = "\n")
print("-" * 50)
print(supercattivo_uno.nomeReale, supercattivo_uno.nomeInCodice, supercattivo_uno.eta, supercattivo_uno.citta, supercattivo_uno.livello_pericoloso, supercattivo_uno.scheda(), sep = "\n")


--ESERCIZIO 2--

Si scelga un contesto che appassioni (es. videogiochi, animali, sport, musica, film, libri, scienza, viaggi, ecc.) e si progetti un programma.

class MusicaDiPianoforte:
    def __init__(self, autore, titolo, anno, tonalita):
        self.autore = autore
        self.titolo = titolo
        self._anno = anno
        self._tonalita = tonalita

    @property
    def anno(self):
        return self._anno

    @anno.setter
    def anno(self, value):
        if value < 0:
            raise ValueError("Anno errato")
        self._anno = value

    @property
    def tonalita(self):
        return self._tonalita

    @tonalita.setter
    def tonalita(self, ton):
        match ton:
            case "#":
                self._tonalita = "Fa diez"
            case "##":
                self._tonalita = "Do diez"
            case "###":
                self._tonalita = "Sol diez"
            case "####":
                self._tonalita = "Re diez"
            case "#####":
                self._tonalita = "La diez"
            case "######":
                self._tonalita = "Mi diez"
            case "#######":
                self._tonalita = "Si diez"
            case "b":
                self._tonalita = "Si diez"
            case "bb":
                self._tonalita = "Mi diez"
            case "bbb":
                self._tonalita = "La diez"
            case "bbbb":
                self._tonalita = "Re diez"
            case "bbbbb":
                self._tonalita = "Sol diez"
            case "bbbbbb":
                self._tonalita = "Do diez"
            case "bbbbbbb":
                self._tonalita = "Fa diez"
            case _:
		raise ValueError("Non esiste")
    
