# Exercícios de JavaScript
Nestes exercícios, vamos usar um case prático de um formulário de contatos simples para explorar algumas capacidades de manipulação do DOM/BOM pelo JavaScript. 

## Exercício 1 - Preparação
Siga as etapas abaixo com atenção:
- Loque-se  com sua conta no [GitHub](https://github.com/);
- Acesse o repositório com os exercícios propostos [clicando aqui](https://github.com/Luferat/JavaScript_DOM_Exercices_01);
- Faça um 'Fork' do repositório em sua conta, clicando no botão [Fork] no canto superior direito da página do repositório;
- Abra o GitHub Desktop e logue-se com sua conta GitHub;
   - Menu `File → Options → "GitHub.com" → [Sign in]`
- Clone o seu repositório na máquina local, preferencialmente na pasta `Documentos\GitHub\...`
  - Menu `File → Clone repository`
- Abra o Visual Studio Code e neste carregue a pasta com o repositório clonado;
  - Menu `File → Open folder...`
- Verifique se a extensão "[Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)" do editor *Ritwick Dey* está instalada;
  - Se não estiver, providencie pelo menu `View → Extensions`...  

## Exercício 2 - Código fornecido
Faça uma cópia de `exercicio_01.html` nomeada `exercicio_02.html`, abrindo-a no VSCode.

*Deixe `exercicio_01.html` intacto para servir de referência para o "case".*

Com a ajuda do instrutor e das referências citadas no próprio código, estude, documente e compreenda cada linha de código, tirando as dúvidas que surgirem.

*Dica: complemente a documentação fornecida com o código usando seu próprio entendimento, isso facilita a aprendizado.*

## Exercício 3 - Funções de Data
Faça uma cópia de **`exercicio_01.html`** nomeada `exercicio_03.html`, abrindo-a no VSCode.

Na sequência, crie, documente e teste uma função `dataAtual()` que retorne a data atual UTC no formado `System Date (AAAA-MM-DD HH:II:SS)`. 

**ATENÇÃO!** A data gerada será armazenada com os dados do formulário, representando assim a data de envio deste e deve estar em [UTC](https://pt.wikipedia.org/wiki/Tempo_Universal_Coordenado) - *Temps Universel Coordonné*.

*Dica: Para esta função usaremos um objeto `Date()` e seu método `toISOString()` para obter um `system date`.*

> Referências: 
> - https://www.w3schools.com/jsref/jsref_toisostring.asp
> - https://www.w3schools.com/js/js_dates.asp


## Exercício 4 - Sanitização

Faça uma cópia de `exercicio_03.html` nomeada `exercicio_04.html`, abrindo-a no VSCode.  

Na sequência, crie, documente e teste uma função `sanitiza(string)` que recebe, trata e retorna a string de parâmetro da seguinte forma:

- Remove qualquer tag HTML da string;

*Dica: use a REGEX `/<[^>]*>?/gm` para identificar tags HTML.*
 - Substitui as quebras de linha dos campos de formulário (`\n`) pela tag `<br>` do HTML;
 
*Dica: use a REGEX `/\n/g` para identificar quebras de linha em strings.*
- Finalmente, remova todos os espaços que ocorrerem no começo e no final da string.
>Referências:
> - https://www.w3schools.com/jsref/jsref_replace.asp
> - https://www.w3schools.com/jsref/jsref_trim_string.asp

## Exercício 5 - Obtendo os campos
Faça uma cópia de `exercicio_04.html` nomeada `exercicio_05.html`, abrindo-a no VSCode.

Na sequência, edite a função `processaContato()` de forma a receber os dados preenchidos no formulário, sanitiza-los e armazená-los em um objeto nomeado `contato{}`, da seguinte forma:
   
    var contato = {
        nome: ...,
        email: ...,
        assunto:...,
        ...
    }
*Dicas: obtenha o valor do campo preenchido usando a função `el()` já existente para ler o atributo `value` deste e a função `sanitiza()`, criada anteriormente, para sanitizar os dados obtidos. Por exemplo: `none: sanitiza(el('#nome').value)`.*
