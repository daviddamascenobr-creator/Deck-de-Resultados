# Deck de Resultados

Gerador do e-mail mensal de **Fill Rate Data Original** e **Items Fill** por rede.

## Como usar

1. Abra o `index.html` no navegador (Chrome ou Edge). Precisa de internet para carregar as bibliotecas de planilha e gráfico.
2. Clique em **Escolher arquivo** (ou arraste) e selecione o `Deck de Resultados SP.xlsx`. Dá para soltar mais de um arquivo, por exemplo uma base de 2025, para ter a comparação com o ano anterior.
3. Escolha a **rede**, o **ano** e o período **De – Até** (por padrão, de janeiro até o mês anterior ao atual). Os gráficos mostram só os meses do período.
4. Confira os KPIs, os gráficos, os motivos de perda e ajuste o comentário, os destinatários e a assinatura.
5. Clique em **Confirmar e gerar modelo de e-mail** e depois em **Baixar e-mail (.eml)**. O arquivo abre no Outlook como rascunho, com Para, Cópia, assunto e gráficos.

A planilha é lida só no navegador; nada é enviado para fora.

## Como os números são calculados

- **Fill Rate** do mês = soma de `Volume Atendido FR Aurora` / soma de `Volume Total FR` (aba `Base_Fill Rate`).
- **Items Fill** do mês = soma de `Chaves Items Fill` / soma de `Chaves Totais Items Fill` (aba `Base_Items Fill`).
- **YTD / acumulado** = mesmas somas do mês "De" até o mês "Até".
- **vs ano anterior** = variação relativa entre os YTDs (só aparece se houver base do ano anterior).
- **Motivos de perda** (no texto sugerido) = soma de `Perdas IF` por `DePara_motivos` no mês.
- Destinatários vêm da aba `Base email`, cruzando `Número Rede` com `CÓD. REDE`.

## Planilha modelo

`Planilha Modelo - Deck de Resultados.xlsx` traz só o que o gerador precisa, com instruções na primeira aba e linhas de exemplo (SONDA, 2026) em amarelo:

- **Base_Fill Rate**: `CÓD. REDE`, `REDE`, `nome_rede_pdv`, `ano`, `mes`, `Volume Total FR`, `Volume Atendido FR Aurora`.
- **Base_Items Fill**: `CÓD. REDE`, `REDE`, `nome_rede_pdv`, `ano`, `mes`, `DePara_motivos`, `Chaves Totais Items Fill`, `Chaves Items Fill`, `Perdas IF`.
- **Base email**: `Número Rede`, `Rede`, `To`, `Cópia`.

O gerador acha as abas pelos cabeçalhos, então os nomes das abas podem mudar, mas os cabeçalhos não.
