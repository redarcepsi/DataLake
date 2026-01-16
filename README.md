# Atelier Big Data & Data Lake

## Introduction

Ce projet vise à concevoir, implémenter et exploiter un Data Lake professionnel à partir de données hétérogènes issues de différentes sources métier. L'objectif est de centraliser les données de transactions, de ventes et de sécurité afin d'améliorer la détection de fraude et l'analyse décisionnelle.

## Architecture du Data Lake

Le Data Lake est structuré en trois zones principales :

- **Raw** : données brutes telles que reçues.
- **Staging** : données nettoyées, typées et enrichies.
- **Curated** : données prêtes pour usage métier, BI ou Data Science.

## Sources de données

Les données proviennent de plusieurs sources :

- Transactions bancaires & fraude (CSV + JSON – Kaggle)
- Ventes européennes par pays (CSV – Kaggle)
- Logs d'authentification RBA (CSV – Kaggle)

## Phases du projet

### Phase 1 – Ingestion & Exploration (Zone RAW)

Les données doivent être déposées sans modification dans la zone raw. Charger chaque source avec Spark et analyser les schémas, la volumétrie et la qualité des données.

### Phase 2 – Nettoyage & Structuration (Zone STAGING)

Typage des données, suppression des doublons, harmonisation des pays et sauvegarde en Parquet.

### Phase 3 – Enrichissement & Indicateurs (Zone CURATED)

Jointures multi-sources, création d'indicateurs métier et scores simples de risque.

## Livrables attendus

- Dossier `data_lake` structuré
- Scripts Spark commentés
- Datasets Parquet en staging et curated
- README détaillant architecture et choix techniques

## Critères d'évaluation

- Qualité de l'architecture Data Lake
- Rigueur du nettoyage et des transformations
- Pertinence des indicateurs métiers
- Clarté et professionnalisme de la restitution

## Stack technique

- **Langage** : Java 17
- **Framework Big Data** : Apache Spark
- **Format de stockage** : Parquet
- **Outils de gestion de données** : Apache Hadoop, Apache Hive (si applicable)
- **Autres bibliothèques** : (à préciser selon le contenu du repository)

## Architecture
DataLake/
├── config/
├── data/ 
├────── curated/
├────── raw/
├────────── logs/
├────────── sales/
├────────── transactions/
├────── stagging/
├── notebooks/
├── src/
├── requirements.txt
└── README.md

## Installation et configuration

1. Cloner le repository :
   ```bash
   git clone https://github.com/redarcepsi/DataLake.git
