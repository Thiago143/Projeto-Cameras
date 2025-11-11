# CHANGELOG – Projeto Câmeras Ostensivas

Formato baseado em [Keep a Changelog](https://keepachangelog.com/pt-BR/1.0.0/) e seguindo [Semantic Versioning](https://semver.org/spec/v2.0.0.html) quando versões forem publicadas.

## [Unreleased]
- Estruturação dos desenhos CAD, memorial descritivo e mapas derivados (GeoJSON/KML).
- Consolidação das fontes editáveis (Keynote, DOCX recentes) nas pastas `base/`.
- Integração do DevOps Agent aos pipelines de exportação e push automático.

## 2025-11-11
### Adicionado
- `README.md` com visão geral do projeto, estrutura e próximos entregáveis.
- `GITHUB_MANUAL.md` adaptado ao contexto do Projeto Câmeras, documentando fluxo Git/GitHub, checklist e papel do DevOps Agent.
- `projeto_tecnico_poste/orcamento/caixa_servico/README.md` descrevendo os orçamentos da caixa interna.
- `projeto_tecnico_poste/mapas/raw/metadata.md` registrando fonte e instruções dos shapefiles AISPs.
- `docs/conteudo/projeto_cameras.md`, `docs/conteudo/documento_tecnico_cameras.md`, `docs/conteudo/orcamento_imaginatech_caixa.md`, `docs/conteudo/README.md`, `docs/conteudo/sumario_executivo_cameras.md` e `docs/conteudo/apresentacao_2025-11.md`, preparando o repositório para trabalhar majoritariamente em Markdown.
- Templates adicionais: `projeto_tecnico_poste/memorial_descritivo/memorial_tecnico_poste.md`, `projeto_tecnico_poste/entrada_requisitos/locais_instalacao.csv`, `projeto_tecnico_poste/mapas/pontos_instalacao.csv`, `projeto_tecnico_poste/orcamento/orcamento_resumo.csv`.
- `docs/operacionais/PROCESSOS.md` descrevendo o fluxo ponta-a-ponta de atualização e revisão.

### Modificado
- `inventario_arquivos.csv` passou a rastrear novos documentos (apresentação 2025-11, orçamentos da caixa, pacote de mapas).
- `projeto_tecnico_poste/mapas/README.md` agora referencia o shapefile extraído `shp_limite_aisp_072024` e o template `pontos_instalacao.csv`.
- Entradas dos DOCX/HTML legados atualizadas para apontar as novas fontes em Markdown e o inventário passou a incluir os novos templates/processos.

### Contexto
- Preparação para publicar a primeira versão integrada no GitHub privado, garantindo que todas as pastas tenham instruções claras e inventário atualizado antes da sincronização inicial.

## 2025-11-10
### Adicionado
- Estrutura completa do `projeto_tecnico_poste/` (requisitos, normas, desenhos, memorial, orçamento, mapas, imagens).
- `inventario_arquivos.csv` com colunas de status e referência de substituição.
- Organização temporal dos arquivos em `arquivo/2025-05`, `base/2025-06-07` e `base/2025-11`.

### Modificado
- `docs/operacionais/AGENTS.md` atualizado com diretrizes do repositório.

### Contexto
- Reorganização inicial do acervo para distinguir materiais legados, base vigente e documentação operacional, preparando a migração para controle de versão profissional.
