🌾 Chatbot Agritec (v5.2 - Estável e Integrado com Gemini)

O projeto Chatbot Agritec tem como objetivo oferecer suporte prático e inteligente a agricultores, integrando informações oficiais de diversas APIs da Embrapa (como Agritec, ClimAPI, Agrofit e RespondeAgro) a um assistente conversacional avançado, utilizando o modelo Gemini 2.5 Flash para processamento final da resposta.

A versão atual (v5.2 - Estável e Integrado com Gemini) representa um salto na capacidade de resposta e utilidade do assistente.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

✨ Destaques da Versão v5.2

• Processamento de Resposta com Gemini:

- O Gemini 2.5 Flash é usado para summarizar dados brutos das APIs, traduzir termos técnicos (ex: códigos climáticos e agronômicos) e suprimir a repetição de tabelas longas e complexas, garantindo uma resposta final concisa, clara e profissional.

- Implementação de Lógica de Autonomia: O Gemini é instruído a usar seu conhecimento geral sobre o tema AGRO quando as APIs da Embrapa não retornam dados específicos para a consulta (e.g., uma cultura muito específica).

• Integração de Múltiplas Bases de Dados (APIs Embrapa):

- AGRITEC v2: Consultas a endpoints essenciais como Zoneamento Agrícola (época de plantio ideal por risco, tipo de solo e município), Cultivares recomendadas por UF, e Produtividade (estimativa baseada em data de plantio e cultivar de referência).

- CLIMAPI v1: Consulta de dados climáticos (temperatura, precipitação, umidade) por cidade, usando geocodificação para obter as coordenadas.

- AGROFIT v1: Pesquisa de produtos formulados (defensivos) por marca comercial e busca de defensivos específicos para pragas/doenças (utilizando nome científico).

- RespondeAgro v1: O principal fallback de busca para perguntas gerais, utilizando a base de conhecimento de publicações da Embrapa.

- SmartSolos v1: Inclusão de um endpoint de demonstração para classificação de solos. (WORK IN PROGRESS)

• Melhoria na Interpretação (PLN):

- Uso do spaCy e expressões regulares para identificar a intenção do usuário (zoneamento, clima, defensivo, praga) e extrair entidades cruciais (cultura, UF, município, data de plantio).

- Lógica de validação geográfica aprimorada que direciona corretamente a consulta para a API Agritec ou aciona o fallback RespondeAgro quando falta uma localização.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

🚀 Próximos Passos e Metas de Desenvolvimento

O foco de desenvolvimento futuro do Chatbot Agritec está em expandir sua acessibilidade e profundidade de consultas, com as seguintes metas definidas:

• Versão v6.0 (Próxima Etapa):

- Integração com o Telegram ou outro serviço de mensagem para ampliar o alcance e a usabilidade da ferramenta.

• Versão v7.0 (Futuro):

- Expansão das Consultas com mais parâmetros da Agritec (e.g., recomendações de adubação e correção de solo).

- Melhoria da Interpretação de Linguagem Natural, tornando o assistente mais flexível e próximo de um assistente real.

O objetivo final é disponibilizar uma ferramenta de assistência digital acessível, que utilize dados oficiais e IA para auxiliar produtores na tomada de decisão agrícola.
