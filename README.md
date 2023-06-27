# Raspagem_links_MercadoLivre
Um script feito com BeatifulSoup que busca alguma informações de anúncios do Mercado Livre, inicialmente feito para uma concessionária para comparar os preços dos concorrentes.

Inicialmente o código foi feito para comparar os preços de peças automotivas de vendedores oficiais da Volkswagem. O primeiro script faz a busca dos produtos baseado no que o usúario procura, e retorna um arquivo de texto com os links.

O segundo script entra em cada link e salva as informações em outro arquivo txt, a partir daí é só abrir o excell e ver os resultados.



#Como vai funcionar meu programa?

1 - Preparar uma listra com links que o programa vai ler, no caso basta pegar uma lista de sku e ir ubstituindo a parte correspondente do texto

2 - O programa vai pegar o primeiro link, acessa-lo e pegar todos os links do anúncios assim como as guestões de pesquisa, vai pular para a proxima página e repetir a operação,
    quando não houver mais páginas, o programa deve trocar de link e repetir o processo

3 - Todos os links serão salvos em um arquivo de texto próprio

---------------- 2º PARTE (Coleta de Dados - Full Soup)---------------------

4 - Ao terminar de obter todos os links, o prorama fará uma nova raspagem, dessa vez irá acessar o arquivo de texto contendo os links salvos na iteração anteriror.
ao acessar CADA UM dos links, salvaremos os atributos das informações que queremos, sendo eles: TÍTULO, PREÇO, SEM JUROS?, QUANTIDADES DE ITENS VENDIDAS, MARCA, SKU DESCRIÇÃO, LOJA

5 - Salvamos as informações em um arquivo de texto, separando as informações do item com um ; e pulando uma linha para o próximo item
