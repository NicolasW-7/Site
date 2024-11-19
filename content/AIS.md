+++
date = "2024-11-18T11:19:15+01:00"
draft = false
title = "Administrateurs d'infrastructures sécurisées"
[cover]
    image = "/images/paysages.jpeg"
    alt = ""
    caption = "*The Wonderful Journey of secure infrastructures administrator !*"
+++

## Résumé
- Listes des tâches et du référentiel de formation.
- Apprentissages réalisé a [IMTNordEurope](https://imt-nord-europe.fr/)
- Toutes les documentations et procédures sont disponibles sur [**Procédures**](/Procedures/) ou sur [GITHUB](https://github.com/NicolasW-7/AIS-DevOPS/tree/main/AIS)


# Référentiels de formations

---

| **N° Fiche AT** | **Activités Types**                                                                            | **N° Fiche CP** | **Compétences Professionnelles**                                                      |
|-----------------|------------------------------------------------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------|
| 1               | Administrer et sécuriser les infrastructures                                                   | 1               | [Appliquer les bonnes pratiques dans l’administration des infrastructures](#1--appliquer-les-bonnes-pratiques-dans-ladministrations-des-infrastructures)              |
| -               | -                                                                                              | 2               | [Administrer et sécuriser les infrastructures réseaux](#2-administrer-et-sécuriser-les-infrastructures-réseaux)                                  |
| -               | -                                                                                              | 3               | [Administrer et sécuriser les infrastructures systèmes](#3-administrer-et-sécuriser-les-infrastructures-systèmes)                                 |
| -               | -                                                                                              | 4               | [Administrer et sécuriser les infrastructures virtualisées](#4-administrer-et-sécuriser-les-infrastructures-virtualisé)                             |
| 2               | Concevoir et mettre en œuvre une solution en réponse à un besoin d’évolution                    | 5               | [Concevoir une solution technique répondant à des besoins d’évolution de l'infrastructure](#5-concevoir-une-solution-technique-répondant-à-des-besoins-dévolution-de-linfrastructure---6-mettre-en-production-des-évolutions-de-linfrastructure) |
| -               | -                                                                                              | 6               | [Mettre en production des évolutions de l'infrastructure](#5-concevoir-une-solution-technique-répondant-à-des-besoins-dévolution-de-linfrastructure---6-mettre-en-production-des-évolutions-de-linfrastructure)                               |
| -               | -                                                                                              | 7               | [Mettre en œuvre et optimiser la supervision des infrastructures](#7-mettre-en-œuvre-et-optimiser-la-supervision-des-infrastructures)                       |
| 3               | Participer à la gestion de la cybersécurité                                                    | 8               | [Participer à la mesure et à l’analyse du niveau de sécurité de l’infrastructure](#8-participer-à-la-mesure-et-à-lanalyse-du-niveau-de-sécurité-de-linfrastructure)        |
| -               | -                                                                                              | 9               | [Participer à l’élaboration et à la mise en œuvre de la politique de sécurité](#9-participer-à-lélaboration-et-à-la-mise-en-œuvre-de-la-politique-de-sécurité)           |
| -               | -                                                                                              | 10              | [Participer à la détection et au traitement des incidents de sécurité](#10-participer-à-la-détection-et-au-traitement-des-incidents-de-sécurité)                   |

---

## Administrer et sécuriser les infrastructures

![Illustration](/images/Sauron.jpeg)

### 1 . Appliquer les bonnes pratiques dans l'administrations des infrastructures

**"** J'ai mis en place **des backup journaliers** pour garantir la protection des données essentielles de l'infrastructure. Ces sauvegardes sont effectuées automatiquement chaque jour afin de minimiser les risques de perte de données en cas de panne ou d'incident. En complément, j'ai déployé une solution de **réplication** sur deux sites distincts pour assurer la continuité de service en cas de défaillance d'un des sites. La réplication en temps réel ou à intervalles réguliers permet de dupliquer les données critiques sur un autre emplacement géographique, renforçant ainsi la résilience de l'infrastructure.

Pour cette solution, j'utilise une **machine virtuelle**, tout en ayant une **machine physique** dédiée pour stocker les sauvegardes et gérer les données sensibles de façon sécurisée. Cette architecture hybride entre machine virtuelle et machine physique permet de bénéficier de la *flexibilité* et de la *scalabilité* d'une solution virtuelle, tout en garantissant la *stabilité* et la *sécurité* d'une infrastructure physique.

En plus de ces stratégies, des **tests de restauration réguliers** sont effectués pour m'assurer que les données peuvent être récupérées rapidement et intégralement en cas de besoin.**"**

### 2. Administrer et sécuriser les infrastructures réseaux

**"** J'ai effectué l'**installation**, le **brassage** et le **déploiement** d'une salle de cours dans un **VLAN dédié**. Cette approche permet d'isoler le réseau de la salle de cours du reste de l'infrastructure, offrant ainsi une meilleure **gestion du trafic** réseau et une **sécurité renforcée**. Le brassage implique la connexion physique des équipements réseau (commutateurs, prises RJ45, câbles) à des racks de brassage. **"**

### 3. Administrer et sécuriser les infrastructures systèmes

**"** Mise en place d'une **politique de sécurité multifacteur (MFA)** sur un logiciels de gestions des mots de passes (vaulwarden) pour renforcer la porctections des comptes utilisateurs et l'accés aux données. **"**

### 4. Administrer et sécuriser les infrastructures virtualisé

**"** J'ai déployé une solution de **sauvegarde des VM avec Veeam**, assurant une protection complète grâce à des **sauvegardes automatisées** et **fiables**, tout en **optimisant** les temps de restauration grâce à la déduplication et aux sauvegardes incrémentielles. Cette solution garantit la **continuité de service** en cas de panne et permet une **récupération rapide** des *VM ou de leurs données*. **"**

[TOP⬆️](#référentiels-de-formations)

## Concevoir et mettre en oeuvre une solution en réponse à un besoin dévolution

![Illustration](/images/Elrond.jpeg)

### 5. Concevoir une solution technique répondant à des besoins d’évolution de l'infrastructure &  6. Mettre en production des évolutions de l’infrastructure 

**"** Dans le cadre de la conception d'une solution technique pour répondre à l'évolution de l'infrastructure et de la mise en production de ces évolutions, j'ai mis en place un trousseau de mots de passe **auto-hébergé** avec **Vaultwarden**. 

Cette solution **facilite la gestion** et **l'ajout de mots de passe** en permettant aux utilisateurs de stocker, organiser et récupérer leurs mots de passe de manière **centralisée** et **sécurisée**. Vaultwarden augmente la sécurité des comptes utilisateurs grâce à l'**intégration de l'authentification multifacteur (2FA)**, réduisant ainsi le risque de compromission des mots de passe. Ce trousseau remplace une ancienne solution moins sécurisée, tout en garantissant une meilleure gestion des accès aux ressources critiques.

 En centralisant tous les mots de passe dans une seule application, Vaultwarden permet de simplifier leur gestion tout en améliorant la conformité aux bonnes pratiques de sécurité. La solution a été mise en production après une phase de tests, garantissant une transition fluide et une adoption rapide par les utilisateurs. **"**

 Pour cette partie les procédures sont sur mon [GITHub](https://github.com/NicolasW-7/AIS-DevOPS/blob/main/AIS/Proc%C3%A9dure/Linux/Installation%20Procedure%20Vaultwarden%20on%20Docker%20%5BEN%5D.md)

 ### 7. Mettre en œuvre et optimiser la supervision des infrastructures

**"** J'ai travaillé sur l'optimisation du système de supervision via **What's Up Gold**, une solution de monitoring réseau et de gestion des performances. L'une des tâches principales a été de restructurer les métriques supervisées (pour le Partage*), ce qui a permis d'adapter les paramètres de suivi aux besoins spécifiques de l'infrastructure.

 Cette restructuration a **amélioré la visibilité sur l'état de santé des équipements réseau**, des serveurs et des applications critiques, facilitant ainsi l'identification rapide des anomalies ou défaillances.**"**

[TOP⬆️](#référentiels-de-formations)

## Participer à la gestion de la cybersécurité

![Illustration](/images/Oracle.jpeg)

### 8. Participer à la mesure et à l’analyse du niveau de sécurité de l’infrastructure

 **"** **Veille technologique** régulière, notamment sur des failles de sécurité critiques affectant des outils et équipements utilisés au sein de l'entreprise. Par exemple, j'ai suivi de près les **vulnérabilités** récemment découvertes dans **Outlook** et sur les bornes **Aruba Wifi**, permettant ainsi de prendre des mesures correctives rapidement. En parallèle, durant ma formation, j'ai acquis des compétences pratiques en **audit de sécurité**, notamment sur **Windows Server** et **Linux**, ce qui m'a permis de réaliser des analyses approfondies des configurations systèmes et de détecter d'éventuelles faiblesses dans les infrastructures. **"** 

### 9. Participer à l’élaboration et à la mise en œuvre de la politique de sécurité

 **"** L'élaboration et la mise en œuvre de la politique de sécurité est essentielle pour garantir la confidentialité, l'intégrité et la disponibilité des ressources. J'ai activement participé à la gestion des accès utilisateurs, en m'assurant que les politiques d'accès aux ressources étaient conformes aux principes du moindre privilège et aux normes de sécurité en vigueur. (en application sur les accées et le partage des collection Vaultwarden). Cela inclut la gestion des droits d'accès, la mise en place de contrôles d'authentification forte, ainsi que la revue régulière des comptes utilisateurs pour prévenir tout accès non autorisé. Ces actions ont permis de renforcer la sécurité en limitant l'exposition des données sensibles.**"** 

### 10. Participer à la détection et au traitement des incidents de sécurité

 **"** Travaille avec l'outil de monitoring **What's Up Gold** pour surveiller en temps réel l'état des infrastructures et identifier rapidement les anomalies ou incidents de sécurité. Ce travail a inclus la configuration et l'optimisation des alertes, ce qui a permis de réagir plus efficacement aux incidents détectés. Grâce à cet outil, il a été possible de suivre les performances des équipements, de détecter des comportements suspects et de lancer des actions correctives rapidement, réduisant ainsi le temps de réponse aux incidents de sécurité.**"** 

 [TOP⬆️](#référentiels-de-formations)