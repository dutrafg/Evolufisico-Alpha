# WidgetKit Alpha 0.2.0 — iPadOS-inspired

## Escopo
- O Modo Pro permanece no código original; o Modo Moderno é selecionado em Configurações → Personalização.
- A Dock continua restrita aos nove módulos originais, com navegação Estendida e sem barra lateral no Moderno.
- Widgets em 4 tamanhos: Pequeno, Médio, Grande e Extragrande. O seletor de tamanho fica no próprio widget e a escolha é persistida localmente. A família maior revela mais listas, filtros e gráficos quando há dados.
- Pilhas continuam opcionais, agora também redimensionáveis; nenhuma pilha inicial é instalada.
- Tarefas: consulta do armazenamento nativo de Organização e criação/conclusão no widget.
- Avaliações: contagens reais, alunos, datas e registros recentes, sem inventar indicadores.
- Evolução: seleção de aluno e gráfico de peso obtido de avaliações existentes.
- Agenda: próximos eventos da Organização.
- Cobranças: resumo de registros com leitura pela API existente. Alterações de pagamentos continuam no módulo original.
- Calculadora: IMC dentro do widget com validação de peso e altura.
- Notas: listagem do módulo Organização; edição completa no módulo original.
- Outras opções da biblioteca continuam sendo resumos ou atalhos para funções que exigem a tela completa.

## Verificações executadas
- Sintaxe do JavaScript principal do Modo Moderno: `node --check` passou.
- Geração de conteúdo para 7 tipos de widget em quatro tamanhos (28 combinações), via VM Node com dados simulados: sem erro.
- HTML gerado com código do aplicativo original e camada moderna integrada.
- Conferência do blob `index.html` no GitHub após publicação.

## Limitações da homologação
A execução ponta a ponta no Chromium da sessão não foi concluída porque o ambiente bloqueou navegação local; o fallback com conteúdo inline excedeu o tempo disponível. Portanto **não** se declara a interface visual, a persistência integrada, a navegação nem operações de cobrança como homologadas nesta atualização. Não inserir dados sensíveis reais até validação.
O ponto de partida clínico da versão Alpha ainda é o HTML original 1.0.30 Pré-Beta, separado da versão estável.

## Referências oficiais
- https://support.apple.com/pt-br/guide/ipad/ipad1b2665da/27/ipados/27
- https://developer.apple.com/design/human-interface-guidelines/widgets
- https://developer.apple.com/documentation/widgetkit/adding-interactivity-to-widgets-and-live-activities
