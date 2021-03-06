# Anything
## Introdução
### Propósito do documento de requisitos 
O documento de visão define o escopo de alto nível e o propósito de um programa, produto ou projeto. Uma instrução clara do problema, solução proposta e os recursos de alto nível do produto ajudam a estabelecer expectativas e a reduzir riscos. Este tópico fornece uma estrutura de tópicos de conteúdo potencial para o documento de visão.
Consulte Desenvolvendo uma Visão para obter uma explicação de como o proprietário do produto ou o analista de negócios trabalha com as partes interessadas para desenvolver um documento de visão. Este tópico, que faz parte da orientação do cenário Collaborative Lifecycle Management, descreve o processo do desenvolvimento da visão. Este tópico descreve o conteúdo típico para o documento. É possível copiar esta estrutura de tópicos e colá-la em um novo documento, e usá-la como a base para seu documento de visão. Use as partes desta estrutura de tópicos que são relevantes para seu projeto.

### Escopo do produto 
O sistema a ser desenvolvido será composto seguindo padrões de modelo web para exibição e compra de produtos on-line. Ele será basicamente um E-COMMERCE que venderá produtos fabricados e produzidos por pequenos produtores da região do Seridó no Rio Grande do Norte, pensando em divulgar assim os produtos locais para o Brasil e o mundo.

## Descrição geral
### Requisitos funcionais
|  CÓD 	|   REQUISITO	| DESCRIÇÃO | DETALHAMENTO |  PRIORIDADE
|---	|---	|---  |--- | --- |
|  RF001 	|  Cadastro de Produtos | No RF001 será possivel realizar o cadastro de todos os produtos, como também a atualização, remoção e pesquisar todos os produtos cadastrados | codigo, nome, preço, tipo do produto, detalhes do produto (quantidade, tamanho e cor dos produtos) | Alta |
| RF002 | Cadastro de Clientes | Para o cliente poder fazer uma compra ele tem que ser cadastrado no sistema, o CPF será a PK da tabela, será coletado também o e-mail do cliente, para poder enviar algumas informações, como cupons de desconto, promoções, entre outras coisas, vai ser possivel realizar também atualização dos dados de cadastro, fazer o delete e pesquisar todos os clientes cadastrados  | CPF, nome completo, data de nascimento, e-mail e telefone.  | Alta |
| RF003 | Cadastro de Cidades | No cadastro de cidades será obrigatório o preenchimento das informações referente as cidades  | nome e estado | Média | 
| RF004 | Cadastro de Vendedores | Os vendedores serão os interessados por vender na plataforma, é possivel realizar cadastro dos vendedores, a atualização dos dados, como também a remoção e pesquisa dos mesmos, os vendedores podem cadastrar um produto e referenciar a ele mesmo | CPF, nome completo, data de nascimento, endereço (rua, bairro, CEP, cidade) e-mail e telefone. | Alta |
| RF005 | Realização de Vendas  | O sistema permitirá fazer vendas condicionais gerando código para os mesmos, que posteriormente podem ser recuperados e passarem para venda fechada. |  | Alta |
| RF006 | Realização de Vendas  | Em qualquer tipo de venda será obrigatório o preenchimento do cliente que está realizando a compra, o vendedor e o tipo da venda. |  | Alta |
| RF007 | Realização de Vendas  | No momento de efetuar alguma venda será necessário selecionar produtos. O sistema permitirá selecionar somente produtos que estejam em estoque e disponíveis para venda e a quantidade disponível em estoque. | | Alta |
| RF008| Realização de Vendas  | Cada venda terá um atributo chamado “tipo_venda”, onde será possível identificar se a venda é um orçamento ou se é uma venda condicional.|  | Alta |
| RF009 | Realização de Vendas  | Para vendas condicionais que não tiverem sido canceladas, será possível recuperá-las para a conferência dos produtos e a mesma poderá ser tornar uma venda fechada. Para fechar essa venda e serem geradas as prestações da mesma, será necessário apenas excluir as mercadorias devolvidas e finalizar com as mercadorias que o cliente quiser ficar.| | Alta |
| RF010 | Realização de Vendas  | Para recuperar alguma venda condicional será necessário informar apenas o CPF do cliente. | | Alta |
| RF011 | Realização de Vendas  | Após qualquer venda ser fechada o valor da venda será agregado ao valor de vendas efetuadas pelo vendedor da venda e será agregado ao valor todal das vendas | | Alta |
| RF012 | Realização de Vendas  | Ao ser finalizada uma venda, o(s) produto(s) vendido(s) deverá(ão) ficar indisponível para a venda e o mesmo será decrementado do valor total de unidades disponíveis. | | Alta |
| RF013 | Cálculo das Parcelas   | O sistema irá gerar automaticamente o valor das parcelas para o vendedor, sendo necessário apenas informar o(s) produto(s), data de vencimento, se será feito com ou sem entrada e o valor da entrada | | Media |
| RF014 | Cálculo das Parcelas  | Será permitido, dentro do valor estipulado para os vendedores, descontos no momento da realização da venda. | | Media |
| RF015 | Controle de Caixa   | Ao ser paga uma prestação por um cliente a mesma entrará como entrada no dia correspondente a efetivação do pagamento.| | Media |
| RF016 | Controle de Caixa | Poderá ser calculado no final de cada dia o lucro da empresa.| | Media |

### Requisitos não-funcionais
|  CÓD 	|   REQUISITO	| DESCRIÇÃO 
|---	|---	|---  |
|RNF001| Geral | O sistema deve ter uma inteface simples e com soluções intuitivas. |
|RNF002| Geral |  As informações serão armazenadas em um Banco de Dados.  |
|RNF003| Acesso ao Sistema |  O sistema poderá ser acessado somente pelo administrador do sistema e pelos vendedores devidamente cadastradas no sistema |
|RNF004|  Acesso ao Sistema | O acesso ao sistema se dará pela informação de usuário e senha |
|RNF005| Permissões do Sistema: Administrador | O administrador do sistema terá acesso à todas as áreas do sistema, com permissão de leitura, exclusão, inclusão e alteração. |
|RNF006| Permissões do Sistema: Vendedores | Permissão para realizar todos os tipos de cadastros, alterações e exclusões nos mesmos |
|RNF007|  Permissões do Sistema: Vendedores | Permissão para realizar vendas condicionais tanto de clientes da loja como dos vendedores externas |
|RNF008|  Permissões do Sistema: Vendedores | Permissão para efetuar pagamentos de prestações de clientes|
|RNF009|  Permissões do Sistema: Vendedores | Permissão para consultar produtos e seu estoque|
|RNF010|  Permissões do Sistema: Vendedores |Não tem permissão para fazer nenhum tipo de consulta referentes as vendas da empresa, vendas dos vendedores, das comissões e ao caixa|
|RNF011|  Permissões do Sistema: Vendedores | Não é permitido fazer nenhum tipo de lançamento no caixa|
|RNF012|  Permissões do Sistema: Vendedores | Permissão para concluir vendas no sistema|
|RNF013|  Portabilidade |O sistema deve executar em sistemas operacionais Linux, Windows, Android ou IOS mediante uso de navegador de internet.|

### Perfis dos usuários
|| Administrador - responsavel por fazer todas as funções no sistema

|| Usuario - o usuario pode fazer pesquisas dos produtos, fazer compras e alterar o proprio cadastro

|| Vendedores - ( se virar marketplace o vendedor seria as pessoas interessadas em vender alguma coisa na plataforma)

|| e-commerce - efetua as vendas, calcula frete, organiza descontos

### Riscos
|  DATA  	|   RISCO	|  PRIORIDADE | STATUS |   PROVIDÊNCIA/SOLUÇÃO 
|---	    |---	    |---          |------  |----
| 17/09/2020 | Não aprendizado das ferramentas utilizadas pelos componentes do grupo a tempo | Alta | Todos | Vigente |  Reforçar estudos sobre as ferramentas e receber apoio dos integrantes que dominam o mesmo | 
| 17/09/2020 |  Divisão de tarefas mal sucedida | Baixa | Gerente | Vigente |  Acompanhar o desenvolvimento de cada membro da equipe e estimar tempo necessário para conclusão das tarefas |
| 17/09/2020 |  Implementação de protótipo com as tecnologias escolhidas pela equipe | Alta | Todos | Vigente |  Buscar tutoriais e a documentação das tecnologias para implementar os primeiros casos |



### Suposições e dependências
A seguir será classificado as suposições presentes no desenvolvimento do projeto, teremos como base a análise de acontecimentos internos e externos, que podem influenciar no andamento do mesmo e que servem de base para o acompanhamento e melhor tomada de decisão do gerente e da divisão de tarefas da equipe de analistas.
1. Tempo
* Estimar o tempo gasto necessário para conclusão do projeto até o dia da apresentação final no componente curricular e ter atingido a última iteração com sucesso dentro do prazo estabelecido pelo cliente (Docente);
2. Recursos 
* Delegar tarefas para não sobrecarregar membros da equipe e fazer reuniões periódicas para acompanhamento do projeto e propor as novas metas a serem alcançadas;
3. Design e desenvolvimento
* Escolher bem o layout, com base na preferência do cliente, e utilizar as melhores estratégias que as
ferramentas de desenvolvimento tenha a oferecer;
4. Tecnologia
* Aprimorar os conhecimentos na tecnologia escolhida e buscar produtividade com maior rapidez, pois de acordo com a complexidade dos módulos do sistema, a equipe deve estar com o domínio da documentação da linguagem utilizada para melhor suporte e discussão;
5. Qualidade
* Passar confiança para o cliente (Docente), tanto na parte de segurança dos dados até a implementação de uma interface rápida e intuitiva.

A determinação de dependências implica na sequência da execução das atividades e da lógica do negócio. Por isso alguns fatores devem ser discutidos na reunião com o cliente (Docente) para definição de prioridade dos módulos e da interligação existente entre eles. Será listado as principais dependências e como será feito a análise por parte da gerência para a estratégia de andamento do projeto.
1. Dependências obrigatórias
* Seguir o modelo conceitual definido pelo contrato, analisar bem os requisitos e as regras de negócio para não entregar um projeto paralelo e que não cumpra com o pré-estabelecido;
2. Dependências arbitradas
* Uma iteração, dependendo do caso, terá que ser iniciado após a conclusão da anterior;
3. Dependências externas
* Montar um cronograma para as atividades desenvolvidas no projeto, tendo em vista o cumprimento de outros projetos e avaliações em componentes curriculares diferentes;
4. Dependências internas
* Ficar atento às regras de negócios e definir bem a cláusula para quando houver solicitação de alteração da lógica de negócio por parte do cliente.

# Perspectiva do produto
A perspectiva geral do projeto Anything é promover uma plataforma online de venda de produtos, onde os usuários (que são os clientes do serviço) podem consultar produtos e verificar a disponibilidade de estoque para efetuar a compra, dependendo da disponibilidade, o cliente poderá fazer suas compras tranquilamente. Já no perfil de administrador (responsável pelo gerenciamento do serviço), tem acesso a lista de usuários e manutenção dos perfis de fornecedores dos produtos, onde estará sendo anexado na base de dados do sistema, permitindo a consulta por parte do usuário e o interesse de efetuar os pedidos.

O intuito do projeto é promover uma plataforma fluida e fácil de operar, e buscar uma solução viável de rápido acesso, através da internet, para um ramo que movimenta boa parte dos negócios na região e valorizar o comércio local para divulgar para outras regiões e até pro mundo inteiro.


