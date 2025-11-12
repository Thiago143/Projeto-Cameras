# Checklist de Instalação e Comissionamento – Totem de Videomonitoramento
Versão: 2025-11-18
Fonte: `docs/tecnico/CADERNO_TECNICO_PONTO_MONITORAMENTO.md`, `docs/tecnico/CHECKLIST_ACEITE_PONTO.md`, `Instalação de Câmeras para 4º BPM RJ/plano_manutencao.md`

| Etapa | Item | Critério | Evidência | Status |
| --- | --- | --- | --- | --- |
| Pré-Instalação | Parecer de viabilidade civil | Laudo simples confirmando solo/estrutura | PDF/assinatura | [ ] |
| Pré-Instalação | LOS Visão Cruzada validada | Registro fotográfico A↔B (dia/noite) | Pasta `evidencias/PXX/` | [ ] |
| Estrutura | Fundação concretada | Dimensões 40x40x100cm, fck ≥ 25 MPa | ART + foto | [ ] |
| Estrutura | Tubo/caixa de passagem | PVC 100 mm ou aço galvanizado tratado | Foto antes da vedação | [ ] |
| Instalação | Fixação anti-vandalismo | Chumbadores inox + trava química | Notas de instalação | [ ] |
| Instalação | Cabeamento energizado | Isolação testada (megger ≥ 10 MΩ) | Relatório elétrico | [ ] |
| Instalação | PoE/No-break | Autonomia ≥ 4h e aterramento aferido | Foto painéis + checklist | [ ] |
| Comissionamento | Firmware atualizado | Versão homologada | Screenshot dashboard | [ ] |
| Comissionamento | Perfil ONVIF testado | Stream principal/sub validados | Print do VMS | [ ] |
| Comissionamento | KPIs baseline | MTBF/MTTR inicial e uptime previsto | Registro em `docs/kpis-definicoes-e-formulas.md` | [ ] |
| Operação | Inventário atualizado | `inventario/pontos_cameras.csv` com campos `ve_*` e evidências | Commit com referência | [ ] |
| Operação | Checklist LGPD | Papéis, base legal, retenção e trilha registrados | Ata + fluxo de dados | [ ] |

> Preencha e anexe ao dossiê do ponto. Sem os itens acima, o slide 17 (Riscos & Mitigações) deve sinalizar pendências.
