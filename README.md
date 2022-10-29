
## Resumo CSS - Casvating Style Sheets

#### O que é possível criar com CSS:

* Layout e estilização de páginas web;
* Animações;
* Formas geométricas e desenhos;
* Filtros;
* Contadores;

#### Propriedade e valor
~~~css
propriedade: valor;
Exemplo:
color: white;
~~~

#### CSS inline
Adicionando o código CSS utilizando o atributo **style** dentro das tags HTML, elemento por elemento.
_Exemplo:_
~~~html
<h1 style="background: red; color: white;">CSS in line</h1>
<h2 style="color: red;">Trilha CSS</h2>
~~~
#### CSS Interno:
Código CSS fica dentro da tag <'head'> da página html com a tag <'style'>.
_Exemplo:_
~~~html
<head>
    ...
    <style>
        h1{
            background-color: blueviolet;
            color: azure;
        }
        h2{
            color: blueviolet;
        }
    </style>

</head>
~~~

#### CSS Externo
Um arquivo externo com extensão .css com todas as regras de estilo que queremos utilizar com uso da tag <'link'> dentro do <'head'> do html.

  * **O CSS externo é o melhor pelos motivos abaixo:**
    * Carregamento da página fica mais rápido;
    * Código fica organizado;
    * Manutenção no código é mais prática devido a organização;
    * Estilos podem ser reutilizados em várias página;

_Exemplo:_
~~~html
 <link rel="stylesheet" href="style.css">
~~~
#### Depurando CSS
Utilizado para identificar problemas no código, através do **Dev Tools**.
* **Atalhos para acessar Dev Tools**
  * Clicar com botão direito do mouse e inspecionar;
  * CTRL + SHIFT + I;
  * CTRL + SHIFT + C;
  * F12;

#### Seletores CSS
* Seletor por **TAG** HTML, especificando a tag;
    ~~~css
    h1{
        background-color: blueviolet;
        color: azure;
    };
    ~~~
* Seletor por **ID** (**#**): Seleciona o id específico;
    ~~~css
        #nome-id {
            color: red;
        }
    ~~~
* Seletor por **Classe** (**.**): Seleciona a classe específica.
    ~~~css
        .nome-classe {
            color: red;
        }
    ~~~
* Seletor **Universal** (**' * '**): Seleciona todos os elementos do HTML;
    ~~~css
        * {
            color: red;
        }
    ~~~
* Seletor de **Atributo** (**[atributo]**) ou (**[atributo="valor"]**): Seleciona elementos que possuem um atributo específico em nosso documento HTML e conseguimos também buscar atributos com um valor específico;
    ~~~CSS
        [title] {
            color: red;
        }/*Vai selecionar todos os elementos que tiverem o atributo "title"*/

        OU

        [title="Netflix"] {
            color: red;
        }/*Vai selecionar todos os elementos que tiverem o atributo "title" e mais o valor "entre aspas", valor EXATO.*/

        OU

        [title~="Net"] {
            color: red;
        }/*Vai selecionar todos os elementos que tiverem o atributo "title" e mais o valor "entre aspas", neste caso busca parte do valor, não necessitar ser idêntico.*/

        OU

        [title|="Net"] {
            color: red;
        }/*Vai selecionar todos os elementos que tiverem o atributo "title" e mais o valor "entre aspas" imediatamente seguido de um hífen.*/

        OU

        PREFIXO
        [title^="Net"] {
            color: red;
        }/*Vai selecionar todos os elementos que tiverem o atributo "title" e que COMECE com o valor entre aspas.*/

        SUFIXO
        [title$="Net"] {
            color: red;
        }/*Vai selecionar todos os elementos que tiverem o atributo "title" e que TERMINE com o valor entre aspas.*/

        ALL
        [title*$*="Net"] {
            color: red;
        }/*Vai selecionar todos os elementos que tiverem o atributo "title" e que CONTENHAM em qualquer parte o valor entre aspas.*/
    ~~~

#### Agurpamento de Seletores
Podemos utilizar as características do CSS simultaneamente em tags, classe, id e atributo, bastando colocar todos separados por **vírgula**, conforme exemplo abaixo:
~~~css
.classe, #id, [atributo]{
    color: red;
  }
  /*Neste caso aplico em todos os elementos a mesma característica*/
~~~

Para Afunilar este filtro e utilizar mais de um elemnto por exemplo podemos filtrat por classe e tag p, basta não ter nem vírgula nem espaço entre os elementos:
~~~css
p.classe#id{
    color: red;
  }
~~~
#### Combinadores
##### * Descendente
##### Filho
Seleciona **apenas** os filhos diretos do seletor, utilizando o sinal de **>**, conforme exemplo:
~~~css
div > p{
    color: red;
  }
~~~

