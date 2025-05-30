﻿# DesafioConversoMoeda
Este projeto foi desenvolvido como desafio do curso da Alura para praticar o uso de APIs, manipulação de dados externos e estruturação de um projeto Java voltado para conversão de moedas. O objetivo principal foi permitir que o usuário selecione pares de moedas, informe um valor, e obtenha a conversão em tempo real utilizando a API v6.exchangerate-api.

FUNCIONALIDADES:
Menu interativo no console com 6 opções de conversão de moeda.

Entrada do valor a ser convertido feita pelo usuário.

Consulta à ExchangeRate API em tempo real.

Exibição do resultado convertido com base na taxa atual.

Encapsulamento da lógica de chamada de API, menu e formatação de resposta.

Validação de entrada e controle de fluxo.

TECNOLOGIAS USADAS:
Java 17

API HTTP nativa (HttpClient)

Gson (para desserializar JSON)

Java Records (estrutura de dados imutável para representar a resposta da API)

Map.of() para estruturar pares de moedas

DESAFIOS ENCONTRADOS:
Compreensão da estrutura da resposta da API: A API retorna todas as taxas de conversão a partir de uma moeda base. Inicialmente, parecia necessário fazer duas requisições — uma para cada moeda —, mas depois compreendi que bastava uma única chamada e acessar o valor da moeda destino diretamente.

Modelagem da estrutura da resposta da API com record: Foi necessário ajustar o record da resposta para trabalhar com um Map<String, Double> em vez de campos fixos como USD, EUR, etc., permitindo maior flexibilidade para acessar moedas de forma dinâmica.

Construção do menu e entrada do usuário: Para permitir a escolha de pares de moedas sem usar estruturas muito repetitivas ou difíceis de manter, utilizei um Map<Integer, String[]> (semelhante a um dicionário em outras linguagens) para armazenar e acessar os pares com base na escolha do usuário.

Tratamento de erros e validações: Implementei verificações para opções inválidas no menu, controle de saída e possíveis falhas na comunicação com a API.

 Licença
Este projeto é apenas para fins educacionais, como parte dos cursos da Alura.
