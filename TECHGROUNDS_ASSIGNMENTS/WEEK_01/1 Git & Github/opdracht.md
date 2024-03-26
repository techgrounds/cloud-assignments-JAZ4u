# [1- Git & Github]

GitHub is a web-based platform used for version control using Git. It provides hosting for software development projects, allowing developers to collaborate on code, track changes, and manage projects effectively. GitHub offers features like issue tracking, pull requests, code review, and wikis, making it a popular choice for open-source as well as private projects.

## Key-terms

## Opdracht

Bestudeer:
Gedistribueerde en gecentraliseerde versiebeheer
Begrijp de volgende termen:
Repository
Main / Master
Branch
Commit
Push / Pull
Merge
Fork

Opdracht 1:

- Maak een GitHub account als je er nog geen hebt.
- Maak een repository op je GitHub account. Deze repository gebruik je alleen om te testen. Je mag hem na de opdracht weer verwijderen.
- Geef permissies aan je teamgenoten om de repository te gebruiken.
- Push code naar je repository. Het maakt niet uit wat voor code het is. Let op: je mag de 'upload file'-optie op de Github website niet gebruiken. 
- Pull / Clone een repository van je peer.
- Tip: In Slack vind je een link naar de officiële Git & Github Fundamentals Classroom

Opdracht 2:

- Maak een nieuwe repository aan voor je portfolio via de GitHub Classroom-link in Slack.
- Beschrijf voor jezelf hoe je je repository gaat inrichten op een manier zodat het voor iedereen (jezelf en buitenstaanders) duidelijk is wat de structuur is.

### Gebruikte bronnen

- CHAT GPT

### Ervaren problemen

Ik kende Github totaal niet , de GITHUB windows app begreep ik na wat trial en error. 

### Resultaat

 Bestudeer:

- Gedistribueerde en gecentraliseerde versiebeheer
  
  Versiebeheer, een essentieel onderdeel van softwareontwikkeling, kan worden onderverdeeld in gedistribueerd versiebeheer en gecentraliseerd versiebeheer. Hieronder worden beide benaderingen beschreven:
  
  1. **Gedistribueerd versiebeheer (DVCS - Distributed Version Control System)**:
     
     - Bij gedistribueerd versiebeheer heeft elke ontwikkelaar een volledige kopie van het hele versiebeheersysteem inclusief de complete geschiedenis van het project.
     - Belangrijke voorbeelden van gedistribueerde versiebeheersystemen zijn Git, Mercurial en Bazaar.
     - Voordelen:
       - Betere prestaties bij offline werken: Ontwikkelaars kunnen volledige repositories lokaal hebben en hun werk voortzetten zonder een continue internetverbinding.
       - Flexibiliteit in samenwerking: Ontwikkelaars kunnen verschillende branches maken en samenvoegen zonder afhankelijk te zijn van een centrale server.
       - Betere veiligheid: Omdat er geen enkel punt van uitval is, is het minder waarschijnlijk dat het hele systeem faalt.
     - Nadelen:
       - Kan complexer zijn om te begrijpen en te beheren, vooral voor beginners.
       - Het beheer van de samenvoeging (merge) kan soms ingewikkelder zijn dan bij een gecentraliseerd systeem.
  
  2. **Gecentraliseerd versiebeheer (CVCS - Centralized Version Control System)**:
     
     - Bij gecentraliseerd versiebeheer is er een centrale server die de enige bron van waarheid is. Ontwikkelaars halen hun kopieën van de codebase op en werken er lokaal aan, maar ze moeten wijzigingen naar de centrale server pushen en daarvan pullen.
     - Voorbeelden van gecentraliseerde versiebeheersystemen zijn Subversion (SVN) en Perforce.
     - Voordelen:
       - Eenvoudigere workflow: Aangezien er één centrale autoriteit is, is het beheer van wijzigingen eenvoudiger.
       - Mogelijkheid tot meer controle: Administrators kunnen striktere toegangscontroles opleggen.
     - Nadelen:
       - Afhankelijkheid van een centrale server: Als de centrale server uitvalt, kan niemand nieuwe wijzigingen pushen of pullen.
       - Minder geschikt voor offline werken: Ontwikkelaars moeten altijd verbonden zijn met de centrale server om te werken.
  
  Elk type heeft zijn eigen voor- en nadelen, en de keuze tussen gedistribueerd en gecentraliseerd versiebeheer hangt vaak af van de specifieke behoeften en voorkeuren van het ontwikkelteam.

- Begrijp de volgende termen:
  
  - Repository
    Projects on GitHub are stored in repositories, which can contain folders, files, images, videos, spreadsheets, and data sets - anything your project needs.  
  
  - Main / Master
    In GitHub, "main" or "master" refers to the default branch of a repository. Historically, GitHub used the term "master" as the default branch name, but in response to ongoing discussions about diversity and inclusion in the tech industry, GitHub decided to rename the default branch from "master" to "main" in October 2020.

This change was made to remove potentially offensive or exclusionary language from the platform's default settings. The term "main" is now commonly used as the default branch name across many version control systems and platforms, including GitHub.

The default branch typically serves as the primary development branch where the latest changes and updates are merged. It's the branch that is checked out by default when someone clones the repository or navigates to it on GitHub. However, users can still create and work with branches with different names depending on their workflow and project requirements.

- Branch
  In GitHub, a branch is a parallel version of a repository's codebase. It allows developers to work on different features, fixes, or experiments without affecting the main codebase. Branches are essential for collaborative development workflows and are commonly used in conjunction with pull requests for code review and integration.

- Commit
  In GitHub, a commit represents a specific change or set of changes made to a repository's codebase. Each commit captures a snapshot of the repository at a particular point in time, including the modifications made to files.

- Push / Pull
  In Git and GitHub, "push" and "pull" are fundamental commands used to synchronize changes between your local repository and a remote repository, such as the one hosted on GitHub. Here's an overview of each:

Push: The git push command is used to upload local repository commits to a remote repository. When you've made changes to your local repository and want to share them with others or update the remote repository, you use git push. Typically, you specify the remote repository and the branch you want to push to, like git push origin master (to push your local master branch to the origin remote repository).

Example:
`git push origin master`

Pull: The git pull command is used to fetch and integrate changes from a remote repository into your local repository. It's essentially a combination of git fetch (which downloads changes from the remote repository) followed by git merge (which integrates those changes into your local branch). git pull is used when you want to update your local repository with changes made by others on the remote repository.

Example:
`git pull origin master`
This command fetches changes from the master branch of the origin remote repository and merges them into your current local branch

- Merge
  
  In the context of GitHub and version control systems in general, "merge" refers to the process of combining changes from one branch (often called the "source" branch) into another branch (often called the "target" branch). This is typically done when developers have been working on separate branches with different features or fixes and need to incorporate their changes into a common branch, such as the main development branch.

- Fork
  
  In the context of GitHub and version control systems in general, "merge" refers to the process of combining changes from one branch (often called the "source" branch) into another branch (often called the "target" branch). This is typically done when developers have been working on separate branches with different features or fixes and need to incorporate their changes into a common branch, such as the main development branch.

Opdracht 1:

- Maak een GitHub account als je er nog geen hebt.
  
  - <mark>[LINK naar persoonlijke JAZ4u GITHUB] [JAZ4u · GitHub](https://github.com/JAZ4u)</mark>
  
  - <mark>[LINK naar TechGrounds CloudAssignments] JAZ4u GITHUB] [JAZ4u TechGrounds Cloudassignments/cloud-assignments-JAZ4u) · GitHub](https://github.com/techgrounds/cloud-assignments-JAZ4u)</mark>

- Maak een repository op je GitHub account. Deze repository gebruik je alleen om te testen. Je mag hem na de opdracht weer verwijderen.

- Geef permissies aan je teamgenoten om de repository te gebruiken.

- Push code naar je repository. Het maakt niet uit wat voor code het is. Let op: je mag de 'upload file'-optie op de Github website niet gebruiken. 

- Pull / Clone een repository van je peer.

- Tip: In Slack vind je een link naar de officiële Git & Github Fundamentals Classroom

 Opdracht 2:

- Maak een nieuwe repository aan voor je portfolio via de GitHub Classroom-link in Slack.
  https://github.com/techgrounds/cloud-assignments-JAZ4u

- Beschrijf voor jezelf hoe je je repository gaat inrichten op een manier zodat het voor iedereen (jezelf en buitenstaanders) duidelijk is wat de structuur is.
  
  ****************
  
  Het opzetten van een goed gestructureerde repository is essentieel voor het begrijpen en onderhouden van een project, zowel voor jezelf als voor buitenstaanders. Hier zijn enkele stappen om een duidelijke structuur te creëren:
  ​
1. **Leesbare documentatie toevoegen**:
   Begin met het toevoegen van een README-bestand in de hoofdmap van je repository. Dit README-bestand moet een overzicht geven van het project, de doelstellingen, instructies voor installatie en gebruik, en eventuele bijzonderheden over de structuur van de repository.
   ​

2. **Mapstructuur definiëren**:
   Bedenk een logische mapstructuur die de verschillende componenten van je project organiseert. Bijvoorbeeld:
   ​
   
   - `src/`: voor broncodebestanden.
   - `docs/`: voor documentatiebestanden.
   - `tests/`: voor testbestanden.
   - `assets/`: voor afbeeldingen, video's, of andere niet-codebestanden.
   - `scripts/`: voor hulpprogramma's of scripts die worden gebruikt bij het bouwen, testen of implementeren van het project.
     ​

3. **Naamgeving van bestanden en mappen**:
   Gebruik consistente en beschrijvende namen voor mappen en bestanden. Vermijd het gebruik van spaties en speciale tekens in namen, omdat dit problemen kan veroorzaken op verschillende besturingssystemen.
   ​

4. **Gebruik van Git-ignore-bestanden**:
   Voeg een `.gitignore`-bestand toe om bestanden en mappen te negeren die niet moeten worden opgenomen in de versiebeheerhistorie, zoals tijdelijke bestanden, gegenereerde bestanden en afhankelijkheden.
   ​

5. **Documentatie binnen de code**:
   Voeg commentaar toe aan je code om de functionaliteit en het doel van verschillende delen van de code uit te leggen. Dit maakt het gemakkelijker voor anderen (en jezelf in de toekomst) om de code te begrijpen en aan te passen.
   ​

6. **Gebruik van branches**:
   Maak gebruik van Git-branches om nieuwe functies te ontwikkelen of bugs op te lossen zonder de hoofdtak van het project te verstoren. Zorg ervoor dat de branchnaam betekenisvol is en duidelijk aangeeft welke functie of bug wordt aangepakt.
   ​

7. **Issue tracking**:
   Maak gebruik van de issue tracker van het versiebeheersysteem (bijv. GitHub Issues) om taken, bugs en andere problemen bij te houden. Wijs taken toe aan teamleden, wijs prioriteiten toe en houd de voortgang van het project bij.
   ​

8. **Code review**:
   Stel een proces op voor het beoordelen van code voordat deze wordt samengevoegd in de hoofdtak van het project. Dit helpt bij het identificeren van fouten, het delen van kennis en het handhaven van codekwaliteit.
   ​
   Door deze richtlijnen te volgen, kun je een goed gestructureerde repository creëren die gemakkelijk te begrijpen en te onderhouden is voor zowel jou als anderen die aan het project werken.
   
   *************
