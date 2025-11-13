# 🚚 Rota Inteligente: Otimização de Entregas Urbanas com IA

Projeto desenvolvido para demonstrar o uso de **Inteligência Artificial**, **K-Means** e **algoritmos de busca de rotas** (A* / heurísticas) para otimizar entregas urbanas em uma cidade grande, utilizando como exemplo o **centro de São Paulo** como estudo de caso para simular um cenário real.

---

## 🌟 Objetivo

O objetivo principal é gerar economia de custos e tempo operacional, propondo rotas mais curtas e eficientes para a frota de entregadores.

Redução de Custos: Menor distância percorrida implica menor consumo de combustível e manutenção.

Otimização do Tempo: Entregas mais rápidas, melhorando a satisfação do cliente.

Eficiência: O sistema agrupa pedidos por regiões (clustering) antes de calcular a rota otimizada.

---

## 🧠 O Pipeline: Como Funciona

O projeto segue um fluxo de trabalho em duas etapas de otimização:

Clustering Geográfico: O algoritmo K-Means processa as coordenadas dos pedidos e os agrupa em clusters regionais. Cada cluster representa uma micro-região a ser atendida por um único entregador.

Roteamento Otimizado: Dentro de cada cluster (com um número gerenciável de pontos), aplicamos um algoritmo de busca heurística (TSP) para determinar a sequência de paradas que resulta na distância total mais curta.

---

## 🚀 Tecnologias Utilizadas

Categoria	Tecnologia	Uso Principal
Linguagem	Python 3.10+	Scripting e lógica principal.
IA/Clustering	scikit-learn	Implementação do K-Means (cluster_utils.py).
Análise de Dados	pandas, numpy	Manipulação e preparação do dataset de pedidos.
Grafos	networkx	Modelagem da rede de pontos para cálculo de rotas.

---

## 🗂️ Estrutura do Projeto

Em desenvolvimento

---

## 👥 Autor
Gabriel Dino Gomes

Curso: Engenharia da Computação – UniFECAF (2025)
Disciplina: Artificial Intelligence Fundamentals
