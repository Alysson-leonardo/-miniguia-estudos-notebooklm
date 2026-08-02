# -miniguia-estudos-notebooklm
Este repositório tem como finalidade instruir a criação de um notebooklm especializado em design de arquitetura e princípios SOLID aplicados a programas TypeScript.

Já o notebooklm em si, possuo o intuito de utilizar como ferramenta de revisão teórica e posteriormente, caso os resultados sejam satisfatórios, como uma base de dados para criar uma MCP capaz de refatorar códigos de acordo com material utilizado.

Materiais utilizados como fonte de dados para a criação do notebooklm:
https://drive.google.com/file/d/1rk0v4oIyCFFHg5JJC9YsiE9YHw8AF2ZT/view?usp=drive_link - exemplos real de código
https://drive.google.com/file/d/152J12mm2esXoxPvWsJYByuv1zIPt8_94/view?usp=drive_link - modelos da estrutura de código
https://www.youtube.com/watch?v=SWgCLOW1bCE - arquitetura de software - canal: fernanda kipper | dev

https://www.youtube.com/watch?v=zcDKQqFmjEA - Clean Architecture - canal: fernanda kipper | dev

https://www.youtube.com/watch?v=jBOLRzjEERk - SOLID aplicado em um código real - canal: rocketseat(com diego como professor)
https://www.youtube.com/watch?v=vAV4Vy4jfkc - princípios SOLID - canal: rocketseat(com diego como professor)

Observação: Caso a fernanda kipper e/ou a rocketseat peçam a remoção dos links desse repositório, farei isso.

Prompts de teste:

# Interferência de contexto
verificar se a IA dá a mesma resposta para o mesmo prompt caso incluirmos pequenos prompts desconexos no meio das duas respostas.
Exemplificação: se eu fizer uma pergunta A e a IA me responder B, após isso vou fazer perguntas que não tem relação com a pergunta A, como se eu tivesse aberto outro chat, e após isso vou fazer a pergunta A de novo e verificar se a IA está misturando o contexto das outras perguntas não correlacionadas para reformular a resposta da pergunta A.

Prompt A: tenho uma clinica veterinária e no momento quero apenas fazer o cadastro e listagem dos animais de estimação
Prompt B: tenho um zoologico e já tenho o código de cadastro e listagem especifico para animais de zoologico, agora gostaria de um codigo para fazer o agendamento de vacinas e exames dos animais.

Conclusões:



<img width="423" height="261" alt="image" src="https://github.com/user-attachments/assets/d34ad590-68d9-4f50-9034-fe4c0b375c7d" />
pdfs: cenário-veterinario e cenário-zoologico

O conteúdo criado com o prompt B não alterou a reposta do prompt A, portanto não houve interferência de contexto e intervenção proativa da IA, apesar de que o conteúdo do prompt B poderia ser reaproveitado no cenário do prompt A. Então a IA não considerou o conteúdo do prompt B e nem fez correlação entre os 2 cenários.

# Definição de papel
verificar se a IA está comprindo o papel que defini no inicio do prompt
exemplificação: quero verificar se a IA via agir de forma objetiva, me entregando apenas o que pedi, sem explicar os conceitos e sem me dizer porque tomou alguma decisão, quero apenas que entregue o código estruturado de acordo com os materias.

contextualização: o notebooklm permite a personalização do chat de conversa para agir da forma que queremos passando um prompt, então o usaremos o seguinte prompt para definir o papel dele:
Responda como um desenvolvedor TypeScript e construa a arquitetura de acordo com o cenário que eu fornecer.
Não pense em implementações futuras, limite-se a criar a estrutura apenas com as entidades, relações e cenários passados.
Não quero explicações do porquê do uso de modelos de design e nem explicação das estrutura ou metódos, limite-se a apenas gerar o código.

Prompt: tenho uma loja de açai e no momento quero registrar, listar e excluir os pedidos

conclusão: A IA entendeu perfeitamente o seu papel e não gerou texto desnecessário para o meu objetivo.

pdf: cenário-açai

# Alucinação e busca fora do domínio
Como o conteúdo é limitado, quero verificar se a IA inventa informação para conseguir entregar uma resposta ou se admite que falta informações. Também quero verificar se a IA tenta buscar fora das fontes que forneci para tentar complementar o conteúdo, porque quero que ela utilize apenas o conteúdo que forneci, mesmo que esteja incompleto.

Prompt: Estou criando uma sistema para uma advocacia, mas não possuo conhecimento em direito e não sei quais deveriam ser os requisitos funcionais a serem levados em consideração. Então crie uma estrutura básica da maneira que achar melhor.

conclusão: eu retirei o comando personalizavel, que definia uma papel claro e objetivo para a IA:
"Responda como um desenvolvedor TypeScript e construa a arquitetura de acordo com o cenário que eu fornecer. Não pense em implementações futuras, limite-se a criar a estrutura apenas com as entidades, relações e cenários passados."

Passando apenas o prompt, a IA apenas gerou um texto informando que poderia realizar as intruções do prompt, mas não os fez.
"Posso utilizar as fontes para orientar a estruturação do seu sistema em camadas independentes, garantindo que as regras de negócio fiquem isoladas de ferramentas externas e frameworks
. Além disso, posso ajudá-lo a implementar os princípios SOLID e padrões de repositório para garantir que o código seja fácil de manter, escalável e testável
"
Então a IA não alucinou e nem buscou conhecimento fora do dómino(exceto nos outros testes de veterinaria e açai, onde ela busco esses conhecimentos do dóminio de comida).
