# Pandas — Métodos Úteis

## Visualização

| Método | Descrição |
|---|---|
| `df.head(n)` / `.tail(n)` | Primeiras/últimas n linhas |
| `df.sample(n)` | n linhas aleatórias |
| `df.info()` | Tipos, memória, não-nulos |
| `df.describe()` | Estatísticas (média, std, min, max, quartis) |
| `df.value_counts()` | Frequência de valores únicos |
| `pd.set_option("display.max_columns", N)` | Configurar exibição |
| `df.style.background_gradient()` | Tabela colorida por valor |
| `df.style.bar()` | Barras horizontais nas células |
| `df.style.highlight_max()` | Destacar máximos |
| `df.style.format("{:.2f}")` | Formatar casas decimais |
| `df.plot()` | Gráfico simples (linha) |
| `df.plot(kind="bar"/"hist"/"box"/"scatter")` | Tipos de gráfico |
| `df.hist()` | Histograma de todas as colunas |
| `df.plot.box()` | Boxplot |

## Seleção

| Método | Descrição |
|---|---|
| `df["col"]` | Coluna como Series |
| `df[["a", "b"]]` | Múltiplas colunas |
| `df.loc[linhas, colunas]` | Seleção por rótulo |
| `df.iloc[linhas, colunas]` | Seleção por índice numérico |
| `df.filter(like="palavra")` | Colunas que contêm "palavra" |
| `df.query("col > 10")` | Filtro com expressão |

## Manipulação

| Método | Descrição |
|---|---|
| `df.assign(nova=expr)` | Criar coluna (retorna cópia) |
| `df["nova"] = expr` | Criar/atribuir coluna in-place |
| `df.drop(columns=["a"])` | Remover colunas |
| `df.rename(columns={"antigo": "novo"})` | Renomear colunas |
| `df.set_index("col")` / `.reset_index()` | Definir/redefinir índice |
| `df.sort_values("col")` | Ordenar |
| `df.groupby("col").agg(...)` | Agrupar e agregar |
| `df.pivot_table(index, columns, values)` | Tabela dinâmica |
| `df.melt(id_vars=["id"])` | Derreter (wide → long) |
| `pd.concat([df1, df2])` | Empilhar DataFrames |
| `df.merge(df2, on="chave")` | Juntar (SQL join) |

## Limpeza

| Método | Descrição |
|---|---|
| `df.isna().sum()` | Contar nulos por coluna |
| `df.dropna()` | Remover linhas com nulo |
| `df.fillna(valor)` | Preencher nulos |
| `df.astype({"col": float})` | Converter tipo |
| `df.duplicated().sum()` | Contar duplicatas |
| `df.drop_duplicates()` | Remover duplicatas |

## Avançado

| Método | Descrição |
|---|---|
| `df.apply(função)` | Aplicar função por coluna/linha |
| `df.pipe(função)` | Pipeline de transformações |
| `df.explode("col")` | Expandir listas em linhas |
| `df.corr()` | Matriz de correlação |
| `pd.cut(x, bins)` | Discretizar em faixas |
| `pd.qcut(x, q)` | Discretizar por quantis |

## IO

| Método | Descrição |
|---|---|
| `df.to_csv("saida.csv")` | Exportar CSV |
| `df.to_excel("saida.xlsx")` | Exportar Excel |
| `pd.read_excel()` | Importar Excel |
| `pd.read_json()` | Importar JSON |
