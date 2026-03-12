## Anotações livro linux eficiente na linha de comando
#### **_Pag 34._** 
Sempre que um comando é executado existem etapas que são de responsabilidade do comando e outras do shell. Por exemplo os pipes e coringas(*)

#### **_Pag 47._**
Um barra invertida antes do alias escapa o alias, fazendo o shell procurar um comando com o mesmo nome, ignorando qualuqer sombreamento. Ex: `\less` <arquivo> ->  executa o comando less e não o alias.

#### **_Pag 49._**
Quando o shell procura um comando pelo nome, ele verifica se esse nome é um alias antes de verificar o caminho de pesquisa. É pro isso que um alias pode sombrear (ter procedencia sobre) um comando de mesmo nome.

#### **_Pag 60._**
__Verifique__. Antes de executar `rm`, execute `ls` com padrão desejado para ver quais arquivos são encontrados.
```
$ ls *txt
a.txt   b.txt   c.txt
```
__Exclua__. Se `ls` parece correta. Execute `rm !$` para excluir os mesmos arquivos que foram encontrados:
```
$ rm !$
$ rm *txt
```
`!$` Para todos os argumentos digitados no comando anterior.

#### **_Pag 61._**
Busca incremental com histórico de comandos.
Para resgatar a string mais recente que foi executada preciosne `CTRL+R` duas vezes seguidas.
`CTRL+J` para interromper uma busca incremental e contunuar trabalhando no comando local.

#### **_Pag 64._**
Para coreção de comando digitado erroneamente, por exemplo:
```
$ md5sum *.jg
md5sum '*.jg': No such file or directory
```
Basta digitar o texto anterior (errado), o novo texto (corrigido) e um par de circinflexos (^), desta forma:
```
$ ^jg^jpg
```
Pressione enter e o comando correto aparecerá e será executado. Se o comando original tiver mais de uma ocorrência, apenas a primeira palavra será alterada.

#### **_Pag 65._**
O shell pode usar a mesma sintaxe do sed para substituição de comando. Procure um comando com `!!`
```
$ !!:s/jg/jpg/
```

Você pode começar com expansão de histórico que quiser como md5sum
```
$ !md5sum:s/jg/jpg
```
Irá encontrar o comando mais recente com `md5sum` e fará a substituição de jg para jpg.

#### **_Pag 65._**
O padrão de shell é a edição no estilo EMACS.

A tela META do Emacs é escape (pressiona e solta) ou `ALT` (presiona e mantida assim).

Edição no estivo VIM:
```
$ set -o vi
```
Edição no estivo Emacs:
```
$ set -o emacs
```
#### **_Pag 66._**
| Ação  | Emacs |
| ------------- |:-------------:|
| Movimenta um catactere para frente      | Ctrl-f     |
| Movimenta um catactere para trás      | Ctrl-b     |
| Movimenta uma palavra para frente      | Meta-f     |
| Movimenta uma palavra para trás      | Meta-b     |
| Move para o fim da linha      | Ctrl-a     |
| Move para o fim da linha      | Ctrl-e     |
| Troca a posição de dois caracteres      | Ctrl-t     |
| Troca a posição de duas palavras      | Meta-t     |
| Coloca a primeira letra da próxima pavalra em maiúscula      | Meta-c     |
| Coloca a próxiama palavra inteira em minúscula      | Meta-u     |Ctrl-
| Coloca a próxiama palavra inteira em minúscula      | Meta-l     |
| Excluí um catactere da frente      | Ctrl-d     |
| Excluí um catactere de trás      | Ctrl-h     |
| Excluí uma palavra da frente      | Meta-d     |
| Excluí uma palavra de trás      | Ctrl-w     |
| Remove do cursor ao início da linha      | Ctrl-u     |
| Remove do cursor ao fim da linha      | Ctrl-k     |
| Exclui a linha inteira      | Ctrl-e Ctrl-u     |
| Cola o texto excluído      | Ctrl-y     |
| Desfaz a operação de edição anterior      | Ctrl-_     |
| Desfaz todas as edições feitas até agora      | Meta-r     |