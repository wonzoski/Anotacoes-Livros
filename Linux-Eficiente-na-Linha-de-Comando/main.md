Anotações livro linux eficiente na linha de comando

Pag 34.
    Sempre que um comando é executado existem etapas que são de responsabilidade do comando e outras do shell. Por exemplo os pipes e coringas(*)

Pag 47.
    Um barra invertida antes do alias escapa o alias, fazendo o shell procurar um comando com o mesmo nome, ignorando qualuqer sombreamento.

    Ex: \less <arquivo> ->  executa o comando less e não o alias.

Pag 49.
    Quando o shell procura um comando pelo nome, ele verifica se esse nome é um alias antes de verificar o caminho de pesquisa. É pro isso que um alias pode sombrear (ter procedencia sobre) um comando de mesmo nome.

Pag 60.
    1. Verifique. Antes de executar <rm>, execute ls com padrão desejado para ver quais arquivos são encontrados.
    $ ls *txt
    a.txt   b.txt   c.txt

    2. Exclua. Se a saa de ls parece correta. Execute <rm !$> para excluir os mesmos arquivos que foram encontrados:
    $ rm !$
    rm *txt

    !$  ->  Para todos os argumentos digitados no comando anterior.

Pag 61.
    Busca incremental com histórico de comandos.
    - Para resgatar a string mais recente que foi executada preciosne (CTRL+R) duas vezes seguidas.
    - (CTRL+J) para interromper uma busca incremental e contunuar trabalhando no comando local.