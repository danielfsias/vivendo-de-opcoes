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
. Consiste em possuir a ação em carteira e vender uma opção de compra (Call) sobre ela
Funcionamento: Ao vender a Call, você recebe um prêmio imediato
. Se a ação subir acima do preço de exercício (strike), você entrega as ações pelo preço combinado, ficando com o lucro da valorização mais o prêmio
. Se a ação não atingir o strike, você permanece com os papéis e o prêmio, podendo repetir a operação no mês seguinte
Baixo Risco: O risco é a queda do ativo-objeto, mas o prêmio recebido serve como um amortecedor (proteção parcial), reduzindo seu preço médio de aquisição
Manejo e Rolagem: Caso o preço do ativo chegue perto do strike, você pode realizar a rolagem: comprar a Call do vencimento atual e vender a do mês seguinte, prolongando a operação e coletando mais prêmio.
--------------------------------------------------------------------------------
2. Venda de Put Garantida (Cash-Secured Put)
Ideal para quem deseja adquirir ativos por um preço mais atraente ou simplesmente ser remunerado para esperar.
Funcionamento: Você vende uma opção de venda (Put) e mantém o dinheiro necessário para a compra da ação garantido na corretora
Vantagem: Se a ação fechar acima do strike, você embolsa o prêmio como lucro puro
. Se cair abaixo, você é exercido e compra a ação pelo preço que já considerava vantajoso, descontando o prêmio recebido
Consistência: Deve ser feita apenas com empresas sólidas que você teria prazer em possuir no longo prazo
--------------------------------------------------------------------------------
3. Venda Coberta do "Homem Pobre" (PMCC)
Uma variação da venda coberta que exige muito menos capital, aumentando a eficiência financeira.
Estrutura: Em vez de comprar a ação, você compra uma Call Longa (vencimento em 6 a 12 meses) com strike "dentro do dinheiro" (ITM) e vende uma Call Curta (vencimento em 30 dias) com strike "fora do dinheiro" (OTM)
Análise: A Call longa substitui o ativo-objeto, servindo de cobertura para a venda mensal
. O lucro vem do decaimento temporal (Theta positivo) da opção curta vendida
--------------------------------------------------------------------------------
4. Estrutura de Proteção: Strangle Long Put
Para quem busca renda, mas teme movimentos bruscos de queda (Crashes), esta estrutura combina as duas frentes.
Execução: Venda de uma Call e uma Put (gerando renda por lateralidade) combinada com a compra de uma quantidade maior de Puts longas (Overhead)
Resultado: Em mercados laterais, você ganha com o tempo. Em quedas bruscas, as Puts longas valorizam exponencialmente, protegendo a desvalorização da sua carteira de ações
--------------------------------------------------------------------------------
Pilares para o Sucesso e Consistência
Aproveite a Volatilidade: O momento ideal para vender opções e coletar prêmios "gordos" é quando a Volatilidade Implícita (VI) está alta
. Vender com VI baixa oferece pouco retorno para o risco assumido
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
. O objetivo central é a geração de renda recorrente e a preservação do capital através de estruturas que utilizam o tempo a seu favor
Abaixo, apresento a análise e as sugestões de estruturas baseadas nos pilares de baixo risco e previsibilidade.

--------------------------------------------------------------------------------
1. Venda Coberta Tradicional (Financiamento)
Avaliação de Cenário: Esta operação é ideal para um cenário de mercado neutro a levemente altista
. Antes de iniciar, deve-se verificar se o ativo está em tendência de alta ou lateral através da média móvel de 20 períodos
. A volatilidade implícita (IV) deve estar preferencialmente alta (IV Rank acima de 50%) para garantir prêmios mais "gordos"
Explicação simples e objetiva: Você compra uma ação sólida e vende o direito de outra pessoa comprá-la de você por um preço fixo (strike) em uma data futura.
. Em troca, você recebe um valor em dinheiro imediatamente (prêmio)
Estrutura sugerida: Compra do ativo-objeto (ex: 1000 ações de PETR4) + Venda de Call Fora do Dinheiro (OTM) com strike acima do preço atual.
Riscos envolvidos: O risco oculto é o custo de oportunidade (se a ação subir muito, seu lucro é limitado ao strike) e o risco principal é a queda acentuada do ativo.
Pior cenário possível: O ativo desvalorizar drasticamente (ir a zero), superando a proteção conferida pelo prêmio recebido.
Possível manejo/ajuste: Caso o preço do ativo se aproxime do strike, pode-se realizar a rolagem: recomprar a Call atual e vender uma para o mês seguinte (série futura), coletando mais prêmio e evitando o exercício
--------------------------------------------------------------------------------
2. Venda de Put Garantida (Cash-Secured Put)
Avaliação de Cenário: Estrutura recomendada para cenários de lateralização ou leve baixa, em ativos que você deseja adquirir para o longo prazo.
. Deve-se evitar vender Puts quando a IV está no "piso" histórico, pois o risco assumido não compensa o prêmio baixo
Explicação simples e objetiva: Você é pago para se comprometer a comprar uma ação por um preço que considera justo.
. Se a ação não cair até esse preço, você fica com o prêmio como lucro puro
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

## Cicatrizes mapeadas:
1) Entrada em operações sem entendimento de volatilidade implícita
2) Uso incorreto de alavancagem
3) Falta de planejamento de saída (stop, alvo, rolagem)
4) Operações direcionais em cenários laterais
5) Ignorar efeitos de theta (tempo) contra a posição

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
