<!-- Bannière dynamique -->
<p align="center">
  <img src="https://github.com/HexaNexus28/HexaNexus28/blob/main/!DOCTYPE%20html%20html%20lang%3Dfr%20head%20meta%20charset%3DUTF-8%20meta%20name%3Dviewport%20content%3Dwidth%3Ddevice-width%2C%20initial-scale%3D1.0%20titleBanni%C3%A8re%20LinkedIn%20-%20Yawo%20ZOGLOtitle%20script%20src%3Dhttpscdn.tailwindcss.comscri.png" alt="Yawo ZOGLO — Architecte de l'Invisible | Bricoleur de Logique" width="100%" />
</p>

---

## **Yawo ZOGLO**

**Paris, FR** | **Étudiant-Apprenti Développeur logiciel ESIEA** | <a href="https://yawo-portfolio.vercel.app" target="_blank">Portfolio</a> | <a href="https://www.linkedin.com/in/yawozoglo" target="_blank">LinkedIn</a>

---

## **Mon ADN Technique**

| **Écosystème** | **Outils & Philosophies** |
|----------------|---------------------------|
| **Architecture** | Architectures propres, Design Patterns, Algorithmes clairs et efficaces |
| **Technologies** | **C#** • **PHP** • **JavaScript/TypeScript** • **React** • **Node.js** • **MySQL/PostgreSQL** • **Electron** • **TailwindCSS** |
| **Méthodologies** | Automatisation • Optimisation • Débogage extrême • Scripts bash |
| **Philosophies** | Code résilient • UX invisible • "Moins mais mieux" • "Si c'est compliqué, c'est mal conçu" |

---

## **Projets Professionnels**

### **Skyndar - Écosystème de Gestion de Rendez-vous**
**Application bureau WPF + Site web PHP** - Synchronisation temps réel

Développement d'un écosystème synchronisé comprenant :
- Application bureau WPF pour administrateurs (gestion prestations, créneaux, suivi RDV)
- Site web public pour prise de rendez-vous en ligne (Visio ou présentiel)
- Synchronisation temps réel via MySQL
- Interface intuitive pour gestion complète du cycle de rendez-vous

**Stack** : C# • WPF • PHP • HTML5 • CSS • MySQL • Architecture Client-Serveur
**Statut** : Stable

<details><summary><b>Architecture Skyndar</b></summary>
  
```csharp
// Exemple gestion des créneaux WPF
public void GenererCreneaux(Prestation prestation, CalendarDay DayInWeek)
{
    DateTime Tdate = (DayInWeek != null) ? DayInWeek.Date : new DateTime(currentMonth.Year, currentMonth.Month, 1);
    int offset = ((int)Tdate.DayOfWeek - (int)DayOfWeek.Monday + 7) % 7;
    DateTime firstMonday = Tdate.AddDays(-offset);
    DateTime lastSunday = firstMonday.AddDays(6);
    ObservableCollection<Creneau> existingcreneaux = BDD.GetCreneauxForPrestation(prestation.Id, firstMonday,lastSunday);
    ObservableCollection<CalendarDay> existingdayweeks = BDD.GetDayInWeeks(DayInWeek.Date);
    DaysInWeeks.Clear();
    
    for (int j = 0; j < 7; j++)
    {
        DateTime jour = firstMonday.AddDays(j);
        CalendarDay jourInDB = existingdayweeks.FirstOrDefault(d => d.Date.Date == jour.Date);
        CalendarDay dayVM;

        if (jourInDB != null)
        {
            dayVM = jourInDB;
        }
        else
        {
            dayVM = new CalendarDay(0, jour, jour.Day, true);
            int newId = BDD.GetOrInsertId(dayVM);
            dayVM.Id = newId;
        }
        DaysInWeeks.Add(dayVM);
    }
}
```
</details>

### **Cookify - Plateforme Culinaire Interactive PHP/MySQL + Quiz Multijoueur Temps Réel**

Plateforme web dédiée à la cuisine et découverte culinaire :

- Gestion complète des recettes (CRUD, commentaires, favoris)
- Quiz multijoueur en temps réel via ngrok
- Dashboard personnel avec contenus favoris
- Interface responsive adaptée mobile/desktop
- Système de scoring et classement des joueurs

**Stack** : PHP 8.x • MySQL • JavaScript • HTML/CSS • ngrok • Git
**Statut** : Bêta privée

**Repo** : [Cookify](https://github.com/HexaNexus28/Cookify.git)

<details><summary><b>Exemple de quiz</b></summary>
  
Question: Quel ingrédient manque dans cette recette de carbonara ?

A) Crème fraîche
B) Lardons
C) Œufs (bonne réponse !)
D) Tomates

</details>
  
### **API de Micro-Transactions (ASPNET CORE API + REACT.VITE)**
Backend pour gérer les achats d'items dans les jeux.

- Gestion inventaire et transactions sécurisées

**Statut** : Stable

**Repo** : [Micro-Transactions](https://github.com/HexaNexus28/micro-transactions-app.git)

<details><summary><b>Structure de l'API</b></summary>
  
```csharp
// Exemple de route pour voir les items
public class ItemController : ControllerBase
{
    private readonly IItemService _itemService;

    public ItemController(IItemService itemService)
    {
        _itemService = itemService;
    }

    // GET: api/<ItemController>
    [HttpGet]
    public async Task<IActionResult> GetItems()
    {
        var result = await _itemService.GetAllItemsAsync();
        if (result.Success)
        {
            return Ok(result);
        }
        else return StatusCode(result.StatusCode, result);
    }
}
```
</details>

### **Journal Éducatif (PHP + MySQL + JS)**
Site éducatif interactif pour élèves et enseignants.

- Articles, livres, ressources pédagogiques
- Système de commentaires et likes

**Statut** : Actif

**URL** : <a href="https://www.journaleducatif.com" target="_blank">Journal Educatif</a>

<details><summary><b>Extrait de code PHP</b></summary>

```php
// Récupération des articles récents
$stmt = $pdo->query("SELECT * FROM articles ORDER BY date DESC LIMIT 5");
$articles = $stmt->fetchAll(PDO::FETCH_ASSOC);
```
</details>

### **My-Widget-App (React + Vite + Electron)**
Application desktop pour écouter YouTube.

- Lecture en arrière-plan, interface minimaliste

**Statut** : Stable

**Repo** : [Music Widget](https://github.com/HexaNexus28/music-widget.git)

<details><summary><b>Extrait code Electron</b></summary>
  
```javascript
// Création de la fenêtre principale
function createWindow() {
    mainWindow = new BrowserWindow({
        width: 800,
        height: 600,
        webPreferences: {
            nodeIntegration: true,
            contextIsolation: false,
        },
    });
    mainWindow.loadURL('https://youtube.com');
}
```
</details>

---

## **Statistiques GitHub**

<p align="center"> 
  <img src="https://github-readme-stats.vercel.app/api?username=HexaNexus28&show_icons=true&theme=radical&hide_border=true" width="48%" /> 
  <img src="https://streak-stats.demolab.com/?user=HexaNexus28&theme=radical&hide_border=true" width="50%" /> 
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=HexaNexus28&layout=compact&theme=radical&hide_border=true" width="48%" /> 
</p>

---

## **Philosophie de Développement**

- Le code raconte une histoire, pas seulement fonctionne
- La simplicité prime sur la complexité inutile
- L'apprentissage est plus important que le savoir
- L'échec est une opportunité d'amélioration
- La résilience est une compétence technique

---

## **Contact**

**Projets professionnels** : zoglopiere20@gmail.com  
**Collaborations** : [LinkedIn](https://www.linkedin.com/in/yawozoglo)  
**Développement** : GitHub

---

<p align="center"> 
  <i>"Le futur n'est pas une destination, c'est une direction. Et j'aime conduire vite — mais avec un bon GPS et une boîte à outils bien remplie."</i> 
</p>
