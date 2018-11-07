
# Variabler

Variabler är behållare som innehåller värden

I python är allt som inte är ett nyckelord och är utan ""-tecken en variabel

Vi initialiserar (skapar) variabler genom tilldelningsoperatorn =



```python
#Tilldelningsoperatorn =
#Tilldelar (sparar) vänster sida in i variabeln (behållaren) på höger sida
#Om variabeln inte finns, skapas den nu

#Höger sida kan vara variabel eller värde


#Ex.

tal = 1

namn = "kalle"

inköpslista = ["äppel","banan"]

#Om vi vill skapa en tom variabel använder vi ett passande "tomt" värde på höger sida

#Ex

tal = 0        #0 kan vara passande "tomt" värde för tal

efternamn = "" #Tom sträng (tom text) är passande för textdata

objekt = None  #Specialvärde som python-skaparna har bestämt att betyder "inget"

todo_list = [] # Tom lista


```


```python
#Datatyper

#Det finns några olika typer av data i python
#Datatypen bestämms av python enligt hur variabeln ser ut

#Heltal
1

4

5555

#Decimaltal

0.3

4.5

3.14

#Sanningsvärden, finns bara två

True

False


#Strängar = listor av bokstäver

"Kalle"

'Tjorven'

"""
Lång text
på flera rader
"""

#Listor av saker

[1,2,3,4]

["Hej","Godda","Gokväll"]

[1,"äppel",3.14,"hej"]

#Kan t.o.m. lägga listor in i listor

[[1,2,3],["a","b","c","d"]]

#Dictionaries (ordböcker)

#Jämför en nyckel (en sträng eller ett nummer) som du ger in mot en lista av nycklar, och returnerar värdet.

#Deklareras somkommaseparerade nyckel:värde innanför {}

#Exempel:

primtal = {
    1:False,
    2:True,
    3:True,
    4:False,
    5:True,
    6:False,
    7:True,
    8:False,
    9:False,
    10:False
}

djur = {
    "hund":"Människans bästa vän",
    "katt":"Roliga på internet",
    "orm":"Farlig"
}

#Vi hämtar värden med hjälp av nyckeln

primtal[3]#True

djur["hund"]#"Människans bästa vän"

#Återigen kan vi ha hur komplicerade strukturer som helst

ställen={
    "Europa":{
        "Population":741447158,
        "Yta":10180000,#km^2
        "Länder":["Finland","Sverige","Danmark","Norge","Tyskland","Frankrike","Storbritannien","Belgien","Schweiz","Nederländerna"]
    },
    "Afrika":{
        "Population":1225080510,
        "Yta":30370000,#km^2,
        "Länder":["Etiopien","Ghana","Egypten","Elfenbenskusten","Kongo","Sydafrika","Botswana","Namibien"]
    },
    "Nordamerika":{
        "Population":579024000,
        "Yta":24709000,
        "Länder":["Förenta staterna","Kanada","Mexico","Kuba","Haiti","Jamaica","Barbados","Nicaragua"]
    }
}

#Obs! Ta inte ovan som en geografisk sanning, det fattas många länder
```


```python
#Aritmetiska operationer (räkneroperationer)

#Python har bland annat dessa räkneoperationer som operatorer (enkla symboler)
# +  addition 
# -  subtraktion
# *  multiplikation
# /  division
# %  resten av division
# ** vänster sida upphöjt till höger sida
# // höger-sida-roten av vänster sida

#Ex.

1+1 #== 2

1-1 #== 0

2*2 #== 4

4/2 #== 2

5%2 #== 1 (Resten av 5/2)

2**3 #== 8 (2^3)

8//3 #== 2 (tredje roten av 8)
```


```python
#Specialoperatorer

a = a+1

a +=1

a = a**2

a **=2
```


```python
#Jämförelse-operationer
#Det går att jämföra värden för att få sanninsvärden

1 < 2 #== True

1 > 2 #== False

2 > 2 #==False

2 =>2 #större än eller lika med ==True

2 <=2 #mindre än eller lika med

2 ==2 #lika med == True

2 !=2 #inte lika med

#Boolska operatorer
#kombinerar sanningsvärden

#and: både ock

1 < 2 and 1 < 3 #== True .Både 1 < 2 och 1 < 3 måste vara sanna

#or: antingen eller

1 < 2 or 2 < 1  #== True . Nåndera av 1 < 2 eller 2 < 1 måste vara sann

#not: negation

not 1 < 2 #Inverterar sanningsvärdet. True blir False, False blir True

ett_är_minst = (1 < 2 and 1 < 3)

ett_är_inte_minst = not ett_är_minst
```

# Block

Vissa strukturer i python program är block

Block är: 

 - if-satser
 - if-else-satser
 - for-satser
 - while-satser
 - funktioner
 - klasser

Block består av ett huvud och en kropp

Huvudet börjar med en sträng som identifierar blockets typ, slutar alltid med ett kolon, alltså :

Kroppen av ett block är indenterat (flyttat in till höger på sidan)




```python
#If-block
a = 3
#If-blocket består av ett uttryck i huvudet som evalueras till sant eller falskt


if a > 2:
    print("Hej!")
    
#If-else-sats

a = 0

if a > 2:
    print("Hej?")
elif a >0:
    print("Hej maybe")
else:
    print("Hejdå")
```

    Hej!
    Hejdå
    

# Loopar


```python


#For-loopar
#Med for-block kan loopa genom iteratorer
#Exempel på iteratorer är listor

frukt_lista= ["banan","äppel","citron"]

print("\nfrukt_lista")
#Forblocket består av:

#for
#|  loopvariabel (eller variabler)
#|    |   nyckelordet in
#|    |   |  iterator   kolon!
#|  __|__ |  ____|_____ |
for frukt in frukt_lista:
    print(frukt,"är en frukt")
    #Inne i loopen innehåller loopvariabeln frukt varje värde i iteratorn, ett värde åt gången
    
#För dicts (ordböcker) kan vi packa upp dicten i två variabler, nyckel & värde

#Exempel dict
frukt_dict= {"banan":"söt",
               "äppel":"söt",
               "citron":"sur"
              }


print("\nfrukt_dict")
#Då måste vi först kalla på dictens .items() funktion, annars får vi bara nycklarna

#   första loopvariabeln
#     |   andra loopvariabeln
#   __|__ _|__
for frukt,smak in frukt_dict.items():
    print(frukt,"är en",smak,"frukt")
    
#Vi kan också enkelt loopa över tal med hjälp av range() funktionen (eller xrange)

#range(x) ger ett intervall av tal från 0 till x-1

print("\nrange(5)")
for i in range(5):
    print(i)
#range(x,y) ger ett intervall av tal från x till y-1

print("\nrange(2,5)")
for i in range(2,5):
    print(i)

```

    
    frukt_lista
    banan är en frukt
    äppel är en frukt
    citron är en frukt
    
    frukt_dict
    banan är en söt frukt
    äppel är en söt frukt
    citron är en sur frukt
    
    range(5)
    0
    1
    2
    3
    4
    
    range(2,5)
    2
    3
    4
    


```python
#While-loopar

#while-loopar loopar inte över en iterator, som for loopar, utan de loopar så länge som ett sanninsuttryck är sant

#en while loop kan bli en oändlig loop om man glömmer att uppdatera variabler som är en del av villkoret

i = 0

#while
#|
#|    villkor
#|    __|___
while i < 10:
    print(i)
    i+=1
```

# Loopkontrol

Det går att ändra på programmeringsflöde inne i en loop:

 - break 
  - tar dig ut ur loopen
 - continue
  - tar dig till början av loopkroppen, ifall av for-loop avancerar loopvariabeln en framåt


```python
print("exempel: break")
import random
while True:
    r = random.randint(0,10)
    print(r)
    if r == 5:
        break

print("\nexempel: continue")
#continue exempel

for i in range(1,10):
    if i == 5:
        continue
    print(i)
```

    exempel: break
    3
    7
    6
    4
    4
    9
    0
    9
    8
    10
    6
    10
    9
    9
    10
    7
    3
    8
    7
    1
    8
    1
    7
    2
    9
    8
    2
    5
    
    exempel: continue
    1
    2
    3
    4
    6
    7
    8
    9
    


```python
#Funktionsblock

#Funktionsblocket består av:

#def - alla funktionsblock börjar med def 
#|   funktionens namn - helt som en variabel behöver funktioner ett namn, så att man kan kalla på dem
#|   |             funktionens parametrar, inne i en parentes. Parametrarna är separerade med komman
#|   |             |                     kolon!
#|   |             |                     |
def funktions_namn(parameter1,parameter2):
    a = parameter1+parameter2  #Uträkning (om det behövs)
    return a
#   |
#   |
#   retursats, bestämmer vad funktionens värde blir när den kallas


#För att kalla på en funktion

#använd namnet av funktionen
#|            parentes
#|            |inne i parentesen ge värden som funktionen ska använda för parametrarna, 
#|            || i detta fall blir parameter1 = 1 och parameter2=2
#|            ||
funktions_namn(1,2)


svar = funktions_namn(3,4) #Sparar returvärdet i svar

#Svar kommer att innehålla 7

```
