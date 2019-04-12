#LogProg-Trabalho-1

**Funcionamento do programa**

A entrada do frame é realizada pelo arquivo *frame.json*
Nele temos as seguintes entradas:

 - *states* : Estados presentes no frame, correspondentes aos vértices do grafo correspondente
 - *initialstate* : Estado inicial a partir do qual iniciaremos as operações [] e <>
 - *symbols* : O conjunto de símbolos proposicionais, ou átomos, que estão no contexto do frame
 - *relationships* : As relações entre os estados, correspondentes às arestas do grafo
 - *valuation* : Os conjuntos de estados nos quais cada símbolo é válido.

Para rodar o verificador:
	python valuation.py

O programa vai pedir a entrada da fórmula
	"Formula: "

No formato:
AND- '&'
OR-  '|'
NOT- '~'
IMPLIES- '->' 
NECESSARY- '[]'
PROBABLE- '<>'
SYMBOLS- Qualquer string alfanumérica

(Devido a limitações no parser, as operações de ~, [] e <> devem seguir a ordem de '~<>[]p', qualquer inversão na ordem desses operadores é necessário o uso de parênteses Ex.: '[](~<>p)' ou '[](<>(~p))' )

Saída
O programa retorna com 'True' ou 'False' segundo o resultado da validação