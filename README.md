# imersao-alura-gemini
Chatbot de Triagem para Sintomas Depressivos

Olá! 👋 Este projeto é um chatbot de triagem para sintomas depressivos, desenvolvido durante a Imersão Alura/Google Gemini. O objetivo é mostrar como a lógica de programação pode ser aplicada na área da saúde mental, com a possibilidade futura de integrar modelos de linguagem como o Gemini para melhorar a interação e a análise de dados.

CONTEXTO E MOTIVAÇÃO:

Com experiência em programação e formação em psicologia e psicometria, percebo a importância de ferramentas acessíveis para uma primeira avaliação de saúde mental. Este chatbot é um passo inicial na criação de soluções digitais que podem ajudar a identificar pessoas que precisam de avaliação profissional. A estrutura das perguntas e a forma de avaliar foram baseadas em ferramentas de avaliação com reconhecimento científico, como o SCID-5-RV, o BDI-II e o PHQ-9. A ideia foi usar a lógica dessas ferramentas de um jeito mais simples.

FUNÇÃO:

Avisa: Informa que ele não dá diagnóstico e que é importante procurar um profissional se houver preocupações.
Pergunta: Faz uma série de perguntas sobre sintomas depressivos, seguindo um pouco o modelo de instrumentos como SCID-5-RV, BDI-II e PHQ-9.
Valida: Só aceita "sim" ou "não" como resposta.
Conta: Soma quantas respostas foram "sim".
Verifica: Observa se houve resposta "sim" para as perguntas chave sobre humor deprimido (A1) ou perda de interesse (A2).
Identifica: Vê se a pessoa respondeu "sim" à pergunta sobre pensamentos de morte ou auto lesão (A9).
Resulta: Apresenta uma interpretação inicial com base na pontuação e nas respostas das perguntas chave e sobre ideação suicida, com sugestões sobre o que fazer.

ESTRUTURA (o código tem três partes principais):

1. obter_resposta_sim_nao(pergunta):
Recebe a pergunta a ser feita.
Usa um loop para continuar perguntando até que a pessoa responda "sim" ou "não" (a resposta é convertida para minúsculo e espaços extras são removidos).
Retorna True para "sim" e False para "não".
Se a resposta for diferente, avisa e pergunta novamente.

2.chatbot_depressao_triagem():
Inicia a contagem de pontos e o número de perguntas.
Mostra as mensagens de aviso e introdução.
Define um dicionário perguntas_sintomas com as perguntas e códigos (como "A1"). As perguntas foram elaboradas considerando itens comuns em escalas de depressão.
Passa por cada pergunta:
Exibe a pergunta numerada.
Usa a função obter_resposta_sim_nao() para obter a resposta.
Aumenta a pontuação se a resposta for "sim".
Guarda todas as respostas em um dicionário respostas_sintomas.
Verifica se as respostas para as perguntas chave (A1 e A2) e a de ideação suicida (A9) foram "sim".
Retorna a pontuação, o número de perguntas e se houve "sim" nas perguntas importantes.

3. Execução do chatbot e interpretação dos resultados:
O programa principal executa o chatbot_depressao_triagem() e, com base nos resultados, mostra uma interpretação inicial, enfatizando a necessidade de procurar ajuda profissional, especialmente em casos de ideação suicida ou alta pontuação com sintomas chave presentes.

IDEIAS FUTURAS (este é um protótipo básico, mas há várias formas de melhorar com o Gemini):

Análise de respostas mais ricas: Em vez de só "sim" ou "não", o Gemini poderia entender respostas mais elaboradas.
Perguntas personalizadas: O Gemini poderia adaptar as perguntas com base nas respostas anteriores.
Recomendações mais específicas: Com a análise do Gemini, as recomendações de ajuda poderiam ser mais detalhadas.
Análise de sentimentos: O Gemini poderia identificar o tom emocional nas respostas.
Integração com conhecimento: O Gemini poderia acessar informações sobre saúde mental para fornecer dados mais completos.

RELEVÂNCIA:

Aplica lógica de programação em uma área importante: Mostra o uso da tecnologia na saúde mental.
Considera bases da avaliação psicológica: A estrutura tem relação com instrumentos científicos.
Abre caminho para o uso do Gemini: Apresenta um caso de uso para IA na análise e interação em saúde mental.
É um projeto claro e fácil de entender.
Tem potencial para ajudar pessoas a buscar ajuda.

CONSIDERAÇÕES:

É fundamental lembrar que este chatbot é uma ferramenta de triagem inicial e não substitui a avaliação de um profissional de saúde mental que utiliza instrumentos padronizados como SCID-5-RV, BDI-II ou PHQ-9. O desenvolvimento de tecnologias em saúde mental exige cuidado, responsabilidade e ética para garantir o bem-estar dos usuários. Qualquer desenvolvimento futuro deve envolver profissionais da área e especialistas em ética de IA.

Agradeço a atenção!
