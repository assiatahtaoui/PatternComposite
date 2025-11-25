Composite Design Pattern – Projet Java
📌 Description

Ce projet présente une implémentation simple du pattern Composite, un design pattern structurel qui permet de représenter une hiérarchie d’objets.
Il est utilisé ici pour modéliser un système de fichiers composé de dossiers (Folder) et de fichiers (File), manipulés de manière uniforme grâce au composant abstrait (Component).

📁 Structure du projet
src/
 └── composite/
      ├── Component.java       # Classe abstraite commune (Composant)
      ├── File.java            # Élément simple (Feuille)
      ├── Folder.java          # Élément composé (Composite)
      └── Test.java            # Classe de test / exécution

🧱 Fonctionnement du Pattern
🔹 Component (Composant abstrait)

(facultatif) Méthodes add() et print() selon le besoin
Les composants simples et composés partagent cette interface.

🔹 File (Feuille)

Représente un fichier individuel

Ne peut pas contenir d’autres éléments

Implémente print() pour afficher son nom

🔹 Folder (Composite)

Contient une collection de Component

Peut contenir des File et d’autres Folder

Gère la construction de l'arborescence

Exemple d’utilisation – Test.java

Voici le code exact que tu as fourni, présenté proprement :

public class Test {
    public static void main(String[] args) {

        Folder folder = new Folder("/");

        folder.addChild(new File("java"));
        folder.addChild(new File("xml"));

        Folder entities = (Folder) folder.addChild(new Folder("entitites"));

        folder.print();
    }
}
