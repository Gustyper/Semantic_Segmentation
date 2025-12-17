# Segmentação Semântica em Cenas Urbanas (CamVid)

Este repositório contém o código desenvolvido para o "Programming Assignment 1" da disciplina de Deep Learning. O projeto foca na aplicação de redes neurais profundas para a tarefa de segmentação semântica, visando identificar classes de objetos (carros, peões, estrada, etc.) em imagens de vídeo de condução.

## Funcionalidades e Metodologia

1.  **Processamento de Dados:**
    * **Dataset:** CamVid (Cambridge-driving Labeled Video Database).
    * **Pré-processamento:** Normalização e redimensionamento de inputs e máscaras para $256 \times 256$ pixels.
    * **Data Augmentation:** Implementação de transformações geométricas (rotação limitada, espelhamento horizontal) utilizando a biblioteca *Albumentations* para melhorar a generalização do modelo.

2.  **Modelo de Deep Learning:**
    * **Arquitetura:** DeepLabV3 com backbone ResNet101 (`deeplabv3_resnet101`).
    * Utilização de pesos pré-treinados para acelerar a convergência (Transfer Learning).

3.  **Avaliação e Métricas:**
    * Cálculo de **IoU (Intersection over Union)** utilizando `MulticlassJaccardIndex`.
    * Funções auxiliares para visualização comparativa: Imagem Original vs. Máscara Real (Ground Truth) vs. Máscara Predita.
    * Análise de desempenho detalhada por classe.


* Guilherme Carvalho
* Luiz Felipe

**Orientação:**
* **Professor:** Dário Oliveira
* **Monitora:** Lívia Meinhardt
