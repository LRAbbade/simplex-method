# Simplex

+ Montar o PPL
+ Colocar as variáveis básicas (ie. A, B, C...)
	1. <= -> +
	2. >= -> -

+ Montar a tabela:
					| Variáveis de decisão 	| variáveis básicas | Lado Direito (resultados)
Função objetivo		| (negativar as vars)	|					|
variáveis básicas 	|						|					|

+ while (alguma variável de decisão na função objetivo < 0):
	1. Pegar o mais negativo da função objetivo -> coluna pivot
	2. Dividir os valores do lado direito pela coluna pivot
	3. Pegar o menor dos resultados como número pivot
	4. Trocar o nome da coluna com o nome da linha do número pivot
	5. Calcular a linha pivot pegando a linha do número pivot dividido por ele mesmo
		(linha pivot / número pivot)
	6. Zerar os números da coluna pivot multiplicando todas as linhas
		(número[linha_atual][coluna atual] - número pivot * número[linha_pivot][coluna_atual])

+ Resultado ótimo estará em número[função_objetivo][lado_direito]
+ Valor das variáveis de decisão:
	1. (Variáveis de decisão que foram passadas para a primeira coluna) * (Valor na coluna lado direito)