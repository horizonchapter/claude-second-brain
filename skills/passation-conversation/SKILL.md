---
name: passation-conversation
description: Condense une conversation longue en un bloc autonome à coller dans un nouveau chat, pour continuer sans perte de contexte et économiser des tokens. À utiliser quand l'utilisateur dit « passation », « nouveau chat » ou « context transfer ».
---

# Passation de conversation

Objectif : produire un bloc unique qui permet à un nouveau chat de reprendre exactement où on en est, sans relire l'historique.

## Règles
- Le bloc doit être autonome : un lecteur qui n'a rien vu doit tout comprendre.
- Garde à l'identique : chiffres, noms, liens, chemins de fichiers, identifiants, décisions datées, formulations validées par l'utilisateur.
- Ne garde pas : tentatives abandonnées (sauf la raison de l'abandon si elle évite de recommencer), politesses, explications déjà comprises.
- Distingue ce que l'utilisateur a décidé de ce que tu as seulement proposé.
- Conserve les étiquettes VÉRIFIÉ / ESTIMÉ / HYPOTHÈSE / INCONNU.
- Aucune information sensible (mots de passe, clés, numéros de carte).
- Le plus court possible sans perte : en général 300 à 900 mots.

## Format du bloc (dans un seul bloc de code)

```
# PASSATION : [projet] : [date]

## 1. Objectif
## 2. Décisions prises (et pourquoi)
## 3. État : terminé / en cours (où exactement) / pas commencé
## 4. Fichiers, liens, chiffres et détails critiques
## 5. Contexte utile : contraintes, préférences, pièges rencontrés, idées écartées
## 6. Point d'arrêt et prochaines étapes : dernière action, prochaine action, questions ouvertes

## Consigne pour le nouveau chat
Lis cette passation, résume-la en 3 lignes pour confirmer, puis reprends à « Prochaine action ». Ne refais pas ce qui est terminé.
```

Après le bloc : rappelle d'ouvrir un nouveau chat (dans le même projet si possible), de coller le bloc et de rejoindre les fichiers cités.
