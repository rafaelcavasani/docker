# WireMock

## Como rodar
`docker-compose up -d`

## Como fazer as chamadas
O wiremock irá subir um servidor na porta 8081 da sua maquina.
Basta fazer a chamada para `http://localhost:8081/<caminho_mapeado>`.

Os caminhos ficam mapeados na pasta `stubs/mappings`, em cada arquivo é definido uma requisição com a URI, parâmetros e corpo da chamada.

Os retornos das chamadas estão na pasta `stubs/__files` e são indicadas no campo `bodyFileName` de cada mapeamento das requisições.

A requisição deve ser montada de acordo com o atributo `request` do mapeamento.
