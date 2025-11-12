# Guia de Parametrização – Deck Técnico Genérico PMERJ
Versão: 2025-11-18
Origem: síntese de `docs/tecnico/CADERNO_TECNICO_PONTO_MONITORAMENTO.md`, `docs/operacionais/GOVERNANCA_DOCUMENTAL.md`, `Instalação de Câmeras para 4º BPM RJ/plano_manutencao.md` e inventário `inventario/pontos_cameras.csv`.

## 1. Propósito
Padronizar a apresentação "Deck Técnico Genérico – Totens de Videomonitoramento PMERJ" para qualquer região/unidade, mantendo rigor técnico, governança documental e narrativa neutra. O deck vive em `presentations/deck-tecnico-generico/Deck_Tecnico_Generico_PM_ERJ.pptx`.

## 2. Estrutura dos Slides
| Bloco | Slides | Conteúdo | Fontes primárias |
| --- | --- | --- | --- |
| Executivo | 0–3, 13–15, 21 | Capa, sumário, problema, cronograma paramétrico, modelos CAPEX/OPEX e decisão | `docs/conteudo/documento_tecnico_cameras.md`, `docs/conteudo/sumario_executivo_cameras.md`, `Instalação/.../sumario_executivo.md` |
| Técnico | 4–12, 16–18 | Hardware, antivandalismo, conectividade, arquitetura, dados, KPIs, metodologia de avaliação, topografia/LOS | `docs/tecnico/CADERNO_TECNICO_PONTO_MONITORAMENTO.md`, `projeto_tecnico_poste/`*, `docs/tecnico/CHECKLIST_ACEITE_PONTO.md` |
| Operação/Governança | 8–11, 16–18 | Protocolos CCO/COPOM, governança de dados, manutenção, riscos, interoperabilidade | `docs/operacionais/*.md`, `Instalação/.../plano_manutencao.md`, `docs/juridico/*.md` |
| Case | 19 | Slide opcional com dados do 4º BPM (retirar sem quebrar narrativa) | `inventario/pontos_cameras.csv`, `evidencias/PXX/` |
| Anexos | 22 + A1–A5 | Fichas, checklists, matriz KPI, minuta PPP, identidade visual | `presentations/deck-tecnico-generico/anexos/` |

> *`projeto_tecnico_poste/` concentra mapas (LOS), memorial e orçamentos; use apenas dados agnósticos ou anonimizados.

## 3. Placeholders Obrigatórios
| Placeholder | Onde aparece | Como preencher |
| --- | --- | --- |
| `[N_PONTOS]` | cronograma, KPIs, custos | Utilize um dos lotes 12/16/25/50. Atualize tabelas e gráficos (Slide 13 e anexos) para manter coerência com inventário. |
| `[LINK_PRIMARIO]` | arquitetura, conectividade, anexos | Escolha fibra, rádio ou 4G (fallback). Cite redundância e SLA `[UPTIME_ALVO]`. |
| `[UPTIME_ALVO]` | KPIs e anexos | 99,5% (operacional mínimo) ou 99,7% (sítios críticos). Observar `Instalação/.../plano_manutencao.md`. |
| `[TME_DETECCAO]`, `[TMA_DESPACHO]`, `[TMA_CHEGADA]` | slides 10–11 e `docs/kpis-definicoes-e-formulas.md` | Basear-se nos dados COPOM/CICC da região. Caso não existam, usar baseline 60s / 120s / 8min e marcar como "target". |
| `[CUSTO_CAPEX_PONTO]`, `[OPEX_MENSAL_PONTO]` | slides 15–16 e A3 | Use faixas documentadas no memorial/orçamentos (`projeto_tecnico_poste/orcamento`). Sempre registrar premissas nas notas do slide e no arquivo `docs/kpis-definicoes-e-formulas.md`. |
| `[REGIAO]` | somente quando houver mapa genérico ou topografia | Informe apenas estado/região (ex.: "Interior RJ"), evitando citar AISP/CISP. |

## 4. Fluxo de Atualização
1. **Criar cópia do PPTX:** `cp Deck_Tecnico_Generico_PM_ERJ.pptx Deck_Tecnico_XX_vY.Z.pptx`.
2. **Parametrizar dados chave:** atualizar placeholders, gráficos, cronograma e anexos conforme lote selecionado.
3. **Revisar governança:**
   - Atualizar `docs/kpis-definicoes-e-formulas.md` com baseline/targets.
   - Caso algum dado venha de inventários/atas, registrar no `CHANGELOG.md` e `inventario_arquivos.csv`.
4. **Exportar anexos:**
   - `A1` e `A5` (PDF) já possuem texto base; ajuste quando specs mudarem.
   - `A2` (checklist) deve acompanhar cada execução.
   - `A3` (planilha) precisa dos valores consolidados antes da entrega.
   - `A4` (docx) serve de minuta para CAPEX/PPP – personalize cláusulas financeiras.
5. **Gerar diagrama Visio:** edite `assets/diagrama_arquitetura.drawio` e exporte para `.vsdx` (substituindo o placeholder `assets/diagrama_arquitetura.vsdx`).
6. **QA final:** seguir checklist do commit (slides coerentes, LGPD validada, case opcional destacado).

## 5. Conteúdos Reutilizáveis
- **Hardware & antivandalismo:** ver seção 6 do `Caderno Técnico`. Copiar especificações de poste, blindagem e testes de LOS.
- **Conectividade e energia:** `Instalação/.../solucoes_energia_conectividade.md` traz cenários híbridos (rede, rádio, solar). Utilize gráficos comparativos neutramente.
- **Cronograma paramétrico:** `Instalação/.../cronograma_implementacao.png` pode ser referenciado para os marcos D0–D30–D60; replique as durações mantendo descrições neutras.
- **KPIs:** baseline de manutenção em `plano_manutencao.md` + indicadores operacionais nos documentos de SUMÁRIO/PROJETO.
- **Governança & LGPD:** `docs/operacionais/GOVERNANCA_DOCUMENTAL.md` e `docs/juridico/*` dão base para slides 9 e 17.

## 6. Boas Práticas de Apresentação
- Usar `assets/logos_institucionais.svg` e `assets/icones_kpi.svg` diretamente nos slides para manter identidade.
- Mapas devem partir de `assets/mapa_cobertura_placeholder.png` ou visuais próprios sem referência explícita ao 4º BPM.
- Slide 19 (case) deve ser completamente removível; use dados do inventário apenas como exemplo e cite "Case 4º BPM (removível)" no rodapé.
- Citar anexos no final com hiperlinks internos (A1–A5) para manter trilha documental.
- Sempre relacionar riscos a mitigação concreta (ver `docs/juridico/ANEXO_TECNICO_I_BARRASHOPPING.md` para estrutura de tabela).

## 7. Checklist de Qualidade
- [ ] Todos os placeholders substituídos ou ocultados.
- [ ] KPIs alvo e baseline documentados em `docs/kpis-definicoes-e-formulas.md`.
- [ ] Fluxo operacional revisado com o CCO/COPOM local (evidência na ata ou `evidencias/`).
- [ ] Slide LGPD cita papéis, base legal, retenção e trilha de auditoria.
- [ ] Mapas neutros sem georreferência específica ou com dados fictícios claramente marcados.
- [ ] Cronograma condizente com a capacidade de campo (120 dias máximo para 50 pontos).
- [ ] Case 4º BPM marcado como opcional e removível.

> Em caso de dúvidas, abrir issue interna e registrar dependências conforme `docs/operacionais/GOVERNANCA_DOCUMENTAL.md`.
