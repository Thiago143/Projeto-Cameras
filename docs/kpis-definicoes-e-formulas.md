# KPIs – Definições, Fórmulas e Premissas
Versão: 2025-11-18
Responsável: Thiago (Coordenação Técnica)
Fontes: `Instalação de Câmeras para 4º BPM RJ/plano_manutencao.md`, `docs/tecnico/CADERNO_TECNICO_PONTO_MONITORAMENTO.md`, `docs/operacionais/GOVERNANCA_DOCUMENTAL.md`, `inventario/pontos_cameras.csv`.

## 1. Indicadores Principais do Deck
| KPI | Definição | Fórmula | Meta/Target | Fonte primária |
| --- | --- | --- | --- | --- |
| Disponibilidade do Sistema | Percentual de tempo com todos os subsistemas ativos (energia, rede, sensores) | `(Tempo total - Tempo indisponível) / Tempo total` | `[UPTIME_ALVO]` (99,5% padrão / 99,7% pontos críticos) | NOC / Telemetria VMS |
| Disponibilidade por Totem | Saúde individual (ponto a ponto) | `Horas disponíveis ponto / Horas no período` | ≥ 98% | Inventário + Telemetria |
| TME Detecção | Tempo entre evento e identificação pelo operador | `Σ tempo detecção / Nº eventos` | `[TME_DETECCAO]` (baseline 60 s) | CCO / Logs VMS |
| TMA Despacho | Tempo entre confirmação e despacho COPOM/190 | `Σ tempo despacho / Nº acionamentos` | `[TMA_DESPACHO]` (baseline 120 s) | COPOM/CICC |
| TMA Chegada | Tempo para recurso chegar ao local | `Σ tempo chegada / Nº ocorrências` | `[TMA_CHEGADA]` (baseline 8 min) | COPOM + GPS |
| MTBF | Tempo médio entre falhas críticas | `Horas operadas / Nº falhas` | ≥ 2.000 h | Sistema de manutenção |
| MTTR | Tempo médio para reparar | `Σ tempo reparo / Nº reparos` | ≤ 4 h | Sistema de manutenção |
| Resolução 1º Atendimento | % de chamados resolvidos na primeira visita | `Chamados resolvidos 1ª visita / Total chamados` | ≥ 85% | Plano de manutenção |
| Custo OPEX por Ponto | Custo mensal de operação dividido pelos totens ativos | `Custo mensal / Pontos ativos` | `[OPEX_MENSAL_PONTO]` (baseline R$ 577–634) | Financeiro / Contratos |
| Taxa de Cobertura Topológica | % de pares adjacentes com visão cruzada documentada | `Pares LOS aprovados / Pares planejados` | 100% | Checklists de aceite |

## 2. Baselines e Ranges
| Indicador | Baseline atual (4º BPM) | Range sugerido para deck | Observações |
| --- | --- | --- | --- |
| `[N_PONTOS]` | 12 pontos planejados (Expomag + entorno) | 12 / 16 / 25 / 50 | Escolher cenário e replicar nos gráficos paramétricos. |
| `[CUSTO_CAPEX_PONTO]` | R$ 38k – 55k (fonte: `projeto_tecnico_poste/orcamento/lista_materiais.csv`) | Mostrar faixa + premissas (poste, câmeras, conectividade). |
| `[OPEX_MENSAL_PONTO]` | R$ 577 – 634 (fonte: plano de manutenção) | Exibir faixa e indicar drivers (manutenção, telecom, energia). |
| MTBF | Sem medição histórica (piloto) | Use 2.000 h target | Registrar no slide 17 que valores reais virão após 90 dias. |
| MTTR | 4 h (target contratual) | ≤ 4 h | Associar a SLA de manutenção nível 2. |

## 3. Metodologia de Medição
1. **Coleta Operacional:** dados de despacho (COPOM/190) e chegada (GPS) exportados semanalmente; consolidar no anexo A3.
2. **Telemetria Técnica:** utilizar logs do VMS e controlador PoE para uptime/MTBF/MTTR.
3. **Inventário:** cada atualização em `inventario/pontos_cameras.csv` deve refletir `ve_*` e campos de evidência LOS.
4. **Auditoria:** seguir `docs/operacionais/GOVERNANCA_DOCUMENTAL.md` para rastreabilidade. Sem checklist, não atualizar slides.
5. **LGPD:** slide 9 precisa listar papéis (Controlador: PMERJ; Operador: parceiro). Retenção padrão 90 dias, prorrogável mediante ordem judicial.

## 4. Procedimento para Atualizar Targets
1. Registrar baseline real (por região) nesta tabela (linha nova com data/região).
2. Atualizar planilha `A3_matriz_kpi_metricas.xlsx` com os mesmos valores → manter consistência.
3. No deck, usar notas do apresentador para citar a fonte e data de coleta.
4. Caso algum valor não esteja consolidado, marcar como "target" e citar no slide 17 (riscos) que o indicador aguarda validação.

## 5. Dependências e Evidências
- **Telemetria / Logs:** armazenar prints e exportações em `evidencias/PXX/` seguindo o ID do ponto.
- **Checklist de aceitação:** obrigatório anexar `A2_checklist_instalacao_comissionamento.md` preenchido.
- **Cronograma:** alinhar com `Instalação de Câmeras para 4º BPM RJ/cronograma_implementacao.png` para manter consistência de marcos D0–D30–D60.
- **Relatórios financeiros:** toda menção a CAPEX/OPEX deve citar a planilha oficial em `projeto_tecnico_poste/orcamento/`.

## 6. Histórico de Revisões
| Data | Alteração | Responsável |
| --- | --- | --- |
| 2025-11-18 | Versão inicial com placeholders e metas padrão para o deck genérico. | Thiago |
