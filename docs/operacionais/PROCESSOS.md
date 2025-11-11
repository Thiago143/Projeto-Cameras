# Processos Operacionais – Projeto Câmeras

## 1. Fluxo de Atualização de Documentos
1. Registrar alterações em Markdown (`docs/conteudo/`).
2. Atualizar `inventario_arquivos.csv` (status + referência).
3. Revisar `CHANGELOG.md` e READMEs afetados.
4. Acionar DevOps Agent para commits/push.

## 2. Revisão Técnica (Cada Entrega)
- **Conteúdo**: coerência com dados oficiais (`Análises.pdf`, relatórios mais recentes).
- **Layout**: conferência em PDF exportado (acessibilidade, brasão oficial).
- **Aprovação**: responsável do BPM + coordenação técnica.

## 3. Pipeline de Engenharia do Poste
1. Requisitos de campo (`entrada_requisitos/locais_instalacao.csv`).
2. Memorial (`memorial_descritivo/memorial_tecnico_poste.md`).
3. Desenhos (DWG/PDF) e mapas com coordenadas.
4. Orçamento consolidado (`orcamento_resumo.csv` + `lista_materiais.csv`).

## 4. Controle de Localizações
- Atualizar `mapas/pontos_instalacao.csv`.
- Relacionar cada ponto ao shapefile AISP.
- Anexar fotos/relatórios em `imagens_postes/`.

## 5. Checklist Pré-Expansão
| Item | Responsável | Status |
| --- | --- | --- |
| Conteúdo atualizado em MD | Documentação | ☐ |
| Memorial + desenhos revisados | Engenharia | ☐ |
| Orçamento fechado | Financeiro | ☐ |
| Mapas e pontos validados | GIS | ☐ |
| Commit + Push realizados | DevOps Agent | ☐ |

Atualize este arquivo sempre que o processo mudar (inclua datas e responsáveis).
