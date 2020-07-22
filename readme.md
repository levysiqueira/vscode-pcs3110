# Sintaxe de PCS3110 para o VSCode

### EPUSP - [PCS3110 - Algoritmos e Estruturas de Dados para a Engenharia Elétrica](https://uspdigital.usp.br/jupiterweb/obterDisciplina?sgldis=pcs3110)

#### Prof. Dr. Fábio Levy Siqueira

Este projeto permite que as [palavras reservadas de PCS3110](Pseudocodigo-v04.pdf) - baseada na linguagem usada pelo livro do Cormen, Leiserson, Rivest e Stein (2009) - sejam reconhecidas no VSCode. Com isso são disponíveis as seguintes *features*:

- Reconhecimento das palavras reservadas de PCS3110 (*syntax highlighting*).
- Possibilidade de usar símbolos matemáticos no código (usando o plugin [Prettify Symbols Mode](https://marketplace.visualstudio.com/items?itemName=siegebell.prettify-symbols-mode).

Note que este projeto **NÃO** compila o código, sugere comandos ou verifica a sintaxe. Ele apenas realça as palavras reservadas.

## Tutorial para usar o projeto
1. [Instale o VSCode](https://code.visualstudio.com/)
2. [Adicione o plugin Prettify Symbols Mode](https://marketplace.visualstudio.com/items?itemName=siegebell.prettify-symbols-mode)
3. Copie a pasta "pcs3110" ([o arquivo plugin.zip possui a pasta](plugin.zip)) para a pasta dos plugins do VSCode (no Windows é a pasta %USERPROFILE%\\.vscode\extensions
4. Vá em *Settings* (Ctrl + ,) -> *Extensions* -> *Prettify symbols mode* e escolha *Edit in settings.json* em *Prettify Symbols Mode: Substitutions*
![Editar settings.json](/images/plugin.png)
5. No final do arquivo haverá uma sequência "}", "]" e "}" como mostrado abaixo
![Local da edição](/images/local.png)
6. Depois do "}" antes do "]" (indicado acima) coloque uma vírgula (,) e copie o conteúdo de [settings.json](settings.json), resultado como mostrado abaixo
![Resultado da edição settings.json](/images/resultado.png)
7. Salve o arquivo e o reinicie o VSCode
8. Teste usando o [exemplo.pcs](/exemplo/exemplo.pcs)


## Atalhos para símbolos
Estão disponíveis os seguintes atalhos para símbolos.

Texto | Resultado
----------|----------
-> | →
\\inf | ∞
\\sqrt | √
\>= | ≥
<= | ≤
\\alpha | α
\\beta | β
\\gamma | γ
\\delta | δ
\\forall | ∀
\\exists | ∃
\\in | ∈
\\notin | ∉
\\empty | ∅
\\subseteq | ⊆
\\subset | ⊂
\\union | ⋃
\\intersect | ⋂
\\lceil | ⌈
\\rceil | ⌉
\\lfloor | ⌊
\\rfloor | ⌋

## Bugs
Ao inserir um símbolo, o cursor fica antes do símbolo (apesar de estar depois dele). Isso é uma questão do plugin *Prettify Symbols Mode*.

Caso haja algum problema de implementação, abra uma Issue no GitHub ou faça um Pull request. Qualquer coisa entre em contato comigo (fabio@levysiqueira.com.br).