# Fluxo e arquitetura conceitual

[Voltar ao projeto](../README.md)

## Divisão de responsabilidades

| Pessoa | ChefBot proposto |
|---|---|
| Escolher receita, porções e preferências | Apresentar requisitos e limites |
| Lavar/cortar e disponibilizar ingredientes | Verificar as entradas pelos meios especificados |
| Providenciar utensílios e equipamentos | Executar as ações previstas e informar o estado |
| Realizar etapas externas ou não integradas | Pedir ajuda de forma explícita e aguardar |
| Decidir pela retomada após correção | Revalidar condições e impedir retomada indevida |
| Retirar o preparo e limpar conforme procedimento | Informar conclusão e condição final prevista |

## Organização funcional

~~~mermaid
flowchart LR
    U[Pessoa] --> I[Interface: receita, estado e controles]
    I --> P[Planejador e máquina de estados]
    R[Catálogo de receitas e ações] --> P
    S[Percepção de entradas e ambiente] --> P
    P --> A[Atuação: braços, ferramentas e equipamentos]
    P --> E[Explicações vinculadas ao estado]
    E --> I
    G[Verificação de condições e limites] --> P
    G --> A
~~~

Esta é uma separação conceitual de funções, sem módulos implementados. Um modelo de linguagem, se incorporado futuramente, só apoiaria a explicação de dados disponíveis. Ele não deve produzir diretamente comandos de atuação nem declarar pré-condições como satisfeitas.

## Estados propostos

~~~mermaid
stateDiagram-v2
    [*] --> Espera
    Espera --> Selecao: escolha intencional
    Selecao --> Verificacao: entradas apresentadas
    Verificacao --> AguardaEntrada: ausência ou incompatibilidade
    AguardaEntrada --> Verificacao: correção
    Verificacao --> Execucao: condições verificadas e início confirmado
    Execucao --> AguardaPessoa: etapa manual prevista
    AguardaPessoa --> Verificacao: etapa informada como concluída
    Execucao --> Pausa: comando de pausa
    Pausa --> Verificacao: pedido de continuar
    Execucao --> Erro: falha detectada
    Erro --> Verificacao: causa resolvida e pedido humano
    Execucao --> Emergencia: evento de emergência
    Emergencia --> Verificacao: recuperação autorizada e condições restabelecidas
    Execucao --> Conclusao: critérios atendidos e condição final verificada
    Conclusao --> Espera: encerramento
~~~

O diagrama destaca as transições do preparo. Eventos de emergência também devem ter prioridade nos demais estados em que houver risco ou energia ativa. A resposta física de cada transição precisa ser especificada por tarefa e equipamento.

**Consulta de estado e explicação:** são funções disponíveis sobre o estado operacional, e não um estado que substitui “executando” ou “pausado”. Uma explicação pode ocorrer enquanto a receita continua, desde que isso seja apropriado à tarefa. Consultar informação não autoriza movimento, não muda parâmetros e não suspende proteções.

**Pausa:** suspende a progressão da receita e aplica a resposta prevista para os movimentos e equipamentos. Isso não implica, por si só, que tudo esteja desenergizado ou frio.

**Erro:** informa a causa conhecida, interrompe a progressão e exige correção e revalidação.

**Emergência:** aplica a resposta definida pela análise técnica. O restabelecimento de um controle não equivale a iniciar movimento novamente; recuperação e retomada são deliberadas.

## Dados de uma receita

Cada receita precisaria conter nome, porções, ingredientes e quantidades, utensílios, equipamentos, ações, parâmetros, pré-condições, critérios de término, etapas humanas e condições de interrupção. É uma necessidade de especificação, não uma API nem um catálogo executável nesta entrega.

| Exemplo | Entradas humanas | Ações a estudar | Diferença relevante |
|---|---|---|---|
| Salada | Ingredientes higienizados e cortados; recipientes e utensílios | Dosar, transferir, misturar e montar | Não exige aquecimento |
| Molho de tomate | Ingredientes preparados; panela e equipamento compatíveis | Dosar, transferir, misturar e realizar cocção | Exige tratamento de calor, vapor e fonte térmica |

## Segurança e comunicação

As verificações devem tratar colisão, aprisionamento, ferramentas, estabilidade e contaminação; receitas quentes acrescentam calor e respingos. Pausa e emergência precisam de alternativa à voz. Comandos ambíguos não iniciam nem retomam o preparo.

A [ISO 12100:2010](https://www.iso.org/standard/51528.html) fundamenta a necessidade de apreciação e redução de risco; a citação não significa conformidade do ChefBot. Proxêmica é referência social, não cálculo de distância segura. O alcance nominal de 350 mm também não é um limite de separação validado.
