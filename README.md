# gitPractice

# Disclaimer
Alles wat hier uitgelegd is komt van een beginnend student.  Ik houd geen aansprakelijkheid voor verkeerde resultaten of problemen die ontstaan door het klakkeloos nadoen van wat hier staat. Neem echter gerust contact op als je vragen of opmerkingen hebt.


# Intro
Welkom in de practice repository van klas bin jaar 1. Hier kan iedereen op z'n eigen
gelegenheid dingen uitproberen met git en GitHub. De hoeveelheid features van
GitHub kunnen wat overweldigend zijn. Wees niet bang om ze uit te proberen!

Eerst komt er wat uitleg over [**git**](#git-installeren), en dáárna pas over [**GitHub**](#github). Ze werken nauw samen, maar het zijn verschillende dingen.

De belangrijke functies die we van GitHub kunnen/~~moeten~~ gebruiken in het eerste blok zijn:
  - Online opslag plek
      - Je kunt met je groepje alle scripts op één plek bewaren met de online 'repository' van GitHub.
  - (Grafisch) Versie overzicht
      - Als je werkt aan een bestaand bestand, kun je makkelijk zien wat de veranderingen zijn die iedereen aanbrengt.






### git installeren
om git te kunnen gebruiken moet je het natuurlijk geïnstalleerd hebben.
#### in linux
In de meeste Linux distributies die wij gebruiken (met name Ubuntu) kun je via de terminal met het volgende commando git installeren.
  ```bash
  $ sudo apt install git-all
  ```

#### in windows
Op windows systemen kun [Git Bash](http://git-scm.com/download/win " Git Bash is een versie van git voor Windows") downloaden   .
Als je liever met een grafische user interface werkt kun je dat [hier](https://desktop.github.com/) krijgen

### git instellen
Voordat je met git aan de slag kunt, word het aangeraden om de 'global' variables `user.name` en `user.email` te veranderen. Hiermee laat je git weten wie er gebruik maakt van git. Het maakt in principe niet uit wat je hier invult, maar het wordt wel getoond wanneer je straks commits gaat maken dus denk na over hoe je jezelf noemt. Gebruik in de terminal de volgende commando's:

```bash
git config --global user.name <naam achternaam>
```
```bash
git config --global user.email <naam achternaam>
```
de `--global` marker zorgt ervoor dat je deze variables voor alle git-projecten op de computer zet. Als je per project een andere naam wilt gebruiken moet je dat per map met `git config user.name` aanpassen. [hier meer over het  instellen van git](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup "maar je hoeft dit niet allemaal te doen, hoor")


### Je eerste eigen *lokale* repo maken
Zodra je git goed geïnstalleerd hebt kun je meteen lokaal aan de slag. Wil je straks direct vanuit je terminal dingen uploaden naar GitHub? Zorg dan dat je een GitHub account hebt aangemaakt.

Om een repository met git te initiëren, ga je eerst naar de directory die je wilt tracken met git,
```bash
cd <directorynaam>
```
Om git nu aan het werk te zetten gebruik je het volgende commando:
```
git init
```
Hiermee vertel je git om de bestanden van de huidige directory bij te houden.



###### tip: Om snel je terminal te openen in een specifieke map kun je in Ubuntu in [Nautilus](https://www.linuxquestions.org/questions/ubuntu-63/what-is-nautilus-519503/ "Nautilus is de default file manager van Ubuntu") rechts op een map (of op een wit vlak in een map) klikken en op "Open in Terminal" klikken. Hetzelfde geldt voor Git Bash in windows.
![nautilus](https://github.com/Queuebee2/gitPractice/blob/master/images/ubuntu_open_in_terminal_from_nautilus.PNG?raw=true "How to open a terminal quickly in nautilus" )

Wanneer je dat gedaan hebt kun je bestanden in de directory met de volgende commando's in sync houden met github

|  Command				                   | wat het doet|
| ----------------------             | ----------- |
| `git init `		                     | initaliseert een map |
| `git clone <linkNaarRepo> <naam>`  | kloont (downloadt) een repository  (van bijvoorbeeld GitHub). "`<naam>`" is optioneel, daarmee kun je het je eigen naam geven.|
| `git status `			                 | geeft de current status en staging area|
| `git add <file> `		               | voeg een bestand aan de staging area toe|
| `git add .  `			                 | voeg alle veranderingen aan de staging area toe|
| `git reset HEAD -- <file>`		     | verwijder een bestand uit de lijst van gestagede items|
| `git commit -m "Title" -m "Descr"` |commit staged files met een titel en descriptie message|
| `git push origin master	`	       	 | upload committed files naar de origin's master branch|



### GitHub
GitHub is een soort¿ de online versie van git. Met git kun je (via de terminal) communiceren met GitHub om bestanden/projecten up-todate te houden, te downloaden of juist de uploaden.
Verder biedt GitHub features zoals je die misschien gewent bent van social media platforms zoals Facebook, maar op een zakelijkere manier. Uiteindelijk is het gebruik van GitHub bedoelt voor het delen en bijhouden van code.

### Stappenplan


#### voor een _local_ repoistory
1. `git init` in de map die je gaat gebruiken
2. creëer een bestand
3. `git add . ` voeg je bestanden hiermee aan de staging area toe.
4. `git commit -m "Title" -m "Descr"` 'commit' betekent dat je je toewijd aan de aanpassingen en hiermee definitief de gestagede items in de repository zet.

#### voor een al bestaande (bijv. op GitHub) repository
placeholder text


### Opdracht 1 - pull request
Om deel te nemen aan deze repository wil ik dat je een 'pull-request' maakt. Om dit te doen moet je eerst een 'verandering' hebben om aan te bieden als pull-request.

Probeer op eigen wijze de volgende stappen uit te voeren:

  - klik op create new file
  ![create a new file](https://github.com/Queuebee2/gitPractice/blob/master/images/create_new_file.PNG?raw=true "click here to request the repository owner to add a file you proposed")


  - maak een map met je naam of nickname aan en zet in die map een textbestand "`README`" met wie jij bent. Dit doe je door eerst je (nick)name in te vullen en daarvan een directory te maken door er een '/' achter te zetten. Dan typ je "README.MD" in.


###### Als je het bestand "`README.MD`" ([MD staat voor markdown](https://nl.wikipedia.org/wiki/Markdown "Dit is de normale Markdown, maar GitHub gebruikt zijn eigen versie!")) noemt, kun je jouw readme displayen in jouw map, [zoals in dit voorbeeld](https://github.com/Queuebee2/gitPractice/tree/master/Milain "mijn map en README.MD")


Zoiets als dit:
![creating a readme](https://github.com/Queuebee2/gitPractice/blob/master/images/create_README.PNG?raw=true "Use your own nickname and add a / to make it into a directory.")

Vul daarna onderaan wat informatie over je commit in en klik op 'propose new file'. Hiermee gebeurt het volgende:
  Je 'forkt' deze repo, dat betekent dat je een kopie van deze repository maakt onder jouw naam. Hierin kun je aanpassingen maken en die kun je later met een pull-request aan de oorspronkelijke repo-owner suggereren. Of je kunt er gewoon lekker zelf mee verder.
![commit your file](https://github.com/Queuebee2/gitPractice/blob/master/images/propose_new_file_will_fork.PNG?raw=true "commit and propose the new file")

Maak een pull-request aan.

![create the pull request](https://github.com/Queuebee2/gitPractice/blob/master/images/create_pull_request_stuff_is_gettin_hairy_now.PNG?raw=true "click on create pull request to ask the original repo owner to add your file")

Als alles goed is krijg ik een bericht van je pull-request. Dan kan ik dit 'mergen', en dan wordt je toevoeging deel van het gehele project.

### Opdracht 2
Als je toegang hebt tot deze repository, nodig ik je uit om zelf wat dingetjes te doen. Maak een project aan, maak een issue aan, begin een wiki-page. Maak pull-requests in de map van je buurman. Probeer deze repo over te nemen, doe wat je wilt.

-------------

### andere handige bronnen
Op internet zijn veel uitgebreidere en erg duidelijke guides geschreven over git.

|                                                   |
|---------------------------------------------------|
|https://guides.github.com/activities/hello-world/  |
|https://learngitbranching.js.org/                  |  
|https://try.github.io/                             |  
| https://git-scm.com/                              |
|http://kbroman.org/github_tutorial/                |
