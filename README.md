# MENTOR: Robô instrutor para o treinamento de novos operadores de máquinas

Trabalho de Interação Humano-Robô (IHR) apresentado ao Centro Universitário FEI, como parte das atividades da disciplina Interação Humano-Robô (CCR230), sob orientação do Prof. Dr. Fagner de Assis Moura Pimentel.

## Componentes do Grupo

- **Lucas Nicolini** — RA: 11.219.047-5
- **Thiago Wuo** — RA: 11.120.266-9

> **Sobre o projeto:** o Mentor é uma proposta conceitual baseada na apresentação do grupo, *Mentor_IHR.pptx*. Os recursos descritos são planejados, não funcionalidades já implementadas. Algumas explicações foram acrescentadas para atender ao template da disciplina.

## Resumo

O **Mentor** é um robô móvel criado para ajudar no treinamento de novos operadores de torno CNC. Ele fica em uma sala de treinamento de uma fábrica de autopeças no ABC Paulista e acompanha o aprendiz durante as atividades na máquina real. Por meio de voz, tablet, gestos e projeção de luz, mostra cada etapa, ajuda na conferência dos EPIs e permite repetir explicações sem constrangimento.

A proposta é tornar o aprendizado mais seguro e padronizado, sem perder o contato humano. O Mentor não opera o torno nem substitui seus sistemas de proteção. **O instrutor continua responsável pela avaliação final do aprendiz.**

## Introdução

### Conhecendo o problema — Entrega 1

Treinar um novo operador exige tempo, atenção e experiência. No cenário apresentado pelo grupo, três problemas se destacam: há poucos instrutores disponíveis, cada profissional pode ensinar de um jeito diferente e alguns aprendizes têm vergonha de perguntar novamente quando não entendem uma etapa.

Essa dificuldade se torna ainda mais importante diante de máquinas como o torno CNC. A **NR-12** trata da segurança no trabalho com máquinas e equipamentos e estabelece requisitos de capacitação. Por isso, o Mentor foi pensado como um **apoio ao treinamento**, e não como substituto do ensino formal, da supervisão ou das proteções da máquina.

O robô acompanha exercícios em uma sala com torno CNC, bancada e armário de EPIs. Ele apresenta instruções em etapas, aponta controles e destaca regiões da máquina com luz. O aprendiz faz a atividade no próprio ritmo; quando surge uma situação fora do roteiro, o Mentor chama o instrutor.

**Objetivo geral:** apoiar o treinamento inicial de operadores de torno CNC de forma segura, clara e adaptada ao ritmo de cada pessoa.

**Experiência desejada:** um instrutor paciente, que não julga o aprendiz e permite repetir a explicação quantas vezes forem necessárias.

### Identificação e descrição do projeto

| Item | Definição |
|---|---|
| Nome | **MENTOR** |
| Aplicação | Treinamento assistido de novos operadores de torno CNC |
| Ambiente | Sala de treinamento em fábrica de autopeças no ABC Paulista |
| Tipo | Robô móvel instrutor, com aparência minimalista |
| Usuário principal | Aprendiz de operação CNC |
| Papel do instrutor | Validar os procedimentos, resolver dúvidas complexas e realizar a avaliação final |
| Limite do robô | Não comanda o torno nem substitui os dispositivos de segurança ou a capacitação exigida |

### Objetivos específicos

1. Apresentar procedimentos de operação divididos em etapas claras.
2. Orientar a conferência dos EPIs previstos para cada atividade.
3. Mostrar os componentes da máquina por meio de gestos, tablet e projeção luminosa.
4. Permitir que o aprendiz repita instruções e tire dúvidas previstas no roteiro.
5. Combinar interações espaciais, verbais e não verbais de modo simples e seguro.
6. Preservar a privacidade do aprendiz e manter a decisão final com o instrutor.

### Benefícios esperados

- **Para o aprendiz:** aprender no próprio ritmo, perguntar sem vergonha e receber orientações visuais mais fáceis de acompanhar.
- **Para o instrutor:** ter mais tempo para dúvidas difíceis, acompanhamento individual e avaliação prática.
- **Para a fábrica:** tornar as explicações mais consistentes e organizar melhor as etapas do treinamento.

São benefícios esperados da proposta; ainda não foram medidos em testes.

### Funcionalidades previstas

- **Identificação por crachá:** reconhece o aprendiz e recupera o módulo em andamento.
- **Conferência de EPI:** informa quais equipamentos devem ser usados e pede a confirmação do aprendiz. No exemplo do torno, lembra que luvas não devem ser usadas perto de partes girantes quando houver risco de enroscamento.
- **Orientação passo a passo:** explica a etapa por voz, mostra o texto no tablet e projeta luz no componente indicado.
- **Acompanhamento:** observa a execução e consulta os estados autorizados do CNC, quando disponíveis.
- **Correção:** explica erros previstos no roteiro, com calma, e oferece nova demonstração.
- **Ajuda humana:** chama o instrutor quando há dúvida fora do conteúdo ou quando o módulo termina.
- **Parada do robô:** possui botão para interromper seus próprios movimentos, diferente da parada de emergência do torno.

### Tecnologias e ferramentas propostas

| Componente | Recurso previsto | Função |
|---|---|---|
| Locomoção | Base móvel diferencial e sensores de obstáculos | Deslocar-se apenas nas áreas permitidas da sala |
| Visão | Câmera RGB-D | Perceber a presença do aprendiz e acompanhar a atividade |
| Gestos | Braço de 2 graus de liberdade, sem garra | Apontar sem tocar na máquina |
| Orientação visual | Projetor e tablet de aproximadamente 10 polegadas | Indicar o controle certo e apresentar as instruções |
| Identificação | Leitor de crachá | Iniciar ou retomar a sessão do aprendiz |
| Comunicação | Voz, comandos curtos, botões e legendas | Permitir interação mesmo com ruído e protetor auricular |
| Consulta à máquina | Leitura autorizada de estados do CNC | Informar o contexto da etapa, sem acionar a máquina |
| Controle do treinamento | Roteiro fechado com etapas previamente aprovadas | Evitar instruções improvisadas ou incorretas |
| Prototipagem | Croqui técnico e fluxos de interação | Representar a proposta antes de uma implementação física |

## Público-Alvo e Stakeholders

O público principal são **operadores recém-contratados ou em mudança de função**, entre 18 e 55 anos, com diferentes níveis de experiência. Muitos conhecem a teoria, mas ainda não tiveram contato prático com um torno CNC. O Mentor deve acompanhar essa fase de aprendizado sem pressa.

### Stakeholders

| Categoria | Envolvidos | Interesse e possível impacto |
|---|---|---|
| **Primários** | Aprendizes | Consultam explicações, executam exercícios, recebem feedback e repetem etapas |
| **Secundários** | Instrutores, técnicos de segurança e manutenção | Validam conteúdos, respondem a exceções, supervisionam uso e cuidam da disponibilidade dos sistemas |
| **Terciários** | RH, gerência, CIPA, sindicato e demais operadores | São afetados por políticas de capacitação, trabalho, confiança e uso de dados, mesmo sem operar o robô |

### Personas — Entrega 3

**Thiago, 20 anos — aprendiz (persona primária).** Fez curso técnico em mecânica e está no primeiro emprego. Sabe a teoria, mas nunca operou um CNC. Quer ser efetivado e tem vergonha de pedir para repetir uma explicação. Com o Mentor, ele pode aprender e tirar dúvidas sem se sentir julgado.

**Seu Valdir, 57 anos — instrutor (persona secundária).** Tem 30 anos de fábrica, conhece os detalhes do trabalho e está sobrecarregado com turmas grandes. Ele desconfia do robô e teme ser substituído. Para conquistar sua confiança, o Mentor deve deixar claro que **a experiência do instrutor continua essencial**.

**O que o robô precisa saber:** identificação pelo crachá, etapa do treinamento, progresso do aprendiz e eventuais necessidades de acessibilidade, como legendas para quem tem baixa audição. Não precisa registrar sentimentos nem informações pessoais desnecessárias.

### Mapa de empatia

| Dimensão | Thiago — aprendiz | Valdir — instrutor |
|---|---|---|
| **Vê** | Máquinas grandes, avisos sobre EPI e operadores experientes trabalhando rapidamente | Turmas maiores, novas ferramentas digitais e a chegada de um robô |
| **Ouve** | Ruído da fábrica e brincadeiras direcionadas ao novato | Comentários da gerência sobre custos e produtividade |
| **Diz e faz** | Diz “entendi” mesmo com dúvida; procura vídeos no celular para revisar conceitos | Afirma “robô não ensina macete”; testa a coerência das explicações |
| **Pensa e sente** | Ansiedade para ser efetivado e receio de causar acidente | Orgulho do ofício, sobrecarga e receio de perder seu papel |
| **Dores** | Vergonha de perguntar novamente; pouca experiência prática | Pouco tempo para atenção individual; sensação de desvalorização |
| **Ganhos** | Repetição no próprio ritmo, orientação visível e possibilidade de erro sem julgamento | Mais tempo para situações difíceis e controle sobre a avaliação final |

## Contexto de uso

O cenário é uma **sala de treinamento de fábrica de autopeças no ABC Paulista**, localizada próxima à linha de produção. O espaço contém um torno CNC, uma bancada, armário de EPIs e área demarcada de circulação. Ainda que seja destinado ao ensino, o ambiente está sujeito a ruído de produção, uso de protetor auricular e trânsito de empilhadeiras no corredor adjacente. A circulação do Mentor não deve interferir com rotas logísticas nem aproximá-lo de zonas de risco da máquina.

Na região, o tema **automação e emprego** também merece cuidado. O Mentor deve se apresentar como um apoio para aprendizes e instrutores, e não como um substituto do trabalhador experiente.

**Informações necessárias:** mapa da sala e de suas áreas de risco, posição da bancada e do armário, procedimentos divididos em etapas, EPIs de cada atividade, estados do CNC disponibilizados para consulta e forma de chamar o instrutor.

**Antes de começar:** o aprendiz deve estar identificado, o exercício precisa estar autorizado e a máquina deve estar em condição segura. Quando isso não ocorre, o Mentor não continua o treinamento e solicita ajuda humana.

## Jornada do usuário

A narrativa acompanha **Thiago** em seu primeiro módulo de prática guiada no torno CNC. As letras indicam os canais de interação: **E** = espacial; **V** = verbal; **NV** = não verbal.

| Momento | Acontecimento e contexto | Interação IHR | Resultado pretendido |
|---|---|---|---|
| **1. Chegada** | Thiago entra na sala, se identifica no leitor de crachá e observa o torno. O Mentor se posiciona de frente e aproxima-se lentamente, mantendo cerca de **1,5 m**. | E, NV | Evitar susto; indicar disponibilidade e reconhecer o início do atendimento |
| **2. Apresentação** | O robô confirma a identidade e diz: “Oi, Thiago! Eu sou o Mentor. Eu mostro, você faz.” A tela apresenta o módulo. | V, NV | Reduzir incerteza e explicar os limites de cada participante |
| **3. Conferência de EPI** | O Mentor solicita a verificação dos EPIs aplicáveis e do estado seguro da tarefa. No exemplo apresentado, orienta retirar a luva quando houver risco junto a partes girantes, apontando para o armário. | V, NV | Reforçar o procedimento e solicitar validação antes do avanço |
| **4. Demonstração** | Com o CNC em condição adequada ao passo, o robô se posiciona em **formação em “L”**, aproximadamente a **1 m** do aprendiz, sem bloquear sua visão ou acesso seguro. Aponta e ilumina o controle relevante. | E, V, NV | Estabelecer atenção conjunta sobre um único ponto |
| **5. Vez do aprendiz** | Thiago realiza a ação prevista, enquanto o robô permanece em silêncio, evitando distrações. Se a etapa for confirmada, a expressão da cabeça e o LED indicam aprovação. | NV | Dar autonomia com feedback de fácil interpretação |
| **6. Dúvida ou erro** | Se houver uma divergência reconhecida pelo roteiro, o Mentor informa calmamente o que precisa ser revisado. Se não compreender o evento, suspende a orientação e chama o instrutor. | V, E, NV | Corrigir sem humilhação e evitar improvisações perigosas |
| **7. Encerramento** | O robô resume os passos revisados, oferece a consulta ao histórico de módulos e solicita a presença do instrutor para avaliação final. | V, NV | Encerrar de modo claro, sem confundir conclusão de módulo com certificação |

**Se algo sair do previsto:** o tablet substitui a voz quando houver ruído; o robô espera se o aprendiz precisar de mais tempo; a projeção é desativada se não estiver alinhada; ele aguarda a passagem de empilhadeiras e chama o instrutor quando não consegue confirmar uma condição necessária.

## Análise de concorrência — Entrega 2

O diferencial do Mentor é reunir um **robô presente na sala**, a **prática no CNC real** e a **projeção de instruções diretamente na máquina**. Para avaliar a ideia, comparamos três plataformas robóticas e as alternativas de treinamento apresentadas pelo grupo. Nenhuma delas foi identificada como um produto pronto com todas as funções propostas para o Mentor.

### Principais plataformas robóticas e características

| Robô | Capacidades relevantes | Pontos positivos para UX | Limitações no cenário CNC | Modelo de aquisição/preço |
|---|---|---|---|---|
| **Baxter** — Rethink Robotics, referência de pesquisa | Robô com braços, tela/rosto e feedback verbal/gestual, empregado em pesquisa de ensino de montagem industrial | Demonstração corporal concreta; evidência acadêmica de uso como instrutor | Plataforma de pesquisa anterior, não solução comercial atual pronta para esse treinamento; manipulação não é necessária ao Mentor | Referência histórica de pesquisa; **não há preço comercial atual comparável** |
| **temi V3 / temi Platform** | Mobilidade autônoma, interação por tela/áudio, recursos de programação e serviços | Possibilidade de receber usuário e apresentar módulos ao lado do posto | Não inclui, pronta para uso, projeção de instruções em torno CNC, braço apontador ou validação de procedimento da máquina | Plataforma comercial/RaaS ou compra conforme oferta; custo total depende de customização, licenças e suporte; **sem orçamento comparável verificado** |
| **TIAGo / TIAGo Pro — PAL Robotics** | Plataforma móvel de pesquisa com percepção, HRI, braço(s) e opções de touchscreen | Forte potencial de prototipagem de gestos, navegação e acompanhamento de tarefa | Mais complexidade e recursos de manipulação do que o Mentor requer; integração com o CNC teria de ser desenvolvida | Venda por configuração e proposta comercial; **valor final depende da cotação** |

Esses robôs são **referências de projeto**, não concorrentes diretos comprovados no mercado de treinamento de torno CNC. Baxter já aparecia na apresentação; temi e TIAGo foram acrescentados para ampliar a comparação solicitada no template.

### Alternativas tecnológicas de treinamento citadas pelo grupo

| Alternativa | Vantagens | Limitações percebidas | Relação com Mentor |
|---|---|---|---|
| **Simuladores de realidade virtual (ex.: iniciativas SENAI)** | Permitem repetição e treinamento sem expor inicialmente o aprendiz aos riscos físicos da máquina | A experiência ocorre em ambiente virtual, não substituindo integralmente o contato com o CNC real | Complemento possível antes da prática física |
| **HoloLens com Dynamics 365 Guides** | Sobreposição de instruções ao ambiente físico, perto do ponto de execução | Uso de dispositivo na cabeça juntamente com EPI; adoção e suporte dependentes do fornecedor | O Mentor usa **projeção externa** para dispensar óculos de RA |
| **Baxter instrutor de montagem — pesquisa acadêmica** | Demonstra interação instrucional por gestos, fala e elementos gráficos | Caso estudado em tarefa de montagem, não em CNC; plataforma de pesquisa, sem solução comercial específica | Referência conceitual para a combinação de fala e gesto |

**Observação sobre o slide:** em novembro de 2026, o Dynamics 365 Guides ainda está em ciclo de encerramento. A Microsoft anunciou que o **fim do suporte e da operação ocorrerá em 31 de dezembro de 2026**; portanto, é mais preciso dizer “descontinuação anunciada” do que “já descontinuado”.

### Experiência do usuário e modelos de negócio

Em geral, a realidade virtual e a aumentada oferecem boas formas de visualizar procedimentos, mas dependem de equipamentos específicos. Robôs de serviço já interagem com pessoas, porém precisariam de adaptação para ensinar no CNC. O Mentor combina essas ideias em um roteiro de treinamento na máquina real.

**Custos e modelos de negócio:** não há dados suficientes para afirmar que o Mentor seria mais barato. A implementação dependeria de plataforma física, projetor, adaptação ao CNC, programação, manutenção e atualização dos conteúdos. As soluções comparadas podem ser vendidas como equipamento, serviço ou projeto personalizado, por isso a comparação de preço dependeria de orçamentos reais.

### Padrões, tendências e recomendações

A principal tendência é aproximar a instrução do local onde a tarefa acontece. No Mentor, a prioridade deve ser **clareza e segurança**, não uma conversa livre. O ideal seria começar com um único módulo de treinamento validado, testar a projeção e oferecer sempre uma alternativa à comunicação por voz.

## Design do Robô

### Forma, função e affordances

O croqui original do grupo apresenta um robô ereto, com **aproximadamente 1.450 mm de altura**, cabeça com **450 mm de largura**, base com **600 mm de largura**, cabeça com **300 mm de profundidade** na vista lateral, e linha dos olhos em aproximadamente **1.260 mm de altura**. O robô possui **base diferencial**, cabeça com dois olhos visuais, **câmera RGB-D**, **projetor**, um **braço apontador de 2 graus de liberdade sem garra**, **tablet de 10 polegadas**, **leitor de crachá**, **anel LED** e **botão de parada de emergência do próprio robô**. A nota de projeto limita sua velocidade máxima perto de pessoas a **0,5 m/s**; este valor é uma intenção de projeto, não uma velocidade validada para operação segura.

![Croqui técnico original do Mentor: vistas frontal e lateral](assets/mentor_croqui.png)

*Figura 1 — Croqui do robô Mentor, extraído do slide 10 da apresentação do grupo. Dimensões indicativas, em milímetros, sem validação de fabricação.*

As **affordances** são deliberadas: os olhos indicam direção da atenção; o braço sem garra indica **apontar, não agarrar ou operar**; o tablet convida à consulta e ao toque; o leitor de crachá marca o início de uma sessão; o projetor evidencia o componente demonstrado; o anel luminoso comunica estado. O botão físico deixa explícita a possibilidade de parar movimentos do Mentor. Uma regra essencial de **prometer menos e entregar mais** é apresentá-lo como **instrutor de roteiro assistido**, e não como especialista infalível ou robô capaz de operar o torno.

Para acessibilidade, o texto deve acompanhar a fala, controles devem ser legíveis, as telas devem admitir ajuste de fonte/contraste e as funções essenciais não podem depender somente de cor, som ou reconhecimento de voz. O posicionamento da tela precisa considerar diferentes alturas e condições de mobilidade. A indicação luminosa não substitui instruções de segurança nem sinalizações regulamentares.

### Grau de antropomorfismo

No espectro **máquina → robject → minimalista → humanoide → androide → humano**, o Mentor ocupa a **faixa minimalista**, com elementos sociais suficientes para orientar atenção (olhos, gesto, aceno) sem simular um trabalhador humano. A ausência de mãos e rosto realista reduz a expectativa de manipulação, conversas irrestritas ou relações pessoais. A aparência condiz com um instrutor especializado e reduz o risco de **vale da estranheza**, associado a personagens quase humanos percebidos como artificiais.

Isso também responde à preocupação de Valdir: um robô muito parecido com uma pessoa poderia passar a impressão de que pretende substituir o instrutor. O Mentor **não representa um novo empregado**, mas uma interface pedagógica móvel.

### Padrões de design

O projeto utiliza dois padrões de interação apresentados na literatura de IHR:

1. **Comunicação didática (*didactic communication*):** apresenta uma ação, explica sua finalidade, mostra um exemplo e verifica se o aprendiz pode prosseguir.
2. **Revezamento de turnos (*reciprocal turn-taking*, adaptado para o ensino):** alterna os turnos “o robô mostra” e “o aprendiz faz”, oferecendo silêncio durante a execução e feedback quando a ação termina.

Na prática, é uma relação de **“mestre e aprendiz”**: o robô mostra, o operador faz e o instrutor humano avalia. Essa aplicação ao CNC foi proposta pelo grupo.

### Valores e ética

O projeto adota como valores centrais **segurança** e **privacidade**, sem deixar de considerar a autonomia do aprendiz e o respeito ao trabalho do instrutor.

- **Segurança:** o robô nunca deve aumentar o risco da operação. Não interage fisicamente com comandos da máquina, não autoriza partida, não supera intertravamentos e não substitui o responsável pela capacitação. Instruções operacionais são controladas por versão e aprovação.
- **Privacidade:** o aprendiz precisa saber quais dados são registrados, para que finalidade e com quem poderão ser compartilhados. A proposta não conserva avaliações de emoção, expressões faciais ou gravações de voz como histórico individual.

**Risco ético principal:** registros de erros, hesitações ou tempo de execução serem usados por RH ou gestão como indicadores punitivos, gerando pressão sobre trabalhadores em experiência. **Mitigação proposta:** coleta mínima para o acompanhamento pedagógico, acesso do aprendiz ao próprio histórico, política de retenção clara, visibilidade restrita aos responsáveis autorizados e separação entre feedback instrucional e critérios formais de avaliação. Decisões de aprovação permanecem com o instrutor humano.

Pausas e erros podem indicar que o aprendiz precisa de ajuda, mas não permitem concluir seu estado emocional. Dados pessoais devem ser tratados conforme as regras aplicáveis, incluindo a LGPD.

### Protótipo no papel

O **croqui da Figura 1** é o protótipo em papel do grupo. Ele apresenta as vistas frontal e lateral e a posição dos componentes. Antes de construir o robô, ainda seriam necessários testes de estabilidade, alcance do braço, ergonomia, projeção e segurança de movimentação.

## Ações do robô

| Ação | Pré-requisitos | Mudança esperada no ambiente/estado da tarefa | Limite e fallback |
|---|---|---|---|
| **Identificar aprendiz** | Sessão autorizada e crachá válido | Sessão do módulo certo é apresentada | Se não houver identificação válida, solicitar instrutor |
| **Verificar EPI** | Aprendiz parado diante do robô; lista de EPIs válida para a etapa | Aprendiz confere/ajusta os itens sob orientação | A visão não certifica conformidade; validação humana quando exigida |
| **Demonstrar etapa** | Etapa anterior concluída; versão do roteiro aprovada; condições do CNC verificadas | Aprendiz compreende a ação a ser realizada | Sem confirmação de estado seguro, não demonstrar execução prática |
| **Apontar e projetar** | Alinhamento verificado; região da máquina identificada; área de movimento livre | Componente correto fica destacado visualmente | Se houver incerteza no alinhamento, retirar projeção e chamar instrutor |
| **Acompanhar execução** | Aprendiz executando etapa autorizada; sensores em condições de funcionamento | Etapa identificada como concluída ou necessidade de revisão indicada | Não inferir segurança apenas por vídeo; leitura do CNC é informativa |
| **Corrigir erro** | Divergência reconhecida em regra aprovada | Aprendiz recebe explicação e oportunidade de repetir | Dúvida fora do roteiro → suspensão e instrutor |
| **Encerrar módulo** | Etapas previstas concluídas ou sessão interrompida | Resultado pedagógico exibido e instrutor solicitado | Conclusão no robô ≠ habilitação/autorização para trabalhar |
| **Parar movimento do Mentor** | Botão do robô acionado ou condição de parada identificada | Mobilidade/gestos do Mentor cessam de maneira definida no projeto | A parada do Mentor não substitui a parada de emergência do CNC |

## Interações do robô

### Espacial — Entrega 4

O Mentor considera a **proxêmica de Hall** (distâncias entre pessoas) e as **F-formations** (posição das pessoas durante uma interação). A aproximação inicial é frontal, em baixa velocidade, com parada planejada a **aproximadamente 1,5 m** (zona social). Durante a explicação junto ao painel, utiliza uma formação lateral em **“L”**, a **aproximadamente 1 m**, somente se houver folga segura e sem obstruir zonas de operação. As distâncias são ideias iniciais do grupo e precisam ser testadas antes de qualquer uso real.

| Interação espacial | Pré-requisito | Comportamento | Resposta emocional desejada |
|---|---|---|---|
| **Acolher** | Aprendiz identificado, caminho livre, área segura | Aproximação lenta pela frente; cabeça orientada ao usuário; parada a ~1,5 m | Tranquilidade e previsibilidade |
| **Ensinar junto ao painel** | Máquina e área em condição autorizada; posição livre ao lado | Forma um “L” com usuário e painel; mantém ~1 m quando possível, preservando rota de saída | Foco e sensação de acompanhamento sem invasão |
| **Esperar execução** | Aprendiz no turno de execução | Recolhe gesto, estabiliza base e não invade o espaço de trabalho | Autonomia e menor distração |
| **Contornar pessoas/grupos** | Área mapeada, obstáculos detectados | Reduz velocidade, aguarda abertura ou retorna ao ponto de espera; nunca passa entre pessoas que conversam | Confiança no respeito ao espaço social |
| **Aguardar empilhadeira** | Tráfego percebido em área adjacente | Não cruza a rota; aguarda liberação conforme sinalização local | Percepção de prudência |

**Na aproximação**, o Mentor olha na direção do usuário e se desloca devagar, sempre que possível pela frente. Não movimenta o braço perto de alguém e evita passar entre pessoas que estão conversando.

**Em outros ambientes**, o comportamento muda: numa sala grande, pode manter mais distância; numa sala pequena, é melhor ficar parado em um ponto definido. A segurança vem antes da movimentação.

### Verbal — Entrega 5

A fala do Mentor segue um **roteiro fechado**, revisado pelo instrutor. Não seria um chatbot com respostas livres: inventar ou esquecer um passo pode gerar risco em uma máquina. O robô reconhece comandos simples e responde somente dentro do conteúdo aprovado.

**Fluxo conversacional proposto:** `Boas-vindas → Conferência de EPI → Demonstração → Confirmação de entendimento → Execução silenciosa → Feedback → Próxima etapa / Repetição / Instrutor`.

| Situação | Exemplo de fala do Mentor | Pré-requisito | Emoção/efeito esperado |
|---|---|---|---|
| **Início** | “Oi, Thiago! Eu sou o Mentor. Eu mostro, você faz.” | Crachá identificado | Acolhimento e clareza de papel |
| **Conferência** | “Vamos conferir os EPIs previstos para esta etapa antes de começar.” | Lista aprovada disponível | Atenção e responsabilidade |
| **Demonstração** | “Observe este controle. Vou destacar sua posição na máquina.” | Alinhamento da projeção validado | Segurança e foco |
| **Pedido de repetição** | “Claro. Vou mostrar novamente, passo a passo.” | Solicitação reconhecida | Redução de constrangimento |
| **Erro detectado** | “Vamos revisar esta etapa com calma. Veja novamente a indicação.” | Divergência reconhecida | Apoio, sem julgamento |
| **Pedido fora do escopo** | “Não tenho uma orientação aprovada para isso. Vou chamar o instrutor.” | Dúvida não coberta | Confiança na honestidade do sistema |
| **Fim** | “Concluímos esta parte do treino. O instrutor fará a avaliação final.” | Módulo finalizado | Clareza sobre responsabilidades |

**Ritmo da conversa:** frases curtas, voz adulta e calma e tempo para o aprendiz ler. **Enquanto a pessoa executa a etapa, o Mentor fica em silêncio.** Se ela demora, pode perguntar “Precisa de mais tempo?” sem pressupor que houve erro.

**Limitações:** o barulho e o protetor auricular podem atrapalhar a voz. Por isso, o tablet terá botões grandes e legendas. Quando não compreender uma solicitação, o robô pede confirmação; se a dúvida continuar, chama o instrutor.

### Não verbal — Entrega 6

Os canais principais são **olhar** e **gesto**, apoiados pelo uso de **luz/projeção** e acenos simplificados.

| Canal | Pré-requisito | Comportamento do robô | Resposta emocional esperada |
|---|---|---|---|
| **Olhar/direção da cabeça** | Usuário e elemento de ensino identificados | Olhos da tela alternam atenção do aprendiz para o componente indicado | Entendimento do foco conjunto |
| **Apontamento do braço** | Campo livre e componente validado | Braço de 2 GDL aponta sem encostar ou agarrar | Clareza da instrução sem sensação de ameaça |
| **Confirmação por aceno** | Conclusão da etapa verificada | Movimento discreto de cabeça e sinal visual de sucesso | Reconhecimento do progresso |
| **Projeção localizada** | Calibração segura e posição correta confirmada | Região do controle é iluminada; sem tocar nem comandar a máquina | Menor esforço de localização |
| **Sinalização de pausa/erro** | Divergência conhecida ou interrupção necessária | O robô imobiliza gestos e exibe mensagem; evita sinais ambíguos | Entendimento de que é necessário aguardar |

**O que o robô observa:** presença do aprendiz, posição geral do corpo, pausas e repetição de passos. Isso pode indicar necessidade de ajuda, mas **não permite afirmar o que a pessoa está sentindo**.

**Coordenação entre canais:** fala, gesto e projeção precisam indicar o mesmo ponto. Se o robô disser uma coisa e apontar outra, o aprendiz pode se confundir. Nessa situação, a demonstração deve parar e o instrutor deve ser chamado.

**Recurso próprio do Mentor:** a projeção de luz diretamente no componente, junto da fala, é seu principal diferencial. O anel LED complementa o aviso, mas a informação também aparece em texto para não depender somente de cores.

## Emoção

Para pensar nas emoções durante o treino, o grupo utilizou o **modelo de Russell**, baseado em duas dimensões: **valência** (sensação agradável ou desagradável) e **ativação** (intensidade da reação). Isso ajuda a planejar respostas para momentos de frustração, ansiedade, tédio ou entusiasmo.

**Possíveis sinais:** demora para iniciar uma etapa, erros repetidos e mudança no tom de voz. Como esses sinais podem ter várias causas, o Mentor **não tenta diagnosticar emoções**. Ele apenas oferece ajuda: “Quer rever esta etapa?”.

**Quando acompanhar a emoção:** após um acerto, pode acenar com a cabeça e usar luz verde. **Quando não acompanhar:** diante de irritação ou medo, continua calmo, fala devagar e oferece uma pausa. A ideia não é fingir sentimentos humanos, mas agir de modo respeitoso.

**Limites da relação:** o Mentor não é amigo, conselheiro ou representante do RH. Ele apenas orienta o treinamento. O robô também não deve guardar avaliações emocionais sobre o aprendiz.

## Considerações finais

O Mentor busca tornar o treinamento inicial no torno CNC **mais claro, paciente e padronizado**, sem retirar a importância do instrutor humano. A proposta combina fala, gestos, projeção e deslocamento cuidadoso para acompanhar o aprendiz. Como ainda é um projeto conceitual, as próximas etapas seriam validar o conteúdo técnico, testar a interação e avaliar a segurança do robô em um ambiente real.

## Referências

1. **BRASIL. Ministério do Trabalho e Emprego.** *Norma Regulamentadora nº 12 — Segurança no Trabalho em Máquinas e Equipamentos*. Disponível em: https://www.gov.br/trabalho-e-emprego/pt-br/acesso-a-informacao/participacao-social/conselhos-e-orgaos-colegiados/comissao-tripartite-partitaria-permanente/normas-regulamentadora/normas-regulamentadoras-vigentes/norma-regulamentadora-no-12-nr-12. Acesso em: 11 nov. 2026.
2. **KAHN, Peter H., Jr. et al.** *Design Patterns for Sociality in Human-Robot Interaction*. HRI '08, 2008. Disponível em: https://www.cs.cmu.edu/~illah/CLASSDOCS/kahn.pdf.
3. **QUITTER, Thomas et al.** *Humanoid Robot Instructors for Industrial Assembly Tasks*. HAI '17, 2017. DOI: https://doi.org/10.1145/3125739.3125760.
4. **RUSSELL, James A.** *A Circumplex Model of Affect*. Journal of Personality and Social Psychology, v. 39, n. 6, p. 1161–1178, 1980. DOI: https://doi.org/10.1037/h0077714.
5. **MICROSOFT.** *Dynamics 365 Guides and Remote Assist reaching end of support on December 31, 2026*. Disponível em: https://learn.microsoft.com/pt-br/lifecycle/announcements/dynamics-365-guides-remote-assist-end-of-support. Acesso em: 11 nov. 2026.
6. **TEMI.** *temi Robots; Become a temi Developer*. Disponível em: https://www.robotemi.com/robots/ e https://www.robotemi.com/developers/. Acesso em: 11 nov. 2026.
7. **PAL ROBOTICS.** *TIAGo Mobile Manipulator Robot; Education*. Disponível em: https://pal-robotics.com/robot/tiago/ e https://pal-robotics.com/areas/education/. Acesso em: 11 nov. 2026.
8. **HAZESHIFT.** *Mapa de empatia*. Disponível em: https://hazeshift.com.br/mapa-de-empatia/. Fonte de apoio ao instrumento de empatia citado na apresentação do grupo.
9. **CENTRO UNIVERSITÁRIO FEI.** *Template de projeto de Interação Humano-Robô*. Disponível em: https://github.com/FagnerPimentel-Academic/template-ihr. Acesso em: 11 nov. 2026.

