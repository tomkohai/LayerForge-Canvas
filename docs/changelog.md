



## V0.1 — Système de base (prototype initial)
Création du système de matériaux LF

Première version du système de calques

Ajout des nodes de base (Layer, NBAdd, Master)

Gestion initiale des images internes (TEX_IMAGE)

Première version du canvas 2D dans Blender

Début du mode peinture (Texture Paint + LF routing)


## V0.2 — Add / Remove / Reorder (fondations du layer stack)

Ajout du bouton Add Layer

Suppression de layer avec nettoyage des nodes

Reorder complet du stack

Renumérotation automatique des layers et NBAdd

Correction des index LF (lf_index)

Mise à jour automatique du merge map

Stabilisation du système UID pour chaque layer


## V0.3 — Duplicate & système d’images internes

Ajout du Duplicate Layer

Gestion du buffer CPU/GPU pour les images peintes

Correction du comportement de copy TEX_IMAGE

Anti‑halo straight (première version)

Correction douce (première version)

Introduction du flag lf_is_processed

Stabilisation du duplicate pour éviter les halos gris


## V0.4 — Merge (première version)

Merge des layers checked

Composite NumPy (NORMAL, MULTIPLY, SCREEN, OVERLAY)

Gestion des opacités par layer

Création automatique d’une image fusionnée

Suppression automatique des layers mergés

Mise à jour du merge map après suppression

Sélection automatique du layer de base


## V0.5 — Refactor du système de calques et ajout d'un pipelin normal map 

Refactor complet du système Layer/NBAdd

Refonte de get_real_layer_nbadd_chain

Stabilisation des piles dynamiques

Correction des décalages UID/index

Nettoyage des labels visuels (safe)

Mise à jour du canvas après chaque opération

Correction des problèmes de synchro GPU→CPU

Pipeline de nodes normal map handpaint

Création atttribution et changement de mode render 


## V0.6 — Mode Canvas 2D et line art cam view 

Ajout du mode Canvas 2D

Vue caméra dédiée au dessin

Panel de transformation objet (scale/rotate/move)

Outils de cadrage pour la peinture 2D

Stabilisation du viewport pour le dessin

Correction du comportement du canvas dans Texture Paint


## V0.7 — Outline & Line Art Auto

Ajout du système d’Outline auto

Line Art automatique basé sur la géométrie

Ajustement automatique de l’épaisseur

Correction du comportement en mode 2D

Intégration dans le stack LF


## V0.8 — Merge straight stabilisé (pipeline final)

Passage complet du pipeline en straight

Suppression totale du premul interne

Anti‑halo straight stabilisé

Correction douce conditionnelle (flag lf_is_processed)

Merge sans halo blanc

Merge sans halo gris

Falloff intact

Couleurs non mélangées

Pipeline final stable


## V0.9 — UI & Panels

Panel de gestion des layers

Panel de merge

Panel de transform

Panel de caméra 2D

Nettoyage de l’UI

Réorganisation des menus

Ajout des warnings (merge popup)


## V1.0 — Version finale (release)

Pipeline straight finalisé

Duplicate stabilisé

Merge stabilisé

Système de calques complet (Add, Remove, Reorder, Duplicate, Merge)

Canvas 2D opérationnel

Outline & Line Art auto

UI complète

Première peinture showcase

Animation de draw rendue

Pages Gumroad / itch.io prêtes

Site prêt

Addon prêt pour publication
