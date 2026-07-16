# Wintors & Caaines — Departamento de Coleção (8 robôs)

> Criado em 12/07/2026, substituindo o sistema TF1-TF14 (enxugado por decisão da Barbara). Wintors é o projeto-mãe; este repo é o **departamento de Coleção**. O departamento de Ads (R1-R9) vive em `C:\Users\BARBARA\wintors-intelligence\`.

## Missão
**Decidir a próxima coleção com dado real:** o que relançar, o que evoluir e qual peça nova arriscar — cruzando o que vende de verdade (Shopify) com o que o mercado sinaliza. Todo o resto é meio, não fim.

## Os 8 robôs
| # | Robô | Pasta | Skill | Cadência |
|---|---|---|---|---|
| 1 | Dores & Uso por Esporte | `dores-uso/` | `/colecao-dores` | Trimestral |
| 2 | Varredura de Concorrentes (2 lentes: esportiva + casual) | `concorrentes/` | `/colecao-concorrentes` | Bimestral |
| 3 | Tendências Fitness & Hábitos | `tendencias/` | `/colecao-tendencias` | Mensal leve |
| 4 | Meu Mix & Vendas (Shopify) | `meu-mix/` | `/colecao-mix` | Por ciclo — SEMPRE antes do 6 |
| 5 | Inteligência WGSN (conversa) | `wgsn/` | `/colecao-wgsn` | Sob demanda |
| 6 | Coleção — dimensiona, decide, audita e opina | `colecao/` | `/colecao-decisao` | Por ciclo de coleção |
| 7 | Acervo Visual (board Pinterest + Ralph Lauren) | `referencias/` | `/colecao-referencias` | Bimestral |
| 8 | Estilista (pranchas em PDF; NÃO gera imagem) | `estilista/` | `/colecao-estilista` | Por ciclo — SEMPRE depois do 6 |

Extra fora de cadência: **Jornada de Compra** (`anual/`, 1x/ano). **Voz do Cliente não é robô** — é insumo manual que a Barbara deposita em `colecao/insumos/`.

Cada pasta de robô tem: `dossie.md` (a formação — o dossiê É o prompt, seguir exclusivamente) + outputs datados `YYYY-MM-DD_*.md`.

## Ordem dura do ciclo de coleção
`Robô 4 (mix/vendas)` roda **antes** do `Robô 6 (coleção)` — sem histórico, não se propõe peça. `Robô 8 (estilista)` roda **depois** do 6 — só desenha decisão dimensionada (extras autorais dele são exceção marcada e voltam pro 6). O `Robô 7 (acervo)` alimenta o 8; os robôs 1-3 e 5 alimentam quando têm output fresco; o Robô 6 declara a idade de cada insumo que usou. Fechamento do loop visual: a Barbara gera a imagem final da peça no **Gemini pago dela** (nenhum robô gera imagem) e deposita na pasta → o Robô 7 cataloga com `fonte: "gerada"` vinculada à decisão.

## Regras transversais (valem pra TODOS os robôs — não repetir nos dossiês)
1. **Preflight obrigatório**, nesta ordem: (a) `context/empresa.md` + `context/brand.md`; (b) `context/regras_barbara.json`; (c) `context/feedbacks.json` — todo feedback com status `novo` deve ser lido e citado se relevante; o Robô 6 é obrigado a DISCUTIR cada feedback aberto com a Barbara antes de propor; (d) memória persistente do Claude quando disponível (`~/.claude/projects/C--Users-BARBARA/memory/`).
2. **BR-first:** sinal global sozinho NUNCA classifica FORTE sem eco BR; sinal BR pode ser FORTE sozinho. Benchmark sempre em BRL. Régua completa: FRACO = 1 fonte sem repetição · MÉDIO = 2+ globais sem eco BR, ou 1 BR isolada · FORTE = 2+ BR, ou 2+ globais com eco BR.
3. **Pesquisa em passadas** (nunca busca única): mínimo 2 passadas com queries diferentes, trilha auditável (registrar o que buscou), toda afirmação com **fonte nomeada + data** — sem fonte = marcado "palpite".
4. **Filtro de marca:** toda recomendação passa pelo teste do brand: "cabe em quem transita entre esporte, autocuidado e vida social, estética de clube atemporal (tênis 70-90, verde profundo)?" Alta performance técnica e fast fashion estão fora do território.
5. **Output = 1 tela**, decisões e não observações, cada decisão com número + confiança (alta/média/baixa) + gatilho de mudança.
6. **Grava sempre, sem pedir permissão** (dado privado da Barbara) e **sync git** ao final:
```bash
cd "C:\Users\BARBARA\wintors-colecao"
git pull origin master   # antes de rodar
git add -A && git commit -m "Auto-sync: [robô] — YYYY-MM-DD" && git push origin master   # ao final, best-effort
```
7. **Nada é salvo no Google Drive.** Drive é só FONTE de leitura (PDFs WGSN da pasta "wgsn 25"). Outputs vivem aqui e no GitHub.
8. **Esportes rastreados** (`context/esportes.json`): Corrida · Esportes de Raquete (Tênis, Padel, Beach Tennis) · Musculação · Hyrox · Pilates. A lista só muda com aprovação da Barbara.
9. **Dado perecível nunca é citado como atual** — número de rodada antiga entra sempre com a data do snapshot.

## Registro de feedback (qualquer chat, 10 segundos)
Quando a Barbara disser "anota esse feedback" (ou `/colecao-feedback`): gravar em `context/feedbacks.json` com data, quem falou, sobre o quê (peça/esporte/geral), o que disse, status `novo`. Ciclo: `novo → discutido → incorporado | descartado`. Só o Robô 6 (com a Barbara) muda status.

## O que depende de aprovação da Barbara
- `context/mix.md` — a definição de mix de produto. **Enquanto marcado RASCUNHO, os robôs 4 e 6 não rodam.**
- Mudança na lista de esportes, nas fontes aprovadas de cada dossiê e nas regras deste arquivo.

## Ferramentas testadas (não inventar capacidade)
| Ferramenta | Status | Usada por |
|---|---|---|
| Shopify MCP | ✅ conectado | Robô 4 |
| Chrome conectado (Pinterest logado, captura de concorrente) | ✅ funciona no PC | Robôs 2, 3, 7 |
| Skill `assistir-criativo` (Gemini assiste vídeo TikTok) | ✅ funciona no PC | Robô 1 |
| Conector Google Drive (leitura de PDF) | ⚠️ leitura OK; PDFs pesados WGSN NÃO testados — 1º run do Robô 5 é teste; fallback = Chrome no PC | Robôs 5, 6 |
| Bright Data | ❌ não instalado (pago, pausado) | — |
