# Projeto Câmeras Ostensivas – Base Operacional

Este repositório concentra toda a documentação e os artefatos necessários para planejar, implantar e expandir o programa de câmeras ostensivas conectadas aos batalhões da PMERJ.

## Estrutura
- `base/` – Versões vigentes das entregas (ex.: `2025-11/PROJETO_DE_IMPLEMENTACAO...pdf`).
- `arquivo/` – Histórico de maio/2025 preservado para referência e auditoria.
- `docs/operacionais/` – Guias de processo (`AGENTS.md`, checklists e DevOps).
- `projeto_tecnico_poste/` – Módulo técnico (requisitos, normas, mapas, orçamentos, memorial descritivo, imagens e desenhos).
- `inventario_arquivos.csv` – Inventário central com status (válido/atualizar/substituir) de cada arquivo.

## Fluxo de Trabalho
1. **Documentar**: adicione fontes editáveis e exports lado a lado, mantendo nomes `tema_contexto_vYYMMDD.ext`.
2. **Inventariar**: sempre atualize `inventario_arquivos.csv` ao inserir, mover ou substituir arquivos.
3. **Validar**: use os READMEs de cada pasta como checklist (ex.: `orcamento/`, `mapas/`).
4. **Versionar**: siga o manual `GITHUB_MANUAL.md` para commits, changelog e sincronização com o GitHub.

## Próximos Entregáveis
- Inserir fontes editáveis da apresentação 2025-11 e do sumário executivo.
- Preencher `projeto_tecnico_poste/memorial_descritivo/` com o memorial e normas aplicáveis.
- Associar os pontos de instalação aos shapefiles de AISPs (já disponíveis em `mapas/raw/`).
- Completar `lista_materiais.csv` com quantidades e valores confirmados.

## Sensibilidade dos Dados
O material contém diretrizes operacionais e imagens sensíveis. Mantenha o repositório privado, sanitizado (sem EXIF ou PII) e use criptografia para mídias não documentais.
