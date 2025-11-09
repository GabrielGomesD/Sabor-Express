Sabor Express
=============

Aplicativo web (Flask) para otimização de rotas de entrega com mapa e grafo.

Funcionalidades
---------------
- Restaurante como ponto inicial e final.
- CRUD básico de pontos (tabela editável + inclusão).
- Seleção de pontos que entram na rota.
- Otimização TSP (Vizinho Mais Próximo + 2-OPT).
- Distância total e tempo estimado.
- Mapa interativo (Folium) e grafo (Plotly).
- Download CSV da rota gerada.

Estrutura
---------
- `app/web.py` — servidor Flask (UI web).
- `app/core/geo.py` — Haversine e matriz de distâncias.
- `app/core/optimizer.py` — Heurísticas de rota (NN + 2-OPT).
- `app/core/data.py` — Leitura/gravação CSV e template.
- `app/ui/components.py` — Mapa Folium e grafo Plotly.
- `data/enderecos.csv` — CSV de exemplo.
- `requirements.txt` — dependências do projeto.

Como executar
-------------
1. Crie um ambiente virtual e instale as dependências:
   - `pip install -r requirements.txt`
2. Rode o servidor Flask:
   - `python app/web.py`
   - Acesse: `http://localhost:8000`
3. No navegador:
   - Preencha restaurante (nome/lat/lon) e velocidade.
   - Edite/cole o CSV de pontos na área de texto.
   - Clique em "Calcular melhor rota".
   - Veja resumo, tabela, mapa e grafo; baixe o CSV da rota.

Formato de CSV
--------------
Cabeçalho recomendado:

```
id,nome,endereco,latitude,longitude,selecionado
```

Sinônimos aceitos (case-insensitive): `endereço/endereco/address/rua`, `lat/latitude`, `lon/lng/longitude`, `selecionado/selected/ativo`.

Observações
-----------
- A velocidade média (km/h) no sidebar é usada apenas para estimar tempo; não altera a distância.
- O mapa usa Leaflet/Folium; o grafo é uma visão simplificada (arestas seguem a ordem da rota).
 - Caso encontre problemas de instalação com binários em Python muito recente, prefira Python 3.12.
