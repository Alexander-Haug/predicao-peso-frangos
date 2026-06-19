# Dados

A análise usa a base `Base_Dados_Modelos_peso.xlsx`, com 5.813 lotes e 40 variáveis, de um integrador avícola real (atividade extensionista). A variável-resposta é a coluna AN, `Peso Médio (kg)`.

## Confidencialidade

Os identificadores já vêm anonimizados (o produtor aparece como `P147`, o técnico como `Tecnico_1`, a região como `Regiao_1`), mas ainda assim são dados de produção proprietários. Por isso a base não é versionada neste repositório (veja o `.gitignore`). Há duas formas de tornar o projeto reprodutível.

A primeira, recomendada se o orientador autorizar: como os dados já estão anonimizados, basta colocar `Base_Dados_Modelos_peso.xlsx` nesta pasta. O notebook reproduz tudo exatamente.

A segunda, mais conservadora: manter a base fora do repositório. O notebook já está salvo com as saídas e os gráficos, então o projeto pode ser lido por completo direto no GitHub, sem os dados brutos.

Para rodar localmente, coloque o arquivo nesta pasta e ajuste o `BASE_PATH` no notebook, ou deixe a base ao lado do `.ipynb`.

## Grupos de variáveis

A base original traz uma aba `Metadados` com a descrição de cada coluna. Os principais grupos são:

- Setup e alojamento: produtor, região, técnico, tipo de instalação, nutrição, genética, origem, área, peso do pintinho, aves alojadas, densidade, vazio sanitário e data de alojamento.
- Acompanhamento do lote: pesagens semanais (Peso7 a Peso49) e mortalidades (%Mort7 a %Mort49).
- Medidas do abate, excluídas por vazamento: peso abatido, aves abatidas, idade média, rações e sobra de ração.
- Variável-resposta: `Peso Médio (kg)`, que equivale ao peso abatido dividido pelo número de aves abatidas.
