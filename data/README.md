# Dados

A análise usa a base `Base_Dados_Modelos_peso.xlsx` (5.813 lotes × 40 variáveis), de um
**integrador avícola real** (atividade extensionista). A variável-resposta é a coluna
**AN — `Peso Médio (kg)`**.

## ⚠️ Confidencialidade

Identificadores já vêm pseudonimizados (`P147`, `Tecnico_1`, `Regiao_1`), mas é dado de
produção proprietário. Por isso a base **não é versionada** neste repositório
(veja `.gitignore`). Há duas formas de tornar o projeto reprodutível:

- **Opção A (recomendada se o orientador autorizar):** como os dados já estão anonimizados,
  comitar `Base_Dados_Modelos_peso.xlsx` nesta pasta. O notebook reproduz tudo exatamente.
- **Opção B (padrão seguro):** manter a base fora do repositório. O notebook já está salvo
  **com as saídas e gráficos**, então o projeto pode ser lido por completo direto no GitHub
  sem os dados brutos.

Para rodar localmente, coloque o arquivo nesta pasta e ajuste `BASE_PATH` no notebook, ou
deixe-o ao lado do `.ipynb`.

## Dicionário de variáveis

O arquivo original traz uma aba `Metadados` com a descrição de cada coluna. Principais grupos:

- **Setup / alojamento:** Produtor, Região, Técnico, Tipo de Instalação, Nutrição, Genética,
  Origem, Área, Peso do Pintinho, Aves Alojadas, Densidade, Vazio sanitário, Data de Alojamento.
- **Acompanhamento:** pesagens semanais (Peso7…Peso49) e mortalidades (%Mort7…%Mort49).
- **Abate (excluídas por vazamento):** Peso Abatido, Aves Abatidas, Idade Média, rações, sobra.
- **Alvo:** `Peso Médio (kg)` = Peso Abatido ÷ Aves Abatidas.
