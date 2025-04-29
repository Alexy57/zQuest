# zQuest

**zQuest** est un système de quêtes entièrement personnalisable pour serveurs Minecraft utilisant Skript.

## 📦 Installation

1. Téléchargez le fichier `zQuest.sk`.
2. Placez-le dans le dossier suivant :  
   ```bash
   plugins/Skript/scripts/
   ```
3. En jeu, exécutez la commande :  
   ```bash
   /sk reload zQuest
   ```

> **Remarque** : Assurez-vous d’avoir installé le plugin [Skript](https://github.com/SkriptLang/Skript) et qu’il est fonctionnel.

---

## 🔧 Fonctionnalités

- Configuration **YAML** rapide et puissante
- Éditeur de quêtes **in-game via un GUI**
- Récompenses entièrement personnalisables (objets, XP, argent)
- Support des enchantements, lores, durabilité, etc.

---

## ⚙️ Configuration YAML

Le fichier de configuration YAML vous permet de créer rapidement des quêtes. Il peut être utilisé en complément du créateur de quêtes in-game.

### Exemple :
```yaml
quests: 
  test: 
    name: "test"
    icon: oak_sign
    rewards:
      items:
        diamond_pickaxe7653:
          type: diamond_pickaxe
          amount: 1
          enchantments:
            - fortune 2
            - unbreaking 8
            - efficiency 50
          durability: 1553
        spruce_log7060:
          type: spruce_log
          amount: 64
          durability: 0
        diamond_pickaxe1553:
          type: diamond_pickaxe
          amount: 1
          name: "&cTEST"
          durability: 1561
        diamond1911:
          type: diamond
          amount: 1
          name: "&6Diamant de test"
          lore:
            - "&7Ceci est un diamant de test"
            - "ligne 2"
            - "ligne 3"
          durability: 0
      money: 1000
      xp: 60
```

### Détails :
- `quests` : **Ne pas modifier** ce nom de section. Il est utilisé par le système pour détecter les quêtes.
- `test` : Identifiant unique de la quête. Ne doit pas être dupliqué.
- `name` : Nom affiché de la quête.
- `icon` : Item qui représentera la quête dans le GUI (ex: `oak_sign`).
- `rewards` : Récompenses obtenues à la fin de la quête :
  - `items` : Liste d'objets. Chaque objet a :
    - `type` : ID Minecraft de l'objet (ex: `diamond_pickaxe`)
    - `amount` : Quantité
    - `enchantments` : Liste d'enchantements, format `nom niveau` (ex: `efficiency 5`)  
      → [Liste des enchantements valides](https://www.digminecraft.com/lists/enchantment_list_pc.php)
    - `name` : Nom personnalisé (supporte les couleurs avec `&`)
    - `lore` : Description personnalisée en plusieurs lignes
    - `durability` : Valeur de durabilité
  - `money` : Argent gagné à la fin de la quête
  - `xp` : Points d'expérience reçus (pas des niveaux !)

---


## ❓ Support

Vous avez une question ou un bug à signaler ?  
Envoyez moi un message sur discord !
