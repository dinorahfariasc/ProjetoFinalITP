# Sistema de Gerenciamento de Banco de Dados - ITP
Este é um sistema simples de gerenciamento de tabelas em C. O projeto é estruturado em módulos separados para as operações de criação, edição, exclusão e visualização de tabelas. Abaixo, fornecemos uma visão geral da estrutura do projeto, suas dependências e principais funções.

## Estrutura do Projeto

O projeto é composto por vários módulos organizados em arquivos separados:

- `criacao.h`: Módulo para funções relacionadas à criação de tabelas.
- `edicao.h`: Módulo para funções relacionadas à edição de tabelas.
- `exclusao.h`: Módulo para funções relacionadas à exclusão de linhas e tabelas.
- `visualizacao.h`: Módulo para funções relacionadas à visualização de tabelas.

Cada módulo possui suas implementações correspondentes em arquivos `.c`.

O arquivo principal `main.c` contém a função principal (`main()`) que interage com o usuário e coordena a execução das operações do sistema.

### A estrutura base da tabela foi feita com os seguintes atributos:

`char *nomeTabela`: Um ponteiro para uma string (char *) que armazena o nome da tabela. Essa string representa o nome identificador único atribuído à tabela.

`char **nomesColunas`: Um ponteiro para ponteiro de string (char **) que representa o nome das colunas da tabela.

`void ***listaValores`: Um ponteiro para ponteiro para ponteiro (void ***). Esse campo representa uma estrutura multidimensional que armazena os valores das células da tabela. A ideia é que esta estrutura possa acomodar diferentes tipos de dados. 

`int nCol`: Um inteiro que indica o número total de colunas na tabela. Isso representa o comprimento do array nomesColunas

`int numeroLinhas`: Um inteiro que indica o número de linhas na tabela. 

`int *tiposColunas`: Um ponteiro para um array de inteiros (int *) que armazena os tipos de dados associados a cada coluna.

A ideia desse projeto é usar essa estrutura para as operações com as tabelas, onde todas ficam armazenadas na variavel `todasTabelas` que é utilizada por todo código.

Além das funcoes requeridas implementamos a opção de editar um valor de uma coluna em uma tabela, para em caso de algum erro o usuario não prescisa deletar a linha e criar outra. 


***


## Dependências

O projeto depende dos seguintes cabeçalhos padrão da linguagem C e de seus próprios módulos:

```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include "criacao.h"
#include "edicao.h"
#include "exclusao.h"
#include "visualizacao.h"
```

## Outras Funções
- criarTabela: Permite ao usuário criar uma nova tabela especificando seu nome, colunas e valores iniciais.
- mostarTodas: Lista todas as tabelas existentes.
- criarLinha: Permite ao usuário adicionar uma nova linha (registro) a uma tabela existente.
- mostrarTabela: Exibe os conteúdos de uma tabela específica.
- pesquisaValor: Pesquisa e compara um valor em um coluna de uma tabela.
- editarValorTabela: Permite ao usuário editar o valor de uma coluna em uma tabela.
- deletarLinha: Permite ao usuário apagar uma linha específica de uma tabela.
- deletarTabela: Permite ao usuário apagar uma tabela existente.

## Contribuição
o Projeto foi feito por Dinorah Farias e Flawbert Lorran, com a seguinte divisão por modulos:

### Dinorah
* criacao
* estruturas
* visualizacao

### Flawbert
* edicao
* exclusao


***


## Compilação e execução
