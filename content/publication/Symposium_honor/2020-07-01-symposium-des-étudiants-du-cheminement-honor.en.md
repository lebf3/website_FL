---
title: L’apprentissage machine pour la prédiction de peptides immunogènes à partir de RNAseq de tumeur
author: Francis Leblanc
date: '2020-0-0'
slug: symposium-des-étudiants-du-cheminement-honor
categories: []
tags: [Deep learning, RNAseq, LSTM]
authors: [admin, J. Zumer, S. Lemieux]
doi: ''
publishDate: '2019-04-26T12:52:50-04:00'
publication_types:
  - '1'
publication: ''
publication_short: ''
abstract: 'Plusieurs stratégies sont présentement explorées afin de conditionner le système immunitaire à reconnaître les cellules tumorales. Cependant, la majorité de ces efforts concentrés sur l’exome, ne permettent pas d’induire une réponse immunologique puisque les peptides utilisés dérivent de gènes normaux surexprimés par les tumeurs qui sont reconnus comme antigène dû soit par les lymphocytes. Les recherches de Laumont et al. 2018 suggèrent que la majorité des tumor specific antigens (TSA) dérivent de régions non-codantes et de cadre de lecture alternatifs. L’identification de TSAs requières actuellement l’intégration de techniques de séquençage d’ADN, d’ARN et de spectrométrie de masse. Plusieurs approches d’apprentissage machine sont maintenant appliquées en biologie et pourraient permettre la découverte de nouveaux TSA, ainsi que d’amoindrir les ressources nécessaires au développement de vaccins contre le cancer. Nous posons donc l’hypothèse qu’un réseau de neurones peut être entraîné afin de faire la prédiction de TSA à partir de données RNAseq de patients. L’objectif initial de ce projet consiste entraîner un réseau de neurones à prédire de courtes séquences d’oligonucléotides afin d’évaluer s’il est possible d’absorbé la complexité du transcriptome. Un modèle dérivé de générateur de texte long short-term memory (LSTM) a été entraîné avec des oligonucléotides RNAseq du chromosome 18 afin de prédire les 10 derniers nucléotides de reads exclus de l’entraînement. Notre modèle LSTM à 2 couches bidirectionnelles de 1000 neurones et une couche linéaire permet actuellement d’atteindre une précision de 55%. Cette valeur est largement supérieure au hasard (précision > 25%), mais largement inférieure aux algorithmes du protocole actuel par table de K-mers. La capacité pourrait être limitante pour cette tâche. L’utilisation de modèles alternatifs tels Convolutional neural network ou Attention pourrait permettre d’augmenter la précision. Néanmoins, ces résultats préliminaires indiquent qu’il est possible d’entraîner un réseau de neurones sur cette tâche très complexe.'
summary: ''
featured: no
url_pdf: ~
url_code: ~
url_dataset: ~
url_poster: ~
url_project: ~
url_slides: ~
url_source: ~
url_video: ~
image:
  caption: ''
  focal_point: ''
  preview_only: no
projects: []
slides: ''
publication: In *Symposium des étudiants du cheminement honor*
links:
- name: Symposium des étudiants du cheminement honor
  url: https://biochimie.umontreal.ca/calendrier/symposium-des-etudiants-du-cheminement-honor/
---

