# Kokua — feeds públicos

Este repositório publica, uma vez por dia, os dados que a app Kokua lê:

- `feeds/overview.json`: resumo (cidades, contagens e fontes);
- `feeds/tiles/`: eventos por zona do mapa;
- `feeds/lookup/`: índice que diz em que zona está cada evento;
- `feeds/<PAÍS>.json`: todos os eventos de cada país;
- `privacidade.html` e `termos.html`: política de privacidade e termos de utilização.

Aqui não há código da app. O ficheiro `.github/workflows/feed.yml` vai buscar o agregador a um repositório privado, corre-o e publica o resultado no GitHub Pages.

## De onde vêm os eventos

De agendas culturais públicas e de APIs oficiais. Cada evento indica a fonte e liga para a página oficial. A lista das fontes de cada dia está em `feeds/overview.json`, no campo `sources`.

O agregador identifica-se como `KokuaBot` e faz um pedido de cada vez a cada site, com intervalo entre pedidos. Só são lidos endereços que o `robots.txt` de cada site permite; isso é conferido à mão quando uma fonte é acrescentada.

## É responsável por uma das fontes?

Se quiser que os seus eventos deixem de aparecer, ou tiver alguma correção, escreva para o contacto indicado na página deste repositório no GitHub Pages. Retiramos a fonte.
