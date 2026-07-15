# Varredura de Concorrentes — 13/07/2026 (v2, método RB-14)

**Cobertura desta rodada: Nike → Corrida (masculino + feminino) apenas.** Método RB-14 aplicado pela primeira vez na íntegra (esporte > gênero > 3 mais vendidos + 3 novidades > ficha completa > cruzamento). Dado o volume real por peça, não deu pra cobrir as 6 marcas nem os 5 esportes numa sessão só — ritmo autorizado pela Barbara é 2 marcas/dia. Este arquivo é o "dia 1" da rodada bimestral; Raquete, Musculação, Hyrox e Pilates da Nike + as outras 5 marcas ficam para as próximas sessões, registrado como pendência (não como "sem sinal"). A 1ª tentativa (sem esse método) está preservada em `2026-07-13_varredura_v1-falha.md` como histórico, não usar como baseline.

**Imagem: resolvido.** O `save_to_disk` do screenshot do Chrome não expõe caminho de arquivo neste ambiente — mas cada página de produto Nike carrega a foto oficial num CDN público (`imgnike-a.akamaihd.net/1920x1920/{código}.jpg`, extraído do próprio HTML da página). Baixei a foto real do produto (1920×1920, sem menu/navbar) pra cada uma das 11 peças, salva em `concorrentes/img/2026-07-13/nike/`. Método documentado no dossiê pra repetir nas próximas marcas.

**Ordenação "mais vendidos":** a Nike Brasil **não expõe ordenação por mais vendidos dentro de categoria/esporte** (dropdown "Ordenar por" só tem Relevância, Lançamentos, Maior desconto, Menor/Maior preço). Existe um carrossel "Mais Vendidos" nas páginas de produto, mas é site-wide (chinelo, mochila, boné, camiseta Park genérica) — não filtrado por esporte, então não serve como proxy. Os "3 mais vendidos" abaixo usam a ordenação padrão Relevância (algoritmo da própria Nike, que pondera popularidade), registrado explicitamente como aproximação, não como dado de vendas real.

---

## Nike — Corrida

### Masculino

**Mais vendidos (Relevância — sem ordenação por vendas real, ver nota acima)**

1. **Camiseta Dri-FIT Nike Run Swoosh Masculina** — [link](https://www.nike.com.br/camiseta-dri-fit-nike-run-swoosh-masculina-063036.html?cor=IG) · [foto](img/2026-07-13/nike/masc_01_camiseta-run-swoosh.jpg) — R$149,99 (R$123,49 Pix) — 4.6★ (25 avaliações)
   Top. Preta, gráfico "RUN" com swoosh em verde-petróleo no peito e reprisado nas costas, corte clássico/solto (não colado ao corpo). Tecido misto 52-57% algodão / 43-48% poliéster — mais "camiseta de algodão com Dri-FIT" do que peça 100% técnica, visual mais casual-esportivo. Só aparece na categoria Corrida.
   **Mix Wintors:** é o tipo de peça mais próxima do nosso território — camiseta gráfica com tecido misto, dá pra imaginar uso fora do treino. Preço (R$149,99) cai dentro do nosso core.

2. **Camiseta Dri-FIT Nike UV Miler Masculina** — [link](https://www.nike.com.br/camiseta-dri-fit-nike-uv-miler-masculina-097985.html?cor=ID) · [foto](img/2026-07-13/nike/masc_02_camiseta-uv-miler.jpg) — R$149,99 (R$123,49 Pix) — 5.0★ (2)
   Top. Preta lisa, sem gráfico grande, barras refletivas na barra, corte solto/relaxed. 100% poliéster com proteção UV — peça 100% técnica, sem ambição estética além do funcional.
   **Sinal:** essa peça aparece tanto no "mais vendidos" (relevância) quanto no topo dos lançamentos — não é aposta experimental, é peça consolidada que a Nike continua girando.
   **Mix Wintors:** fora do nosso território — puramente técnica, sem dupla vida.

3. **Regata Dri-FIT Nike Miler Masculina** — [link](https://www.nike.com.br/regata-dri-fit-nike-miler-masculina-098054.html?cor=ID) · [foto](img/2026-07-13/nike/masc_03_regata-miler.jpg) — R$149,99 (R$142,49 Pix) — 5.0★ (3)
   Top. Preta lisa, sem gráfico, barras refletivas, aberturas laterais na bainha. 100% poliéster.
   **Mix Wintors:** técnica pura, fora do território de clube.

**Novidades**

4. **Shorts Dri-FIT Nike Miler Masculino** — [link](https://www.nike.com.br/shorts-dri-fit-nike-miler-masculino-097968.html?cor=16) · [foto](img/2026-07-13/nike/masc_04_shorts-miler.jpg) — R$249,99 (R$237,49 Pix) — sem avaliações
   Bottom. Verde vivo, tecido woven com forro 92% poliéster/8% elastano, cueca interna com sustentação, bolso traseiro com fecho + bolsos laterais.
   **Mix Wintors:** cor viva e tecnologia de camada dupla — fora do nosso padrão de paleta (verde profundo, não verde neon), mas é sinal de que "short técnico com forro" é o padrão de mercado em corrida.

5. **Camiseta Nike Aeroswift Running Masculina** — [link](https://www.nike.com.br/camiseta-nike-aeroswift-running-masculina-106983.html?cor=NX) · [foto](img/2026-07-13/nike/masc_05_camiseta-aeroswift.jpg) — R$149,99 (R$123,49 Pix) — sem avaliações, "últimas unidades"
   Top. Verde-água pastel, gráfico grande estilizado "N/A" no peito + tipografia vertical "NIKE ELIMINATING" nas costas — visual de statement gráfico, mais "hype" que os outros itens masculinos. 57% algodão / 43% poliéster.
   **Mix Wintors:** é a peça masculina mais "moda" da leva — mostra que a Nike também testa gráfico ousado em corrida, não só o básico técnico.

### Feminino

**Mais vendidos (Relevância)**

1. **Shorts Nike One Swoosh Feminino** — [link](https://www.nike.com.br/shorts-nike-one-swoosh-feminino-059090.html?cor=ID) · [foto](img/2026-07-13/nike/fem_01_shorts-one-swoosh.jpg) — R$299,99 (R$180,49 Pix, 40% off) — sem avaliações
   Bottom. Preto, caimento solto, swoosh branco grande estampado na coxa esquerda (peça-logo, não peça-tecnologia). Woven 100% poliéster.
   **Mix Wintors:** o oposto do nosso approach — aposta no logo grande como estética, não na sobriedade. Alerta de território: se cogitarmos short com aplicação de marca grande, isso já é linguagem Nike, não nossa.

2. **Shorts Nike Dri-FIT Swift Feminino** — [link](https://www.nike.com.br/shorts-nike-dri-fit-swift-feminino-059101.html?cor=ND) · [foto](img/2026-07-13/nike/fem_02_shorts-swift.jpg) — R$399,99 (R$379,99 Pix) — 5.0★ (2)
   Bottom. Rosa, duas camadas (interna justa + externa solta), refletivos, logo Swoosh refletivo na coxa. Estrutura 80% poliéster/20% elastano.
   **Mix Wintors:** cor fora da nossa paleta; estrutura de camada dupla é um recurso técnico que não usamos — lacuna a considerar se formos além do básico.

3. **Regata Nike Dri-FIT Run Swift Feminina** — [link](https://www.nike.com.br/regata-nike-drii-fit-run-swift-feminina-030019.html?cor=52) · [foto](img/2026-07-13/nike/fem_03_regata-run-swift.jpg) — R$299,99 (R$208,99 Pix) — 4.3★ (6)
   Top. Bege/off-white, afunilada na cintura, painel de tela (mesh) grande nas costas para ventilação. 88% poliéster/12% elastano.
   **Mix Wintors:** bege é uma cor que conversa com nossa paleta (areia); corte afunilado com painel nas costas é uma referência técnica aproveitável mantendo sobriedade.

**Novidades**

4. **Regata Dri-FIT Nike Aeroswift Feminina** — [link](https://www.nike.com.br/regata-dri-fit-nike-aeroswift-feminina-029996.html?cor=O1) · [foto](img/2026-07-13/nike/fem_04_regata-aeroswift.jpg) — R$549,99 (R$470,24 Pix) — sem avaliações, "últimas unidades"
   Top. Verde-menta, tecido canelado/ribbed à mostra, corte justo (fitted), fendas laterais, pregas nas costas. 86% poliéster/14% elastano — linha "ADV" premium da Nike, quase 4x o preço da regata básica Swift.
   **Mix Wintors:** textura canelada é um recurso estético interessante e neutro o bastante pra caber em peça de clube — mas o preço/posicionamento é de linha alta-performance, fora do nosso ticket.

5. **Shorts Nike Dri-Fit ADV Aeroswift Feminino** — [link](https://www.nike.com.br/shorts-nike-dri-fit-adv-aeroswift-feminino-028115.html?cor=16) · [foto](img/2026-07-13/nike/fem_05_shorts-adv-aeroswift.jpg) — R$549,99 (R$522,49 Pix) — 4.5★ (18)
   Bottom. Azul lilás, tecido plissado/pregueado à vista, forro curto interno, cós elástico em tela. 86% poliéster/14% elastano.
   **Mix Wintors:** cor e textura fora do nosso território; mas confirma que "plissado" está entrando como diferencial visual em short técnico — vale observar se aparece em mais marcas.

6. **Shorts Nike Dri-FIT Tempo Feminino** — [link](https://www.nike.com.br/shorts-nike-dri-fit-tempo-feminino-060957.html?cor=NZ) · [foto](img/2026-07-13/nike/fem_06_shorts-tempo.jpg) — R$199,99 (R$189,99 Pix) — 5.0★ (3)
   Bottom. Verde-claro, modelagem simples/básica sem camada dupla, bolso interno embutido. 100% poliéster.
   **Mix Wintors:** é a peça mais "entrada" da leva feminina — preço mais próximo do nosso core, corte mais neutro.

---

## Cruzamento (Nike / Corrida)

**Por esporte:** as 11 peças aparecem tagueadas exclusivamente como "Corrida" no site — nenhuma cross-lista com outro esporte rastreado (Raquete, Musculação, Hyrox, Pilates) nesta amostra. Não há sinal de peça "coringa" entre esportes na Nike Corrida.

**Por cor:** Masculino é ancorado em preto técnico (3 das 5 peças: Run Swoosh, UV Miler, Regata Miler) + 1 verde vivo (short) + 1 verde-água pastel gráfico (Aeroswift). Feminino é o oposto — nenhuma cor se repete entre as 6 peças (preto, rosa, bege, verde-menta, azul-lilás, verde-claro): a Nike testa paleta bem mais ampla no público feminino de corrida do que no masculino.

**Por tipo de peça:** Masculino = 3 tops / 2 bottoms. Feminino = 2 tops / 4 bottoms — a Nike concentra a variação (camada dupla, plissado, cortes) nos shorts femininos, não nas peças de cima.

**Por preço vs. core Wintors (R$148-289):** a linha básica de Nike Corrida (Run Swoosh, UV Miler, Miler, Tempo — R$149,99 a R$249,99) **cai dentro ou logo abaixo do nosso core**, competindo direto na mesma faixa de preço com tecnologia Dri-FIT e reconhecimento de marca. Só a linha "Aeroswift/ADV" feminina (R$470-549) fica bem acima, como patamar premium separado — segmentação em duas linhas (básica vs. performance avançada) que não aparece tão marcada no masculino desta amostra.

## Fechamento — o que importa pra próxima coleção

1. **Nike Corrida não disputa o território "clube" da Wintors** — é 100% linguagem técnica (Dri-FIT, refletivos, UV, ventilação), sem peça pensada pra dupla vida academia→rua. Confiança: alta. Gatilho de mudança: se aparecer peça Nike Corrida com corte/tecido claramente "lifestyle" (ex.: camiseta 100% algodão sem gráfico técnico), revisar.
2. **A Nike compete no nosso preço na linha básica** (R$149-249) — não é mais cara que a Wintors nessa faixa, o que reforça que nosso diferencial tem que ser estética/pertencimento, não preço. Confiança: alta. Gatilho: acompanhar se essa faixa sobe na próxima varredura.
3. **Plissado/textura canelada como acabamento técnico-decorativo** apareceu 2x nesta leva (regata Aeroswift canelada, short ADV plissado) — sinal ainda fraco (1 marca, 1 esporte), não FORTE. Confiança: baixa. Gatilho: se aparecer em Adidas/Track&Field na próxima passada, sobe pra médio.

---

**Próximos passos da rodada bimestral:** Nike → Raquete/Musculação/Hyrox/Pilates (masc+fem) ainda pendente, depois Adidas, Wilson, Sporty & Rich, Track&Field, Alo — ritmo de 2 marcas/dia por decisão da Barbara (RB-14). Método de imagem (CDN direto) já resolvido e documentado no dossiê — repetir por marca (cada e-commerce tem seu próprio padrão de URL de CDN, mapear no início de cada marca nova).
