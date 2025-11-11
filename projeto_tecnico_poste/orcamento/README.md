# Orçamento e Quantitativos

Guarde planilhas de custo, memoriais de cálculo financeiro e cotações. Recomendações:
- Use planilhas com abas para materiais, mão de obra e contingências.
- Gere uma versão PDF para anexar a apresentações ou dossiês.
- Registre a fonte de cada preço (fornecedor, data da cotação) diretamente na planilha.

Arquivos atuais:
- `raw/Copia_descritivo_totem4bpm.csv`: export bruto da planilha do Google Sheets (não altere para preservar o original).
- `lista_materiais.csv`: versão normalizada com colunas padrão (`categoria`, `equipamento`, `valor_estimado`, `fonte_link`, `cotacao_status`). Atualize `cotacao_status` para `cotado` assim que houver valor confirmado e acrescente observações (fornecedor, quantidade, validade).
- `caixa_servico/`: orçamentos específicos para a caixa de serviço interna ao poste (contém `Orcamento_Projeto_2.pdf` e a captura HTML `orcamento_imaginatech_caixa.html`). Registre dentro dessa pasta qualquer memorial de cálculo ou contato relacionado a fornecedores da caixa.
- `orcamento_resumo.csv`: consolidação manual por categoria (preencha quantidades, custos totais e status de cada linha para facilitar apresentações).
