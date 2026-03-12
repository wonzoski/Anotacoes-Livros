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
