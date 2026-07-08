**Título do projeto:** Modelação e Análise Dinâmica de um Mecanismo de Leg Press

O objetivo deste projeto foi desenvolver uma análise biomecânica e dinâmica de um exercício de **leg press**, modelado como um **mecanismo plano de quatro barras com junta de translação**. O trabalho permitiu estudar a interação entre os membros inferiores e a plataforma da máquina, aplicando conceitos de cinemática, dinâmica de sistemas multicorpo e formulação Newton-Euler.

O relatório final contém a introdução ao problema, a formulação teórica do mecanismo, a determinação dos graus de liberdade, a definição das condições iniciais, a formulação das equações de movimento, a implementação computacional em MATLAB, a simulação dinâmica, a animação do sistema e a análise dos resultados obtidos.

O sistema foi modelado considerando três corpos principais: a **coxa**, o conjunto **perna-pé** e a **plataforma deslizante da máquina de leg press**. Através da análise estrutural do mecanismo, concluiu-se que o sistema possui **um grau de liberdade**, o que significa que o movimento global pode ser descrito a partir de uma única variável independente.

Foram definidos parâmetros geométricos e antropométricos para representar o utilizador e o mecanismo: comprimento da coxa de 0,39 m, comprimento do conjunto perna-pé de 0,45 m, comprimento da junta de translação de 0,70 m, massa corporal de 65 kg, altura de 1,67 m e massa da plataforma de 60 kg. Com base nestes dados, foram calculadas as massas segmentares, os momentos de inércia e as posições iniciais dos centros de massa.

A análise dinâmica foi desenvolvida com base na **formulação de Newton-Euler**, combinada com **multiplicadores de Lagrange** para impor os constrangimentos geométricos do sistema. Esta abordagem permitiu garantir a ligação entre os segmentos corporais e a plataforma, respeitando as articulações da anca, joelho e tornozelo, bem como a guia linear da máquina de leg press.

Foram formuladas as equações de movimento para a coxa, para o conjunto perna-pé e para a plataforma. Paralelamente, foram definidas as equações de constrangimento, a matriz Jacobiana, o vetor do lado direito das acelerações e o vetor das forças generalizadas. O modelo incluiu a ação da gravidade e uma força externa de **900 N** aplicada à plataforma, representando a resistência exercida durante o movimento.

A implementação computacional foi realizada em **MATLAB**, através de vários ficheiros organizados por função. O código define as condições iniciais, constrói a matriz de massa global, calcula a matriz Jacobiana, determina o vetor das forças generalizadas, calcula o vetor gama, resolve o sistema aumentado das equações de movimento e integra numericamente a evolução temporal do mecanismo.

A integração temporal foi realizada pelo **método de Euler explícito**, usando um passo de integração reduzido, h = 0.00005, para garantir estabilidade numérica. O relatório documenta a simulação para um **intervalo temporal de 5 segundos**, enquanto o código disponibilizado no repositório pode apresentar o parâmetro tfinal ajustado para valores inferiores, como **1 segundo**, com o objetivo de testar o comportamento do modelo, observar a influência do tempo de simulação e facilitar a visualização inicial da resposta dinâmica. Para reproduzir a simulação descrita no relatório, basta definir tfinal = 5 no ficheiro de integração.

Foi ainda desenvolvida uma animação em MATLAB para visualizar o movimento do mecanismo ao longo do tempo. A animação representa a coxa, a perna-pé, a plataforma deslizante e as respetivas juntas, permitindo verificar visualmente a coerência do movimento e o cumprimento dos constrangimentos impostos ao sistema.

Os resultados mostraram que o movimento obtido é fisicamente coerente: a plataforma desloca-se ao longo da guia linear, enquanto os segmentos corporais acompanham o movimento mantendo a ligação entre anca, joelho e tornozelo. A aplicação da força externa permitiu analisar a transmissão do esforço através das barras articuladas e observar a resposta dinâmica do mecanismo.

A equipa concluiu que o modelo desenvolvido permite representar adequadamente o comportamento dinâmico do exercício de leg press, demonstrando a utilidade da dinâmica de sistemas multicorpo na análise biomecânica. Apesar de o método de Euler ser uma abordagem simples, os resultados obtidos foram considerados estáveis e consistentes para uma análise preliminar.

Como possíveis melhorias futuras, foram identificadas extensões como a inclusão de modelos musculares ativos, forças de contacto mais realistas, estratégias de controlo motor e análise das cargas articulares. Estas melhorias permitiriam aproximar o modelo de uma situação biomecânica mais realista e aprofundar a avaliação da performance e da prevenção de lesões no contexto do treino de força.

**Conteúdos deste repositório:**

- Relatório final em PDF — documento completo com introdução, formulação Newton-Euler, análise dinâmica, implementação MATLAB, resultados e conclusões.
- Apresentação final em PDF — slides usados na apresentação do projeto.
- Pasta MATLAB “Leg Press” — código fonte utilizado para simular e animar o mecanismo.
- condictions.m — definição das condições iniciais, parâmetros geométricos e antropométricos do sistema.
- matriz.m — construção da matriz de massa global.
- jacobian.m — cálculo da matriz Jacobiana dos constrangimentos.
- vetor_g.m — definição do vetor das forças generalizadas, incluindo gravidade e força externa aplicada à plataforma.
- vetor_gamma.m — cálculo do vetor associado às acelerações dos constrangimentos.
- integracao.m — resolução do sistema aumentado e integração temporal pelo método de Euler.
- animacao.m — visualização gráfica e animação do movimento do mecanismo de leg press.

Nota sobre o tempo de simulação:

O relatório apresenta a simulação desenvolvida para um intervalo temporal de 5 segundos. No código disponibilizado no repositório, o parâmetro tfinal pode surgir ajustado para valores inferiores, como 1 segundo, de forma a estudar o efeito da duração da simulação no comportamento dinâmico do mecanismo, facilitar testes rápidos e avaliar a estabilidade da integração numérica. Para reproduzir diretamente a simulação apresentada no relatório, deve definir-se tfinal = 5 no ficheiro integracao.m.

Este trabalho foi importante para consolidar conhecimentos em **biomecânica**, **dinâmica de sistemas multicorpo**, **modelação computacional** e **simulação em MATLAB**, aplicando ferramentas de engenharia mecânica à análise do movimento humano e da interação com equipamentos de exercício físico.

Projeto realizado por Ana Beatriz Pereira, Anita Faustino, Bárbara Ribeiro, Jéssica Soares e Matilde Serra, no âmbito da unidade curricular de Biomecânica, do Mestrado em Engenharia Biomédica — Biomateriais, Reabilitação e Biomecânica, lecionada pelo Professor Paulo Flores. **Classificação final: 18,7 valores.**
