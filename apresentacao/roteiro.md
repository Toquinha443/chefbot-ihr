# Roteiro de apresentação — ChefBot

Duração planejada: **15 minutos**, incluindo transições. Slides 17 e 18 são referências de apoio e não integram a fala cronometrada. O tempo é uma proposta para ensaio, não uma medição de apresentação realizada.

A ordem é Nicolas → Thiago → Rafael → Caroline (Carol). A divisão abaixo organiza a fala; todos assinam o projeto em conjunto. Ela não aparece nos slides.

| Pessoa | Slides | Intervalo | Tempo |
|---|---|---|---|
| Nicolas Kuhnast | 1–4 | 0:00–3:45 | 3min45 |
| Thiago Luppi Blumer | 5–8 | 3:45–7:30 | 3min45 |
| Rafael Simões Israel | 9–12 | 7:30–11:15 | 3min45 |
| Caroline Alves Barroso | 13–16 | 11:15–15:00 | 3min45 |

## Nicolas

### Slide 1 — ChefBot

**0:00–0:30 · 30 segundos**

Boa tarde. Nosso projeto é o ChefBot, um robô culinário colaborativo de bancada. O foco do trabalho é a interação: como ajudar no preparo de diferentes receitas e, ao mesmo tempo, manter a pessoa informada e no controle. Esta é uma proposta conceitual de IHR. As imagens ilustram a ideia; ainda não construímos nem testamos um robô físico.

### Slide 2 — O problema na cozinha

**0:30–1:30 · 60 segundos**

Começamos pelo contexto de cozinhar sem o ChefBot. A pessoa precisa separar ingredientes, acompanhar a sequência, observar o ponto dos alimentos e dividir a bancada com outras atividades. Uma interrupção pode fazer com que ela perca a etapa ou precise reler a receita. Para quem tem pouca experiência, essa coordenação também pode gerar insegurança. Para quem já cozinha, o desafio pode ser manter seus hábitos enquanto divide o espaço. Nosso problema não é apenas automatizar movimentos. Queremos entender como reduzir o esforço de acompanhamento e tornar a colaboração compreensível. Essas situações orientam nossas hipóteses; não são resultados de entrevistas.

### Slide 3 — Objetivo e recorte do projeto

**1:30–2:30 · 60 segundos**

A pergunta que orienta o projeto é: como apoiar receitas variadas sem retirar da pessoa a compreensão e o controle do preparo? Delimitamos uma cozinha doméstica, um robô estacionário e receitas compatíveis com ferramentas e condições definidas. A variedade não significa fazer qualquer prato. Usamos salada e molho de tomate para contrastar um preparo frio com outro que envolve calor. O conteúdo de cada receita muda, mas a lógica de escolha, acompanhamento e intervenção deve continuar familiar. A entrega desenvolve esse conceito e suas interações. Implementação, testes com usuários e validação física ficam como próximos passos, sem serem apresentados como já realizados.

### Slide 4 — Pessoas e papéis

**2:30–3:45 · 75 segundos**

Para explorar esse contexto, construímos duas personas hipotéticas. Mariana tem 28 anos, rotina corrida e experiência culinária básica. Ela representa a pessoa que prepararia as entradas e acompanharia o uso cotidiano. Sua necessidade principal é concluir a refeição sem se perder na sequência. Roberto tem 52 anos, cozinha com experiência e ajuda ocasionalmente na cozinha compartilhada. Ele quer entender o preparo, preservar preferências e colaborar sem atrapalhar. A distinção é de papel naquele cenário: uma mesma pessoa poderia assumir outro papel em outro momento. Também consideramos quem limpa ou faz manutenção e quem consome a refeição sem operar o robô. O Thiago vai aprofundar a rotina dessas personas, ainda sem o ChefBot, por meio dos mapas de empatia.

## Thiago

### Slide 5 — Mariana: antes do ChefBot

**3:45–4:40 · 55 segundos**

Este mapa descreve Mariana cozinhando sem o robô. Ela vê ingredientes, louça, uma receita no celular e pessoas circulando. Ouve água, exaustor e conversas. Ela separa itens, relê instruções e alterna tarefas. Ao mesmo tempo, quer conciliar a refeição com seus horários e fica insegura quando perde uma etapa. As dores são o tempo curto, as interrupções e a sequência confusa. O ganho desejado é acompanhar o preparo com menos esforço e perceber quando precisa agir. Reparem que aqui não há comandos, telas ou respostas do ChefBot. Primeiro mapeamos a situação e a necessidade; depois formulamos a solução. Esses itens são hipóteses a investigar.

### Slide 6 — Roberto: antes do ChefBot

**4:40–5:35 · 55 segundos**

O mapa de Roberto também parte da cozinha sem o robô. Ele vê utensílios familiares, ingredientes e outra pessoa ocupando a bancada. Ouve pedidos de ajuda e preferências da família. Costuma conferir ingredientes e observar a consistência. Valoriza seu modo de cozinhar e quer entender por que uma etapa acontece. Suas dores são perder acesso ao espaço e não saber quando intervir. O ganho desejado é ajudar sem atrapalhar e preservar seus hábitos. Assim, o mapa não afirma que ele já usou uma automação ou reagiu a ela. Ele organiza o contexto anterior que usaremos para decidir como a colaboração deve funcionar.

### Slide 7 — Necessidades orientam o design

**5:35–6:35 · 60 segundos**

Agora transformamos as necessidades mapeadas em decisões para o ChefBot. A dificuldade de acompanhar etapas sugere estado resumido e informação fácil de consultar. A necessidade de compreender o preparo sugere explicações sob demanda. A cozinha compartilhada exige pedidos claros e indicação de quando a pessoa pode participar. Adotamos dois padrões de interação: comunicação didática e recuperação de erros. Eles se combinam quando falta um utensílio: o robô informa o que falta, explica por que precisa dele e aguarda a correção. Depois revalida as condições antes da retomada. As funcionalidades aparecem nesta etapa como propostas do projeto, sem serem confundidas com aquilo que as personas já fazem ou sentem.

### Slide 8 — Referências de outras plataformas

**6:35–7:30 · 55 segundos**

Comparamos três referências robóticas e uma alternativa de preparo. Moley integra automação ao ambiente da cozinha e ajuda a pensar a relação entre manipulação e espaço. Posha é uma referência próxima para a rotina doméstica de carregar ingredientes e acompanhar uma receita. BOTINKIT Omni mostra sequência, dosagem e controle térmico em uma operação comercial. Como alternativa, Thermomix oferece preparo guiado em um aparelho multifunção. Os mercados e as configurações são diferentes. Nossa comparação é documental, baseada nos fornecedores; não fizemos testes de desempenho. Para o ChefBot, destacamos comunicação e controle na cozinha compartilhada. O Rafael vai mostrar como essas necessidades se traduzem na forma e no funcionamento proposto.

## Rafael

### Slide 9 — Forma e função

**7:30–8:25 · 55 segundos**

O ChefBot foi pensado como uma unidade estacionária de bancada, com dois braços e uma face digital simples. Os braços sugerem manipulação, e a face ajuda a sinalizar atenção; ela não comprova compreensão humana. A interface de receita e os controles de pausa e emergência precisam ser identificáveis e distintos. Também propomos texto legível, voz ajustável e comunicação que não dependa apenas de cor ou fala. O esboço usa formas primitivas para discutir essa organização. As dimensões, como a altura de 700 milímetros, são preliminares e não servem para fabricação. Quando houver calor, o cooktop fica separado, ao lado da base.

### Slide 10 — Jornada de uma receita

**8:25–9:25 · 60 segundos**

Na jornada proposta, a pessoa escolhe uma receita e recebe a lista de entradas e etapas humanas. Ela lava, corta e disponibiliza os ingredientes; o sistema verifica as condições previstas antes de iniciar. Durante o preparo, o estado fica visível e explicações podem ser solicitadas, sem pedir confirmação de todo movimento rotineiro. Se uma etapa depender da pessoa, o robô faz um pedido claro e aguarda. Na salada, estudamos transferência, mistura e montagem. No molho de tomate, acrescentamos cocção e requisitos térmicos. A interação é consistente, mas as condições não são iguais: parar um braço não elimina calor residual. A conclusão também depende de critérios definidos para cada receita.

### Slide 11 — Ações, estados e limites

**9:25–10:25 · 60 segundos**

A arquitetura conceitual separa a interface, o catálogo de receitas, a percepção, o planejamento e a atuação. Uma receita estrutura as ações e suas pré-condições: misturar, por exemplo, depende de ferramenta, recipiente e parâmetros definidos. O fluxo passa por selecionar, verificar, executar e concluir. Há ainda espera por ajuda, pausa e tratamento de falha. Consulta e explicação são funções sobre o estado atual: perguntar o que está acontecendo não deve apagar o estado de execução nem liberar movimento. Um eventual modelo de linguagem só apoiaria explicações. Após falha ou emergência, não há retomada automática; a causa precisa ser resolvida, as condições revalidadas e a continuação deliberada pela pessoa.

### Slide 12 — Espaço compartilhado

**10:25–11:15 · 50 segundos**

Como o ChefBot é fixo, quem se aproxima é a pessoa. Propomos uma formação em L, com ambos orientados para a mesma região da bancada. Essa área de atenção é o o-space; a circulação fica fora dela. Usamos proxêmica para discutir conforto social, sem transformar suas distâncias em limites de segurança. Se alguém ocupar o espaço de trabalho, a proposta é suspender a progressão e pedir liberação. O robô não atravessa grupos nem corredores, e os braços não devem passar entre pessoas. Em uma demonstração para a turma, separaríamos operador e observadores. A Carol vai concluir com comunicação, emoções e avaliação.

## Caroline

### Slide 13 — Comunicação multimodal

**11:15–12:15 · 60 segundos**

Na comunicação verbal, escolhemos comandos restritos e vinculados aos estados. Exemplos são selecionar uma receita, consultar o estado, pedir explicação e pausar. A voz proposta é clara e calma, em português brasileiro. Quando houver demora, o sistema informa que está verificando, sem deixar a pessoa em silêncio sem retorno. Como a cozinha tem ruído, voz não pode ser a única via de controle. Na comunicação não verbal, usamos olhar e postura dos braços: olhar indica atenção e destino; o recolhimento ajuda a entregar o turno à pessoa. Fala, gesto e estado precisam concordar. Dizer que alguém pode colocar um recipiente enquanto o braço atravessa o local seria uma quebra dessa coordenação.

### Slide 14 — Emoção e valores

**12:15–13:15 · 60 segundos**

O modelo de Russell oferece dois eixos para pensar o afeto: valência e ativação. Usamos essa referência para projetar respostas, sem afirmar que o robô detecta emoções com precisão. A prioridade é o que a pessoa comunica. Diante de uma dúvida, ele pode oferecer explicação; diante de irritação, deve manter um tom calmo. Pode acompanhar uma satisfação com uma expressão breve, mas não imitar raiva ou ansiedade. Sinais de processamento e erro continuam sendo estados operacionais, não sentimentos. Os valores principais são autonomia humana e segurança. O risco é a face amigável gerar confiança excessiva. Por isso, a interação deve comunicar limites e manter a possibilidade de intervenção.

### Slide 15 — O que temos e como avaliar

**13:15–14:15 · 60 segundos**

O resultado deste trabalho é a especificação conceitual: problema, contexto, personas, mapas, referências, forma e interações. Não temos hardware, software de execução ou resultados de testes com participantes. A próxima etapa seria um protótipo de interface ou storyboard para verificar compreensão. Pediríamos, por exemplo, que a pessoa selecionasse uma receita, identificasse a etapa atual e resolvesse uma entrada ausente. Também observaríamos se distingue pausa, erro e emergência e entende como retomar. Registraríamos dúvidas, erros de interpretação e tempo para encontrar os controles, com critérios definidos antes da coleta. Ensaios físicos viriam depois de análise e validação técnica; confiança percebida não é prova de segurança.

### Slide 16 — Contribuição e próximos passos

**14:15–15:00 · 45 segundos**

A contribuição do ChefBot é propor uma colaboração compreensível entre pessoa e robô na cozinha. Partimos de hipóteses sobre a rotina sem o produto, traduzimos necessidades em requisitos e organizamos uma interação que possa ser reutilizada em receitas diferentes. O fio condutor é manter etapa, ajuda e controle claros. O próximo passo é confrontar essas hipóteses com usuários e revisar a proposta em um protótipo de interação, antes de avançar para atuação física. O repositório reúne o detalhamento e as referências. Obrigada; ficamos à disposição para as perguntas.

## Pontos para o ensaio e as perguntas

- Os mapas retratam a rotina sem ChefBot. As funcionalidades aparecem depois como resposta às necessidades.
- Personas e falas são hipóteses autorais, não entrevistas.
- O projeto trata de receitas variadas compatíveis; molho de tomate é um exemplo.
- O repositório é documental; não há software ou hardware funcional a demonstrar.
- Não atribuir economia de tempo, aceitação ou segurança a testes que não ocorreram.
- Se for necessário encurtar, resumir os exemplos verbais; preservar o encadeamento contexto → necessidades → decisões → avaliação.
- Perguntas sobre execução física: as imagens e cotas são preliminares; viabilidade, riscos e integração são etapas futuras.
- Perguntas sobre mapas antes de personas: mantivemos a ordem de exposição do template, mas o conteúdo dos mapas é anterior à solução.
