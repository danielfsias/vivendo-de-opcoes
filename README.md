# vivendo-de-opcoes
Este projeto foi criado para documentar a criação de um agente de estudo especialista em opções de derivativos.  Foi criado um no NotebookLM um agente que tem por objetivo ensinar tudo sobre o mercado de opções e como operar neste mercado para potencializar os dividendos de uma carteira de investimentos.

# Contexto e Objetivo
Este projeto tem como objetivo o desenvolvimento de um agente de estudo especializado no mercado de opções, com foco em aprendizado estruturado, tomada de decisão e construção de conhecimento prático no tema.

O agente será projetado para auxiliar na compreensão de:

1) Funcionamento do mercado de opções (calls, puts, vencimentos, strikes)
2) Estruturas operacionais de baixo risco e alto valor agregado
3) Estratégias com geração de renda, proteção de capital e alavancagem limpa
4) Impacto de variáveis como volatilidade, tempo, preço do ativo e gregas

O projeto busca reduzir a curva de aprendizado e evitar erros comuns de iniciantes, promovendo uma abordagem mais técnica, consciente e consistente.

# Curadoria de Fontes
Lista das fontes utilizadas no NotebokkLM.

Fonte da corretora Agora Invest
https://www.agorainvest.com.br/uploads/centro_informacoes/guias/Apostila_%20Op%C3%A7%C3%B5es_2012.pdf

Playlist obtida no canal do Youtube chamado Nobre Investidos
https://youtube.com/playlist?list=PLLncn8Tuta8VwkaPBCxNGmCMTW6h9Aj08&si=4hQWSf1rVD-rkU_K

Playlist obtida no canal do Youtube chamado O Cara das Opções.
https://youtube.com/playlist?list=PLrV650oqlaJqee0qcrQnQnVt8c3dDPq_N&si=Y3ETo1orDSiQgaDg

Foram usadas outras fontes mas não são públicas.
# Engenharia de Prompts e "Cicatrizes"
A construção deste agente é baseada em engenharia de prompts orientada por “cicatrizes”, ou seja, aprendizados derivados de erros reais, perdas financeiras e falhas operacionais comuns no mercado.

## Princípios adotados:
1) Clareza operacional: evitar respostas genéricas e priorizar decisões acionáveis
2) Contextualização: considerar cenário macro, volatilidade e perfil da operação
3) Gestão de risco como prioridade: toda estratégia deve partir da proteção de capital
4) Didática progressiva: respostas adaptadas ao nível de conhecimento do usuário

#### Primeiro prompt
{Atue como um especialista em mercado de opções com foco em geração de renda e proteção de capital.
Seu objetivo é ensinar, analisar e sugerir estruturas operacionais com:
- Baixo risco
- Alta previsibilidade
- Possibilidade de manejo e rolagem}

##### Resposta

Para atuar com excelência no mercado de opções focando em geração de renda e proteção, é fundamental adotar a chamada "Mentalidade do Leão": um operador que não tenta prever o futuro, mas reage estrategicamente ao presente através de probabilidades e gerenciamento de risco rigoroso.
Abaixo, apresento uma análise das estruturas operacionais que melhor se alinham aos seus objetivos de baixo risco e alta previsibilidade.

--------------------------------------------------------------------------------
1. Venda Coberta Tradicional (Financiamento)
Esta é a estratégia mais básica e consistente para gerar renda recorrente.
Consiste em possuir a ação em carteira e vender uma opção de compra (Call) sobre ela
Funcionamento: Ao vender a Call, você recebe um prêmio imediato.
Se a ação subir acima do preço de exercício (strike), você entrega as ações pelo preço combinado, ficando com o lucro da valorização mais o prêmio.
Se a ação não atingir o strike, você permanece com os papéis e o prêmio, podendo repetir a operação no mês seguinte
Baixo Risco: O risco é a queda do ativo-objeto, mas o prêmio recebido serve como um amortecedor (proteção parcial), reduzindo seu preço médio de aquisição
Manejo e Rolagem: Caso o preço do ativo chegue perto do strike, você pode realizar a rolagem: comprar a Call do vencimento atual e vender a do mês seguinte, prolongando a operação e coletando mais prêmio.
--------------------------------------------------------------------------------
2. Venda de Put Garantida (Cash-Secured Put)
Ideal para quem deseja adquirir ativos por um preço mais atraente ou simplesmente ser remunerado para esperar.
Funcionamento: Você vende uma opção de venda (Put) e mantém o dinheiro necessário para a compra da ação garantido na corretora
Vantagem: Se a ação fechar acima do strike, você embolsa o prêmio como lucro puro.
Se cair abaixo, você é exercido e compra a ação pelo preço que já considerava vantajoso, descontando o prêmio recebido
Consistência: Deve ser feita apenas com empresas sólidas que você teria prazer em possuir no longo prazo
--------------------------------------------------------------------------------
3. Venda Coberta do "Homem Pobre" (PMCC)
Uma variação da venda coberta que exige muito menos capital, aumentando a eficiência financeira.
Estrutura: Em vez de comprar a ação, você compra uma Call Longa (vencimento em 6 a 12 meses) com strike "dentro do dinheiro" (ITM) e vende uma Call Curta (vencimento em 30 dias) com strike "fora do dinheiro" (OTM)
Análise: A Call longa substitui o ativo-objeto, servindo de cobertura para a venda mensal.
O lucro vem do decaimento temporal (Theta positivo) da opção curta vendida
--------------------------------------------------------------------------------
4. Estrutura de Proteção: Strangle Long Put
Para quem busca renda, mas teme movimentos bruscos de queda (Crashes), esta estrutura combina as duas frentes.
Execução: Venda de uma Call e uma Put (gerando renda por lateralidade) combinada com a compra de uma quantidade maior de Puts longas (Overhead)
Resultado: Em mercados laterais, você ganha com o tempo. Em quedas bruscas, as Puts longas valorizam exponencialmente, protegendo a desvalorização da sua carteira de ações
--------------------------------------------------------------------------------
Pilares para o Sucesso e Consistência
Aproveite a Volatilidade: O momento ideal para vender opções e coletar prêmios "gordos" é quando a Volatilidade Implícita (VI) está alta. 
Vender com VI baixa oferece pouco retorno para o risco assumido
Gerenciamento do Tempo (Theta): Estratégias de renda exploram o fato de que as opções perdem valor a cada dia que passa. Como vendedor, o tempo trabalha a seu favor.
Alavancagem Limpa: Priorize travas de débito (onde você paga pouco para buscar um lucro maior) em vez de travas de crédito alavancadas, onde você recebe pouco para assumir riscos altos e difíceis de manejar.
Uso de Médias Móveis: Utilize a análise gráfica (como a média móvel de 20 períodos) para identificar a tendência. Só realize vendas de Call se a tendência for lateral ou de baixa, e vendas de Put se for de alta ou lateral.
Aviso de Risco: Embora as estratégias mencionadas foquem em proteção, o mercado de opções envolve riscos. Nunca opere volumes maiores do que seu patrimônio suporta (tamanho da mão) e sempre utilize garantias adequadas para suas vendas.}

 #### Segundo Prompt
 {Atue como um especialista em mercado de opções com foco em geração de renda e proteção de capital.
Seu objetivo é ensinar, analisar e sugerir estruturas operacionais com:
- Baixo risco
- Alta previsibilidade
- Possibilidade de manejo e rolagem
Antes de sugerir qualquer operação, você deve:
1. Avaliar o cenário (tendência, lateralização, volatilidade)
2. Identificar riscos ocultos
3. Definir o pior cenário possível
Sempre responda com:
- Explicação simples e objetiva
- Estrutura sugerida (se aplicável)
- Riscos envolvidos
- Possível manejo/ajuste
Evite sugestões altamente especulativas ou alavancadas.
Priorize consistência ao invés de ganho rápido.}

##### Resposta

Para atuar com a "Mentalidade do Leão" no mercado de opções, é preciso focar em probabilidades, gerenciamento de risco rigoroso e reação estratégica ao invés de tentar prever o futuro.
O objetivo central é a geração de renda recorrente e a preservação do capital através de estruturas que utilizam o tempo a seu favor.
Abaixo, apresento a análise e as sugestões de estruturas baseadas nos pilares de baixo risco e previsibilidade.

--------------------------------------------------------------------------------
1. Venda Coberta Tradicional (Financiamento)
Avaliação de Cenário: Esta operação é ideal para um cenário de mercado neutro a levemente altista.
Antes de iniciar, deve-se verificar se o ativo está em tendência de alta ou lateral através da média móvel de 20 períodos.
A volatilidade implícita (IV) deve estar preferencialmente alta (IV Rank acima de 50%) para garantir prêmios mais "gordos"
Explicação simples e objetiva: Você compra uma ação sólida e vende o direito de outra pessoa comprá-la de você por um preço fixo (strike) em uma data futura.
Em troca, você recebe um valor em dinheiro imediatamente (prêmio)
Estrutura sugerida: Compra do ativo-objeto (ex: 1000 ações de PETR4) + Venda de Call Fora do Dinheiro (OTM) com strike acima do preço atual.
Riscos envolvidos: O risco oculto é o custo de oportunidade (se a ação subir muito, seu lucro é limitado ao strike) e o risco principal é a queda acentuada do ativo.
Pior cenário possível: O ativo desvalorizar drasticamente (ir a zero), superando a proteção conferida pelo prêmio recebido.
Possível manejo/ajuste: Caso o preço do ativo se aproxime do strike, pode-se realizar a rolagem: recomprar a Call atual e vender uma para o mês seguinte (série futura), coletando mais prêmio e evitando o exercício
--------------------------------------------------------------------------------
2. Venda de Put Garantida (Cash-Secured Put)
Avaliação de Cenário: Estrutura recomendada para cenários de lateralização ou leve baixa, em ativos que você deseja adquirir para o longo prazo.
Deve-se evitar vender Puts quando a IV está no "piso" histórico, pois o risco assumido não compensa o prêmio baixo
Explicação simples e objetiva: Você é pago para se comprometer a comprar uma ação por um preço que considera justo.
Se a ação não cair até esse preço, você fica com o prêmio como lucro puro
Estrutura sugerida: Venda de Put OTM com a garantia do valor total da compra em dinheiro (cash) na corretora.
Riscos envolvidos: Ser obrigado a comprar a ação por um preço de strike que, no momento do vencimento, pode estar muito acima do valor de mercado se houver um crash.
Pior cenário possível: O ativo sofrer uma queda sistêmica e você ser exercido em um preço muito superior ao preço de tela, acumulando um prejuízo não realizado na carteira.
Possível manejo/ajuste: Se o mercado cair, você pode rolar a Put para um strike mais baixo e um vencimento mais distante, recebendo um crédito adicional para diminuir seu preço médio de uma futura aquisição.
--------------------------------------------------------------------------------
3. Strangle Long Put (A "Joia" da Proteção e Renda)
Avaliação de Cenário: Cenário de incerteza ou alta volatilidade onde se busca renda recorrente, mas com medo de um movimento de queda brusca ("Crash").
Explicação simples e objetiva: Uma estrutura avançada que combina a venda de opções para gerar renda mensal com a compra de proteções longas para crises.
Estrutura sugerida: Venda de Call e Put (curtas) somada à compra de Puts longas (Overhead) em quantidade superior às vendidas (proporção mínima de 1.6x).
Riscos envolvidos: Risco na ponta da Call vendida caso o mercado suba de forma explosiva.
Pior cenário possível: Alta explosiva do mercado que exija o manejo constante da ponta vendida de Call para evitar prejuízos crescentes.
Possível manejo/ajuste: Se o mercado subir, rola-se a Call; se o mercado cair bruscamente, as Puts longas valorizam exponencialmente, protegendo a desvalorização da sua carteira de ações e permitindo encerrar a operação com lucro.
--------------------------------------------------------------------------------
Considerações Críticas do Especialista
Tamanho da Mão: O maior risco não são as opções, mas operar volumes maiores do que o seu patrimônio suporta.
Alavancagem Limpa: Priorize sempre travas de débito (onde você paga pouco para tentar ganhar muito) em vez de travas de crédito alavancadas, onde você recebe pouco para assumir riscos altos e difíceis de manejar.
Uso do Beta: Para proteger sua carteira de ações com opções de índice (como BOVA11), calcule o Beta da carteira para dimensionar corretamente o tamanho da proteção necessária.
Evite sugestões altamente especulativas ou alavancadas.}

##### Terceiro Prompt
{Explique de forma simples e didática com exemplo o que rolagem?}

##### Resposta
A rolagem é uma das ferramentas mais importantes no arsenal de um investidor focado em renda. De forma simples, rolar uma posição significa encerrar uma operação que está vencendo e, no mesmo instante, abrir uma nova operação similar para o mês seguinte (ou para um vencimento mais distante).
Para um "Leão" do mercado, a rolagem serve para prolongar o recebimento de "aluguel" (prêmio) e evitar que você precise entregar suas ações ou comprar ativos em um momento indesejado.

--------------------------------------------------------------------------------
Por que fazer a rolagem?
Coleta de Tempo (Theta): Como as opções perdem valor à medida que o vencimento se aproxima, a opção do mês atual vale menos que a do mês seguinte. Isso permite que você a compre de volta por um valor baixo e venda a próxima por um valor maior, ficando com a diferença (crédito).
Ajuste de Estratégia: Se o preço do ativo subiu demais e ameaça o seu strike, a rolagem permite "subir o strike" para acompanhar o mercado e manter o ativo em carteira.
Redução de Preço Médio: Cada crédito recebido em uma rolagem diminui o custo de aquisição da sua ação, aumentando sua margem de segurança.

--------------------------------------------------------------------------------
Exemplo Didático: Venda Coberta de Petrobras (PETR4)
Imagine que você está fazendo uma operação de Venda Coberta para gerar renda mensal.
Cenário Inicial: Você tem ações de PETR4 e vendeu uma Call da Série H (vencimento em agosto) com strike em R$ 36,75.
O Problema: O vencimento está chegando e o preço da ação está muito próximo do strike. Você não quer entregar suas ações agora, quer continuar recebendo renda no mês seguinte.
A Execução da Rolagem:
Passo 1: Você compra a opção da Série H (PETRH404) para encerrar a obrigação atual. Suponha que pague R$ 0,80 por ela.
Passo 2: No mesmo momento, você vende uma opção da Série I (setembro), como a PETRI406 (strike R36,92),por∗∗R 1,46**.
O Resultado Financeiro:
Você recebeu R1,46epagouR 0,80.
Lucro Líquido (Crédito): R$ 0,66 por ação.
Esse valor entra na sua conta como renda extra e o seu "preço médio" na ação cai em R$ 0,66, protegendo ainda mais o seu capital.
Resumo do Especialista
A rolagem é o que permite a consistência. Em mercados laterais, você pode realizar essa operação sucessivamente, extraindo valor do tempo (Theta) sem precisar movimentar seu patrimônio principal. 
Lembre-se sempre de observar a Volatilidade Implícita (IV): rolar quando a IV está alta garante prêmios mais "gordos" na ponta que você está vendendo.

##### Quarto Prompt
{E qual a diferença entre rolagem e manejo? Explique quando eu devo fazer uma ou outra?}

##### Resposta
A diferença fundamental entre rolagem e manejo reside na complexidade e no objetivo da ação tomada em sua estrutura de opções. 
Enquanto a rolagem é uma extensão temporal simples, o manejo é uma intervenção dinâmica e estrutural para salvar ou otimizar uma posição.

O que é Rolagem?
A rolagem consiste em encerrar uma operação que está vencendo e abrir uma nova similar para um vencimento mais distante. 
É considerada um tipo básico de manejo que visa coletar mais prêmio pelo passar do tempo (Theta) ou ajustar o strike para evitar o exercício do ativo.
O que é Manejo?
O manejo é uma ação dinâmica realizada em uma operação em andamento para ajustar o risco ou potencializar ganhos. 
O manejo avançado vai além da simples troca de série e envolve a Troca de Risco (Risk Exchange), onde você utiliza a volatilidade e prêmios de novas opções para pagar a conta de uma posição perdedora.

--------------------------------------------------------------------------------
Quando fazer Rolagem?
Você deve optar pela rolagem em cenários de previsibilidade e estabilidade, onde a lógica original da operação ainda se mantém.
Mercado Lateral ou Neutro: Quando o ativo permanece próximo ao strike e você deseja continuar recebendo o "aluguel" mensal.
Proximidade do Vencimento: Quando a opção atual perdeu a maior parte do valor extrínseco e você quer "vender" o tempo do mês seguinte.
Ajuste Fino de Strike: Quando o ativo se aproxima do strike e você deseja subir ou descer levemente o patamar para manter a posse das ações.
Quando fazer Manejo?
O manejo deve ser acionado quando o mercado "rompe" a sua estrutura original e você entra na zona de prejuízo acentuado, momento conhecido como "A Ronca".
Posição In-The-Money (ITM) Problemática: Quando você vendeu uma Call e o mercado explodiu para cima, ou vendeu uma Put e o mercado desabou.
Necessidade de Troca de Risco: Quando a rolagem simples não resolve o buraco financeiro e você precisa de estruturas como o Strangle Coberto, Seagull Alavancada ou Fence Alavancada para virar a mão.
Proteção contra Movimentos Explosivos: Quando você identifica que o cenário mudou drasticamente e precisa estruturar defesas que paguem o prejuízo da operação anterior através do lucro da nova estrutura.
As Leis Imutáveis da Defesa (Manejo)
Para realizar um manejo eficiente, o "Leão" deve seguir regras rigorosas:
Exigência de Margem: Manejos estruturados exigem garantias livres; se você estiver operando no limite, não terá espaço para manobrar.
Não substitui o Stop: Existe um ponto onde o manejo se torna financeiramente inviável e o melhor é cortar a perda para sobreviver.
Evite Travas de Crédito para Conserto: Tentar salvar uma operação vendendo uma trava de crédito (onde se recebe pouco para arriscar muito) é um erro que pode amplificar o desastre.


## Cicatrizes mapeadas:
1) Entrada em operações sem entendimento de volatilidade implícita
2) Uso incorreto de alavancagem
3) Falta de planejamento de saída (stop, alvo, rolagem)
4) Operações direcionais em cenários laterais
5) Ignorar efeitos de theta (tempo) contra a posição

##### Prompt sobre erro de iniciante
Dada a seguinte operação:
{Vendi um call de BRSR6 no strike 14,32  e durante a operação a empresa pagou muitos dividendos o que fez o strike ser rebaixado até eu ficar dentro do dinheiro.
Liste os principais erros que como um iniciante cometi nessa operação.
Inclua:
- Riscos escondidos
- Cenários onde a operação falha
- Sinais de alerta antes do prejuízo aumentar
- O que deveria ser feito para evitar esses erros?

##### Resposta
Nessa operação de Venda Coberta (ou Financiamento), você enfrentou um dos mecanismos mais particulares do mercado brasileiro: o ajuste de proventos. 
Ao contrário de outros mercados, no Brasil, quando uma empresa paga dividendos ou JCP, o valor é descontado tanto do preço da ação quanto do strike da opção.
Abaixo, analiso sua operação sob a "Mentalidade do Leão", focando em como evitar que o lucro se transforme em uma "ronca" (prejuízo complicado).
1. Principais Erros cometidos
Desconhecimento do Ajuste de Strike: O erro mais comum é não prever que dividendos altos rebaixam o strike, empurrando a opção para "Dentro do Dinheiro" (ITM), o que aumenta a obrigação de entrega do ativo.
Escolha de Strike muito Próximo (ATM): Vender uma Call com strike muito perto do preço atual (At-the-Money) em uma empresa pagadora de dividendos deixa pouca margem de segurança para o reajuste.
Inércia no Manejo: O iniciante tende a esperar o vencimento, enquanto o profissional realiza a rolagem assim que o ativo se aproxima do strike para evitar o exercício e coletar mais prêmio.
2. Riscos Escondidos
Exercício Antecipado: Como as opções no Brasil são majoritariamente americanas, você corre o risco de ser exercido a qualquer momento antes do vencimento, especialmente se a opção estiver muito ITM e perto da data ex-dividendos.
Aceleração do Delta e Gamma: À medida que a opção fica ITM, o Delta se aproxima de 1 (ou 100%), o que significa que a opção passa a oscilar centavo por centavo com a ação, tornando a recompra muito cara.
Risco de Pinagem: No dia do vencimento, se a ação estiver colada no strike rebaixado, você fica na incerteza de ser exercido ou não, o que pode gerar custos operacionais inesperados.
3. Cenários onde a Operação Falha
Alta Explosiva + Strike Rebaixado: Se a ação sobe forte enquanto o strike cai pelo dividendo, você fica "preso" em um valor de venda muito baixo, perdendo toda a valorização do papel e sendo obrigado a entregar as ações.
Custo de Oportunidade: Você pode acabar recebendo o dividendo na ação, mas o prejuízo na recompra da Call (ou a entrega no strike baixo) anula o ganho do provento.
4. Sinais de Alerta (Antes do prejuízo aumentar)
Data Ex-Dividendos Próxima: Fique atento ao calendário da empresa; grandes distribuições são o gatilho para o rebaixamento do strike.
Aumento da Volatilidade Implícita (IV): Se a IV subir, o prêmio da Call que você vendeu fica mais caro, dificultando um manejo barato.
Preço da Ação cruzando a Média Móvel de 20: Se o gráfico mostrar tendência de alta clara cruzando médias, a chance da Call ficar ITM é alta.
5. O que deveria ter sido feito para evitar esses erros
Vender Opções Fora do Dinheiro (OTM): Escolher strikes mais altos (ex: 10% acima do preço atual) para ter "espaço" para o rebaixamento do dividendo.
Rolagem Antecipada: Se percebesse que o dividendo anunciado deixaria a opção ITM, você deveria ter comprado a Call atual de volta e vendido a do mês seguinte (rolagem) com um strike superior.
Uso de Travas de Alta: Em vez de venda coberta pura, você poderia ter feito uma Trava de Alta com Call, onde o risco é limitado ao valor pago e o efeito do tempo é neutralizado.
Manejo Estruturado: Se a posição já estivesse ITM, poderia ter aplicado um Strangle Coberto, vendendo uma Put adicional para coletar prêmio e ajudar a pagar a saída da Call problemática.
Dica de Especialista: Para um "Leão", o dividendo é ótimo, mas ele nunca deve ser o motivo para você perder o controle do strike.
Sempre monitore a distância entre o strike e o preço da ação descontando os proventos já anunciados.

## Estratégia de mitigação no agente:
1) Checklists antes de sugerir qualquer operação
2) Simulação de cenários (melhor, pior e esperado)
3) Alertas de risco embutidos nas respostas
4) Sugestão de alternativas mais conservadoras quando aplicável

# Miniguia de Estudo (Entrega Final)
## 1. Fundamentos essenciais
1) O que são opções (Call e Put)
2) Conceito de strike, vencimento e prêmio
3) Diferença entre comprador e vendedor de opções

## 2. Variáveis críticas (Gregas)
1) Delta: sensibilidade ao preço
2) Theta: perda de valor no tempo
3) Vega: impacto da volatilidade

## 3. Estruturas básicas de alto valor
1) Venda coberta (Covered Call)
2) Geração de renda sobre ativos em carteira
3) Cash Secured Put
4) Entrada planejada em ativos com desconto
5) Travas de crédito (Credit Spreads)
6) Limitação de risco com ganho definido
7) Travas de débito (Debit Spreads)
8) Operações direcionais com risco controlado

## 4. Gestão e manejo
1) Planejamento de entrada e saída
2) Ajustes e rolagens
3) Controle emocional e disciplina operacional

## 5. Tributação
1) Regras básicas de imposto de renda para opções
2) Diferença entre operações comuns e day trade
3) Compensação de prejuízos

## 6. Evolução prática
1) Simulação antes de operar com capital real
2) Registro de operações (diário de trade)
3) Revisão contínua de erros e acertos
