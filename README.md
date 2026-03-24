# LAB 4 - Manipulation Dynamique des Fragments avec FragmentManager et FragmentTransaction

## Description

Ce projet Android est un TP qui démontre l’utilisation des Fragments en Java avec Android Studio.  
L’application permet de naviguer entre deux fragments (FragmentOne et FragmentTwo) à partir d’une activité principale (MainActivity).

---

## Objectifs pédagogiques

- Comprendre le concept de Fragment
- Manipuler le FragmentManager
- Implémenter la navigation entre fragments
- Structurer une application Android avec Java et XML

---

## Structure du projet

```
tp4android-main/
│
├── app/
│   ├── src/main/
│   │   ├── java/com/example/lab4/
│   │   │   ├── MainActivity.java
│   │   │   ├── FragmentOne.java
│   │   │   └── FragmentTwo.java
│   │   │
│   │   ├── res/layout/
│   │   │   ├── activity_main.xml
│   │   │   ├── fragment_one.xml
│   │   │   └── fragment_two.xml
│   │   │
│   │   └── AndroidManifest.xml
│   │
│   └── build.gradle.kts
│
├── build.gradle.kts
└── settings.gradle.kts
```

---

## Fonctionnement

1. L’application démarre avec MainActivity  
2. Un fragment est affiché par défaut  
3. L’utilisateur peut naviguer entre FragmentOne et FragmentTwo  
4. Le changement se fait dynamiquement sans changer d’activité  

---

## Concepts utilisés

### Fragment
Un fragment représente une partie d’interface utilisateur réutilisable.

### FragmentManager
Permet de gérer les fragments (ajout, remplacement, suppression).

### Transaction de Fragment

```java
getSupportFragmentManager()
    .beginTransaction()
    .replace(R.id.fragment_container, new FragmentOne())
    .commit();
```

---

## Fichiers principaux

### MainActivity.java

Gère l’affichage des fragments et contrôle la navigation.

```java
public class MainActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        getSupportFragmentManager()
            .beginTransaction()
            .replace(R.id.fragment_container, new FragmentOne())
            .commit();
    }
}
```

---

### FragmentOne.java

```java
public class FragmentOne extends Fragment {
    public FragmentOne() {
        super(R.layout.fragment_one);
    }
}
```

---

### FragmentTwo.java

```java
public class FragmentTwo extends Fragment {
    public FragmentTwo() {
        super(R.layout.fragment_two);
    }
}
```

---

### activity_main.xml

```xml
<FrameLayout
    android:id="@+id/fragment_container"
    android:layout_width="match_parent"
    android:layout_height="match_parent"/>
```

---

## Exécution du projet

### Prérequis

- Android Studio
- SDK Android installé
- Java

### Étapes

1. Cloner le projet :

```bash
git clone https://github.com/votre-repo/tp4android.git
```

2. Ouvrir avec Android Studio

3. Lancer l'application :
   - Bouton Run
   - Ou Shift + F10

---

## Résultat attendu
<img width="718" height="1599" alt="image" src="https://github.com/user-attachments/assets/d7f26f5b-36ee-49a5-8b79-58861dccbd44" />
<img width="718" height="1599" alt="image" src="https://github.com/user-attachments/assets/81b437f0-513a-4009-8406-58da56843d01" />
<img width="718" height="1599" alt="image" src="https://github.com/user-attachments/assets/25ae6de8-92db-41ea-a5c6-b3651022252e" />
<img width="718" height="1599" alt="image" src="https://github.com/user-attachments/assets/386be15e-2c27-4ec1-b2a8-3d7accc9b6f2" />


---


## Auteur

- Nom : Ait Hmad Oussama 
---
