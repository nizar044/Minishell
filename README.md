#  Mini Shell – Projet Licence 3 Info (PSI 2024)

Ce projet est un mini interpréteur de commandes Unix/Linux développé en langage C dans le cadre d’un projet académique. Il permet d’exécuter des commandes système simples, avec support des commandes internes, des redirections, des pipelines et de la gestion de processus.

##  Structure du projet

```
shell-Moumad_Oubalkass/
├── src/                  # Fichiers source (.c, .h)
│   ├── main.c            # Point d'entrée du shell
│   ├── cmd.c / cmd.h     # Gestion des processus et exécution
│   ├── parser.c / parser.h  # Analyse des lignes de commandes
│   ├── builtin.c / builtin.h # Commandes internes (cd, exit...)
│   └── Untitled-1.c      # Gestion des redirections (en test)
├── doc/                  # Documentation et exemples d’utilisation
├── Makefile              # Compilation du projet
└── minishell             # (Optionnel) exécutable déjà compilé
```

##  Compilation

Dans le dossier `shell-Moumad_Oubalkass`, exécutez simplement :

```bash
make
```

Cela générera l’exécutable `minishell`.

##  Utilisation

Lancez le shell avec :

```bash
./minishell
```

Ensuite, tapez des commandes comme :

```bash
ls -l
cd ..
echo "Hello world"
cat fichier.txt > sortie.txt
cat fichier.txt >> log.txt
echo 'Erreur' >&2
cat fichier.txt | grep "mot" | wc -l
```

##  Fonctionnalités supportées

- Exécution de commandes classiques (`ls`, `cat`, etc.)
- Commandes internes : `cd`, `exit`, `help`, `export`, `unset`
- Redirections :
  - `>` : redirection de sortie
  - `>>` : redirection avec ajout
  - `>&2` : redirection vers la sortie d’erreur
- Pipelines (`|`) entre commandes
- Nettoyage des entrées (`trim`, `substenv`, etc.)


##  Licence

Projet réalisé à but pédagogique dans le cadre de la Licence 3 Informatique – PSI 2024.
