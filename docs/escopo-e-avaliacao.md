# Escopo e avaliação do ChefBot

[Voltar ao projeto](../README.md)

## Escopo consolidado

O ChefBot é um conceito de robô culinário de bancada para um catálogo de receitas compatíveis. O catálogo não é irrestrito: cada receita precisa especificar ingredientes, ferramentas, parâmetros, etapas humanas e condições de execução.

Salada e molho de tomate são exemplos narrativos de preparo frio e quente. Massa, sorvete e sobremesa aparecem nas ilustrações como possibilidades a estudar. Nenhuma dessas receitas foi executada por um protótipo do grupo.

As ações previstas incluem dosagem, transferência, mistura, montagem e, quando tecnicamente viável, sova e cocção. Lavagem e corte prévios dos ingredientes, operações em equipamentos não integrados e limpeza ficam com a pessoa. O trabalho não demonstra autonomia culinária geral.

## O que esta entrega contém

| Produzido | Natureza |
|---|---|
| Definição de problema, público e contexto | Delimitação conceitual |
| Mariana e Roberto, com mapas de empatia | Hipóteses de design |
| Análise de concorrência e referências | Pesquisa documental |
| Forma, esboços e imagens | Representações conceituais; cotas preliminares |
| Jornada, ações, estados e comunicação | Especificação proposta |
| Apresentação e roteiro | Comunicação do projeto |

## O que ainda não foi realizado

Implementação de interface funcional, sensores, manipuladores, software de execução ou integração térmica; entrevistas ou observações com participantes; testes de usabilidade; ensaios físicos; avaliação de risco concluída; certificação.

Não há resultados quantitativos de desempenho, redução de tempo ou aceitação a reportar. As necessidades das personas são hipóteses que precisam ser confrontadas com usuários reais.

## Próxima etapa proposta

1. Revisar com potenciais usuários as hipóteses sobre rotina, compartilhamento da bancada e intervenção.
2. Construir um protótipo de papel ou interface navegável para salada e molho, sem atuação física.
3. Executar um estudo formativo de compreensão, com participantes consentindo e sem calor ou movimentos robóticos reais.
4. Revisar os estados, mensagens e divisão de responsabilidades a partir dos problemas observados.
5. Só depois especificar a implementação e a validação técnica necessárias para demonstrações físicas.

Blender, Unity, Python e ROS 2 foram considerados nos materiais de origem como possibilidades futuras. Nenhuma ferramenta é apresentada como já utilizada para implementar o ChefBot.

## Roteiro de avaliação futura

| Cenário | Tarefa proposta | Evidência a registrar |
|---|---|---|
| Receita fria | Selecionar salada, identificar as entradas e apontar como iniciar | Acertos e dúvidas sobre a divisão humano-robô |
| Receita com calor | Identificar o que muda no molho de tomate | Compreensão das condições adicionais e do calor residual |
| Informação | Localizar estado atual e pedir explicação | Tempo para encontrar a informação e interpretação da resposta |
| Entrada ausente | Resolver um recipiente faltante em uma simulação | Se entende a interrupção e o próximo passo |
| Cozinha compartilhada | Interpretar o pedido de liberação da bancada | Se sabe onde agir e quando aguardar |
| Pausa e erro | Diferenciar pausa, erro e emergência | Confusões entre controles e expectativas de retomada |
| Retomada | Indicar como continuar após corrigir a causa | Se espera revalidação e uma decisão deliberada |
| Encerramento | Reconhecer o fim e a responsabilidade pela limpeza | Clareza sobre o último contato |

Definir perfil e quantidade de participantes, procedimento e critérios antes da coleta. O estudo inicial deve buscar problemas de compreensão, sem usar uma pequena amostra para alegar aceitação da população. Não são apresentados percentuais de sucesso fictícios.

Segurança física exige ensaios e análise próprios. Uma pessoa sentir confiança ou entender o botão de emergência não demonstra que o sistema físico é seguro.
