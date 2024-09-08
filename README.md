# traducaoAutomatica
Atividade: Tradução Automática - Pedro Silva

1. Tente valores diferentes do argumento num_examples na funçãoload_data_nmt. Como isso afeta os tamanhos do vocabulário do idioma de origem e do idioma de destino?

Após testar valores diferentes no argumento, foi possível perceber que isso impacta diretamente os tamanhos dos vocabulários do idioma de origem e do idioma de destino. Quando num_examples é definido com um valor menor, o vocabulário resultante tende a ser menor, pois menos frases são consideradas para a construção do vocabulário. Isso pode resultar em uma maior quantidade de palavras não vistas se o modelo for aplicado a um conjunto de dados maior, o que pode prejudicar a qualidade da tradução. Por outro lado, ao aumentar num_examples, o vocabulário geralmente se expande, incluindo mais palavras. Embora isso possa melhorar a capacidade do modelo de lidar com uma variedade maior de frases, também pode aumentar a complexidade do modelo, além de potencialmente incluir palavras que podem não ser úteis para a tradução.

2. O texto em alguns idiomas, como chinês e japonês, não tem indicadores de limite de palavras (por exemplo, espaço). A tokenização em nível de palavra ainda é uma boa ideia para esses casos? Por que ou por que não?

A tokenização em nível de palavra não seria a abordagem mais eficaz. Isso ocorre porque a falta de espaços torna difícil identificar onde uma palavra termina e outra começa, resultando em possíveis erros de segmentação. Em vez disso, métodos alternativos, como a tokenização baseada em caracteres ou algoritmos de segmentação de palavras, são mais adequados, pois ajudam a identificar palavras com base em padrões de caracteres e frequências. Além disso, técnicas de subpalavras, como Byte Pair Encoding (BPE) ou WordPiece, são eficazes nesses casos, permitindo que o modelo aprenda representações significativas a partir de combinações de caracteres, melhorando assim a qualidade da tradução.
