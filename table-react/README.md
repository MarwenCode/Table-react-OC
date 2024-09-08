# Employee React Table

**Employee React Table** est un composant React conçu pour afficher et gérer une liste d'employés avec des fonctionnalités telles que la pagination, la recherche et le tri. Ce composant est facile à intégrer dans vos projets et personnalisable selon vos besoins.

---

## Table des Matières

- [Installation](#installation)
- [Utilisation](#utilisation)
  - [Exemple Basique](#exemple-basique)
- [Props](#props)
- [Fonctionnalités](#fonctionnalités)
- [Classes CSS](#classes-css)
- [Exemple Avancé](#exemple-avancé)
- [Développement Local](#développement-local)
- [Contribution](#contribution)
- [Licence](#licence)

---

## Installation

Installez le composant via npm :

```bash
npm install employee-table-react@latest
Note : Assurez-vous d'avoir Node.js et npm installés sur votre machine avant de procéder à l'installation.

npm install employee-react-table --save-dev


Utilisation
Exemple Basique
Voici un exemple basique d'utilisation du composant EmployeeTable avec des données fictives :

jsx
Copier le code
import React from 'react';
import EmployeeTable from 'employee-react-table';

// Données d'exemple représentant les employés
const employeeData = [
  {
    firstName: 'John',
    lastName: 'Doe',
    startDate: '2023-01-01',
    department: 'HR',
    dob: '1990-04-04',
    street: '123 Main St',
    city: 'New York',
    state: 'NY',
    zip: '10001'
  },
  {
    firstName: 'Jane',
    lastName: 'Smith',
    startDate: '2022-05-15',
    department: 'Finance',
    dob: '1988-07-12',
    street: '456 Elm St',
    city: 'Los Angeles',
    state: 'CA',
    zip: '90001'
  },
  // Ajoutez d'autres employés ici
];

function App() {
  return (
    <div className="App">
      <h1>Annuaire des Employés</h1>
      <EmployeeTable employeeList={employeeData} />
    </div>
  );
}

export default App;
Astuce : Vous pouvez personnaliser les données des employés en modifiant le tableau employeeData.

Props
Le composant accepte les props suivantes :

employeeList
Type : Array<Object>

Description : Tableau d'objets représentant les employés.

Structure attendue de chaque objet :

javascript
Copier le code
{
  firstName: string,    // Prénom de l'employé
  lastName: string,     // Nom de famille de l'employé
  startDate: string,    // Date de début au format 'YYYY-MM-DD'
  department: string,   // Département de l'employé
  dob: string,          // Date de naissance au format 'YYYY-MM-DD'
  street: string,       // Adresse (rue) de l'employé
  city: string,         // Ville de l'employé
  state: string,        // État de l'employé (ex: 'NY', 'CA')
  zip: string           // Code postal de l'employé
}
Remarque : Assurez-vous que chaque objet dans employeeList respecte cette structure pour un affichage correct.

Fonctionnalités
Tri des Colonnes : Cliquez sur les en-têtes de colonne pour trier les employés par ordre croissant ou décroissant.
Pagination : Affichez 10, 25, 50 ou 100 entrées par page.
Recherche : Filtrez les employés à travers plusieurs colonnes (prénom, nom, département, etc.).
Responsive Design : Le tableau s'adapte pour une utilisation sur différents types d'appareils (ordinateurs, tablettes, mobiles).
Classes CSS
Bien que le composant utilise styled-components, vous pouvez toujours surcharger certains styles via les classes CSS suivantes :

.table-wrapper : Conteneur principal du tableau.
.table-options : Conteneur pour les options comme la recherche et le nombre d'entrées à afficher.
.search : Conteneur pour la zone de recherche.
.table-header : En-têtes de colonnes pour le tri.
.table-cell : Cellules des lignes de données.
.pagination : Conteneur de la pagination.
.pagination-button : Boutons de pagination ("Previous", "Next").
.pagination-info : Informations sur la pagination (ex: "Page 1 of 5").
.sort-arrows : Contient les flèches de tri (ascendant/descendant).
.icon-sort : Style des icônes de tri (FaSortUp et FaSortDown).
Conseil : Pour personnaliser les styles, vous pouvez cibler ces classes dans votre fichier CSS principal ou dans des styles en ligne.

Exemple Avancé
Voici un exemple avec plus d'options personnalisées, y compris la pagination et la recherche :

jsx
Copier le code
import React from 'react';
import EmployeeTable from 'employee-react-table';

// Données d'exemple supplémentaires
const employeeData = [
  {
    firstName: 'Alice',
    lastName: 'Johnson',
    startDate: '2020-10-10',
    department: 'IT',
    dob: '1985-03-03',
    street: '789 Oak St',
    city: 'Boston',
    state: 'MA',
    zip: '02101'
  },
  {
    firstName: 'Bob',
    lastName: 'Williams',
    startDate: '2018-04-23',
    department: 'Marketing',
    dob: '1982-11-30',
    street: '101 Maple St',
    city: 'Seattle',
    state: 'WA',
    zip: '98101'
  },
  // Ajoutez d'autres employés ici
];

function MyApp() {
  return (
    <div>
      <h1>Répertoire des Employés</h1>
      <EmployeeTable employeeList={employeeData} />
    </div>
  );
}

export default MyApp;
Suggestion : Vous pouvez intégrer ce composant dans différentes parties de votre application pour afficher des listes d'employés selon vos besoins.

Développement Local
Si vous souhaitez contribuer ou travailler sur ce projet localement, suivez les étapes ci-dessous :



bash
Copier le code
cd employee-react-table
Installez les dépendances :

bash
Copier le code
npm install
Lancez l'application en mode développement :
