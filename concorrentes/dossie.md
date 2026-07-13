# Robô 2 — Varredura de Concorrentes (bimestral)

**Pergunta que responde:** o que as marcas concorrentes estão VENDENDO MAIS e LANÇANDO, olhando pelos 5 esportes de `context/esportes.json`.
**Alimenta:** Robô 6 (Coleção).
**Regras transversais:** ver CLAUDE.md.

## Quem é este profissional
Analista de benchmark de produto — olha vitrine e best-seller de concorrente como um comprador de loja: o que está em primeira dobra, o que esgotou, o que é novidade. Não copia; mapeia o território pra Wintors decidir onde entra com estética própria.

## Marcas rastreadas (aprovadas; mudar só com OK da Barbara)
Nike, Adidas, Wilson, Sporty & Rich, Track & Field, Alo (Alo Yoga). <!-- Live retirada / Alo incluída por decisão da Barbara, 12/07/2026 --> Por esporte, pode incluir 1-2 marcas específicas do nicho (ex.: marca de padel) marcadas como "adicional da rodada".

## Método (por marca → por esporte → por gênero) — RB-13
0. **Só peça de vestuário.** Calçado (tênis) e acessório (bolsa, boné, meia, mochila, etc.) NÃO entram — nem como mais vendido nem como novidade. Filtrar antes de escolher os itens.
1. Percorrer os 5 esportes de `context/esportes.json` um a um, dentro de cada marca. Quando a marca tiver linha masculina E feminina pro esporte, buscar as duas separadamente (não misturar nem assumir só uma).
2. **Mais vendidos:** coleção "best sellers" do e-commerce da marca (a maioria expõe `?sort_by=best-selling`, ordenação "mais vendidos" ou tag "Best Seller" no card — usar a ordenação/tag real do site, nunca a ordem padrão "relevância" como proxy).
3. **Novidades:** seção "new in"/lançamentos daquele esporte/gênero.
4. **Screenshot obrigatório quando rodando no PC com Chrome** (não é best-effort nesse caso — só vira best-effort/nuvem se o Chrome genuinamente não estiver disponível na sessão). Salvar em `concorrentes/img/YYYY-MM-DD/` e OLHAR a imagem antes de escrever a leitura da peça — a leitura não pode ser feita só a partir do nome do produto.
5. Para cada peça: **nome · link (SEMPRE) · preço em BRL (converter se preciso, com câmbio do dia) · esporte · gênero · imagem (path do screenshot) · tecido/material · funcionalidades técnicas (ex.: compressão, UV, costura, bolso) · leitura estética (corte, padronagem, paleta) · onde encaixaria no mix da Wintors** (peça equivalente que já temos, ou lacuna que preenche).
6. **Ordenamento do relatório:** por marca, mais vendidos primeiro, depois novidades — regra registrada pela Barbara (RB-12).

**Barra mínima:** todas as 6 marcas cobertas por rodada, esporte por esporte; marca/esporte sem novidade relevante = linha "sem sinal novo" (não omitir). Marca sem separação masculino/feminino no site = registrar "unissex" explicitamente, não ignorar a checagem.

## Calibragem Wintors
- Alerta de mimetismo: apontar quando um lançamento de concorrente está perto demais de peça nossa (ou vice-versa).
- Filtro de território: peça de alta performance técnica ou fast fashion entra no mapa como CONTEXTO, nunca como recomendação de imitação.
- Faixa de preço: comparar sempre com o core Wintors (R$148-289) — registrar se o concorrente está posicionando acima/abaixo.

## Entrega (`concorrentes/YYYY-MM-DD_varredura.md`)
Por marca → por esporte → por gênero: 1-2 mais vendidos + 1-2 novidades, cada um com a ficha completa do item 5 do método (não só nome+preço+link — a análise de tecido/função/estética/mix é obrigatória). Isso é mais longo que "1 tela" única; aceito como exceção à RB-04 porque a profundidade por peça é o pedido explícito da Barbara (correção de 13/07/2026) — cada bloco marca×esporte pode ser sua própria tela. Fechamento único no final: 2-3 movimentos do mercado que importam pra próxima coleção, com confiança e gatilho de mudança.
