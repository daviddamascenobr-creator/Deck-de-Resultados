# Deck de Resultados

Gerador do e-mail mensal de **Fill Rate Data Original** e **Items Fill** por rede.

## Como usar

1. Abra o `index.html` no navegador (Chrome ou Edge). Precisa de internet para carregar as bibliotecas de planilha e gráfico.
2. (Opcional) Clique em **Baixar planilha modelo** para pegar o modelo em branco. Depois clique em **Escolher arquivo** (ou arraste) e selecione o `Deck de Resultados SP.xlsx`. Dá para soltar mais de um arquivo, por exemplo uma base de 2025, para ter a comparação com o ano anterior.
3. Escolha a **rede**, o **ano** e o período **De – Até** (por padrão, de janeiro até o mês anterior ao atual). Os gráficos mostram só os meses do período.
4. Escolha o **modelo de gráfico** (colunas + linha, linha com área, colunas + acumulado ou linhas sobrepostas no modelo da Tamiris; a escolha fica salva no navegador), confira os KPIs e ajuste o comentário, os destinatários e a assinatura.
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

`Planilha Modelo - Deck de Resultados.xlsx` (também no botão **Baixar planilha modelo** do gerador) segue o formato das abas **KPI 25** e **KPI 26** da Tamiris, uma aba por ano:

`Rede_Semana`, `Rede_Mes`, `Rede Nome`, `x`, `cod_rede_pdv`, `mes`, `semana_do_ano`, `% FR Data Original`, `% Items Fill`, `Volume Total FR`, `Volume Atendido FR Aurora`, `Chaves Totais Items Fill`, `Chaves Items Fill`.

O gerador usa `cod_rede_pdv`, `Rede Nome`, `mes` e os quatro volumes. As colunas de % e as chaves `Rede_*` são só conferência. Pode ser uma linha por semana ou por mês. Para Para e Cópia, preencha na tela.

## Base no formato da Tamiris (abas "KPI 25", "KPI 26")

O gerador também lê a base semanal da Tamiris: abas com `cod_rede_pdv`, `Rede Nome`, `mes`, `Volume Total FR`, `Volume Atendido FR Aurora`, `Chaves Totais Items Fill` e `Chaves Items Fill`. Quando a aba não tem coluna `ano`, o ano vem do nome da aba (`KPI 25` = 2025).

Com o ano anterior na base, a comparação segue o modelo dela: o acumulado do ano escolhido (De–Até) contra o **ano anterior completo** (Jan–Dez), e os gráficos mostram o ano anterior inteiro em cinza.

Cada arquivo carregado substitui a base anterior. Para somar arquivos, solte todos juntos.
