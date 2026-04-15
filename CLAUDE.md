# STRATE App - regles

1. Lire ce fichier avant toute modification.
2. Toute modification passe par un plan (meme un fix court).
3. Lire le fichier entier avant toute edition.
4. Interdits : `sed -i`, `git add .`, `git add -A`, `git reset --hard`, secrets en clair, modification de `.env`.
5. Chaque changement doit produire des preuves : tests, smoke, logs ou citations.
6. Ne jamais dire "termine" sans preuves verifiees.
7. Pour le design interface : lire `BRIEFING-INTERFACE.md` avant de toucher aux HTML.

## Memoire Structurelle

Avant toute exploration large du repo, consulter Graphify si disponible pour :
- identifier les noeuds centraux
- reperer les dependances entre modules
- reduire la relecture inutile

Graphify sert a comprendre la structure technique actuelle du code.
Obsidian sert a conserver les decisions, invariants, risques et contexte durable.

Regles :
- ne pas recopier le code dans Obsidian
- n'ecrire dans Obsidian que ce qui doit survivre a la session
- mettre a jour Obsidian apres toute decision qui changerait le comportement d'un autre contributeur (humain ou agent)
- si un doute apparait dans Obsidian sur un fait technique, revalider avec Graphify ou le code avant d'agir

Rafraichir Graphify quand :
- un changement structurel majeur a eu lieu
- un module important a ete ajoute/supprime
- plus de 20% des fichiers du repo ont change depuis le dernier graphe
- l'architecture reelle semble avoir diverge du graphe courant

Rituel :
- debut de grosse session : Graphify
- pendant la session : code
- fin de session : Obsidian
- en cas de doute technique depuis Obsidian : retour Graphify/code
