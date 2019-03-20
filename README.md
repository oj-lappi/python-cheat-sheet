
# Variabler

Variabler är behållare som innehåller värden

I python är allt som inte är ett nyckelord och är utan ""-tecken en variabel

Vi initialiserar (skapar) variabler genom tilldelningsoperatorn =



```python
#Tilldelningsoperatorn =
#Tilldelar (sparar) värdet på höger sida in i variabeln (behållaren) på vänster sida
#Om variabeln inte finns, skapas den nu

#Värdet på höger sida kan vara variabel eller ett bokstavligt värde

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

#Tupler: listor som inte går att ändra

(1,2,3)

#En tupel med ett element måste ha ett komma-tecken efter elementet, annars evalueras det bara som ett simpelt värde

("element",)#tupel som innehåller strängen "element"

("element") #strängen "element"

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

8//3 #== 2 (heltalsdivision, 3 ryms 2 gånger i 8)
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



# If

En if-sats är ett flödeskontroll-block, som låter programmet välja vad som ska hända näst.

Hur programmet väljer


```python
#If-block
a = 3
#If-blocket består av ett uttryck i huvudet som evalueras till sant eller falskt


if a > 2:
    print("Hej!")
    
#Vi kan även genast använda sanningsvärden som vi tidigare beräknat

solen_skiner = True

if solen_skiner:
    print("solen skiner!")


fyra_är_jämnt = 4 % 2 == 0

if fyra_är_jämnt:
    print("Halleluja, fyra är ett jämnt tal!")
```

    Hej!
    solen skiner!
    Halleluja, fyra är ett jämnt tal!
    

# Else

```else``` och ```elif``` kollas efter att ```if```-villkoret har misslyckats (dvs. villkoret har haft ett falskt värde)

```elif``` kollar dessutom ett villkor till, medan else körs oavsett 

det går att lägga hur många som helst elif efter varann


```python
#If-elif-else-sats

a = 0

if a > 2:
    print("Hej?")
elif a >0:
    print("Hej maybe")
else:
    print("Hejdå")
```

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
    

# While-else

Vi kan, som med ```if```, lägga en else efter en while-sats.

Denna kör då villkoret inte är sant, helt som en if-sats.

I praktiken betyder detta att else-satsen körs efter att resten av loopen har körts.


```python
a = 1
while a < 4:
    a+=1
    print("running")
else:
    print("slut")
```


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


```python

```

    running
    running
    running
    slut
    

# Klasser och objekt

Ett objekt är en samling av variabler och funktioner som kan hämtas med hjälp av .-operatorn.

Objekt skapas genom att initialisera en klass. En klass är alltså en bottenplan för ett objekt.
Då ett objekt initialiseras så kopieras klassen in i objektet och sedan körs ```__init__```-funktionen för klassen med objektet som ```self```

## Klass-deklaration

En klass är ett block som alla andra


```python
#nyckelordet class
#|    klassens namn 
#|    |
#|    |  kolon!
#|    |  |
class Dog:#<-kolon!
    
    def __init__(self,name):
        self.name = name
        
    def bark(self):
        print(self.name, "says: Woof!")
    
    def info():
        print("a dog class")
```

En klass är lite som ett eget program som du kan köra när du vill. Ett eget "namespace" som det kallas.

Det betyder att alla variabler, funktioner, och andra programmeringsobjekt som har deklarerats inne i Dog finns tillgängliga, men de ligger alltså inne i ```Dog``` namnrummet.

Alla variabler, funktioner, etc. som vi vanligtvis kallar på ligger i programmeringsfilens eget namnrum, för dem behöver vi inte specifiera namnrum, utan de kan kallas direkt.

För att komma åt variabler i andra namnrum använder vi ```.```-operatorn:

    <namnrum>.<namn>
    
Dvs. för att koma åt ```info```-funktionen i ```Dog``` kallar vi på ```Dog```**.**```info()```


```python
Dog.info()
```

    a dog class
    

Ett objekt är en kopia av Dog-namnrummet, vi skapar objektet genom att *kalla* på klassen Dog, dvs. vi skriver ```Dog()```. När vi kallar på Dog, körs ```Dog.__init__()``` med argumenten:
 - ```self```=objektet vi skapar
 - resten av argumenten fylls i av vad vi ger in i ```Dog()```


```python
dog=Dog("Kalle")
```

När vi kallar på funktioner i ett objekts namnrum, lägger python alltid __objektet__ __själv__ in i funktionens första argument, därför brukar det första argumentet kallas ```self```.


```python
#Nu kan vi kalla på dog.bark()
dog.bark()
```

    Kalle says: Woof!
    

P.g.a. detta kan vi inne i funktionerna komma åt information som är sparat på objektet, i detta fall hundens namn.

    class Dog:
        ...
        def bark(self):
            print(self.name, "says: Woof!") <-- self.name = namnet vi sparade när vi kallade på Dog(), alltså "Kalle"
        ...
        
Vi kan också komma åt namnet direkt från dog.


```python
dog.name
```




    'Kalle'



Men märk att det inte går att kalla på funktioner som inte har några argument, eftersom python alltid tvingar in objektet själv som första argumentet.


```python
dog.info()#TypeError
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-21-65ed32909515> in <module>()
    ----> 1 dog.info()#TypeError
    

    TypeError: info() takes 0 positional arguments but 1 was given


# Ärvning

Om det redan finns en klass som gör 90% av vad du vill åstadkomma, men du skulle vilja lägga till lite funktionalitet, hur skall man göra då? Vi kan ärva (eng. inherit) klassen, alltså lägga till nya bitar till den existerande klassen.

När en klass ärver en annan klass kallas den nya klassen en subklass till den existerande klassen. Vice versa kallas den gamla klassen en superklass till den nya klassen.

Ärvning betyder att vi skapar en klass som utökar en annan klass. Dvs. klassen innehåller alla variabler och funktioner som superklassen har + alla variabler deklarerade i klassen själv. Vi kan **skriva över** variabler och funktioner från superklassen genom att omdefiniera dem. I följande exempel skriver vi över ```__init__```-funktionen.

Ärvning sker genom att ge superklassen in som argument till klassen.

    class Subklass(Superklass):

Detta betyder också att vi kan använda funktionalitet från superklassen i vår klass, såsom i följande exempel.


```python
#             ärver Dog-klassen
#             |
class Collie(Dog):

#       När vi omdefinierar __init__ i Collie skriver vi över den från Dog ärvda __init__-funktionen med den nya funktionen.
#       |
    def __init__(self):
        Dog.__init__(self,"Lassie") #Vi bestämmer att alla Collies har namnet Lassie
#       |
#       Vi kan t.ex. använda __init__ från Dog för att förenkla klassen
```


```python
collie = Collie()
collie.bark()
```

    Lassie says: Woof!
    

```Collie``` är en subklass till ```Dog```, som skiljer sig från ```Dog``` i att vi har hårdkodat namnet "Lassie" till den, annars fungerar ```Collie``` exakt som ```Dog```.

Eftersom vi skrev om ```__init__``` för ```Collie``` så att den endast tar in ```self```-argumentet kallar vi på ```Collie``` utan argument.

Inne i ```__init__``` kallar vi på ```Dog.__init__``` för att skapa en Dog som fungerar. Märk att vi nu måste ge in ```self``` som ett argument, eftersom vi kallar på ```__init__``` explicit, som vilken som helst annan funktion (explicit = uttryckligen, det är vi som kallar på ```__init__``` och inte nån magisk bakgrundsmekanism). 
