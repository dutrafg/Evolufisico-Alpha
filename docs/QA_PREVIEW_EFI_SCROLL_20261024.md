# Prévia de integração EFI Intelligence + correção de rolagem tátil

**Status:** experimental / não homologada. **Destino:** branch `feature/efi-intelligence-scroll-preview-20261024`, sem modificações na `main`.

## Origem
- Base: EvoluFísico Alpha WidgetKit 0.2, recomposto das quatro partes em `source/`.
- Motores EFIA: `assets/efia/efia-anthropometry.js`, `efia-local.js` e `efia-host.js` obtidos da `main` do Evolufisico2.
- Motor EFI: `efi-intelligence/analyzer.mjs` e `fixtures.mjs` do Evolufisico-IA-WEB.
- Entrega: `previews/EvoluFisico2_Alpha_EFI_RC1_Scroll_20261024.html` (~1,97 MB, arquivo único).

## Funcionalidades incorporadas
1. Área EFI dentro do módulo Análises, mantendo o restante da interface original.
2. Seleção de aluno com identidade explícita, objetivo e 3 a 4 avaliações.
3. Análise de registros reais somente quando o adaptador EFIA autorizar a interpretação; veto das auditorias preservado.
4. Dados sintéticos separados e explicitamente identificados para demonstração.
5. Indicadores de peso, cintura, gordura corporal estimada e massa livre de gordura, com limitações e avisos.
6. Parecer editável e opção de copiar o texto.
7. Ajuste de `touch-action:pan-y pinch-zoom` e `overscroll-behavior-y:auto` para rolagem da página e listas internas dos widgets.
8. Em dispositivos com ponteiro grosso, desabilitação do arraste HTML nativo nos cartões; reordenação permanece nos controles ← / → do modo de edição.

## Verificações efetuadas
- Fonte recomposta possui marcação final `</html>`.
- CSS inserido no fechamento da seção `head` externa; scripts inseridos antes do `body` externo, sem alterar os documentos HTML internos.
- Core de IA possui exportação ao objeto global `EFIIntelligenceCore`.
- Arquivo foi criado no GitHub em branch de teste e sua existência/tamanho foram verificados.
- Não houve publicação na `main` ou deploy de produção.

## Homologação pendente
- Abertura e testes interativos reais no Firefox/Chrome/Android.
- Rolagem vertical em widgets pequenos, médios, grandes e extragrandes; listas internas com e sem conteúdo.
- Modo Editar ligado/desligado, arraste no desktop, botões de reordenação no tablet/smartphone.
- Seleção de alunos reais, 3 ou 4 datas e bloqueio por identidade/método incompatível.
- Compatibilidade completa do adaptador EFIA RC2.4 com a versão Alpha antiga; o runtime pode bloquear análises corretamente quando dependências não estiverem compatíveis.
- Modo claro/escuro, PDF, persistência, PWA e backup com teste de regressão.
- Modelo de linguagem generativo e gerenciador de componentes ONNX/WASM: **não incluídos**. A EFI incorporada é determinística e offline; modelos e runtimes grandes ainda não foram publicados/homologados.

**Não declarar versão estável antes dos testes físicos e da integração com a main mais recente do Evolufisico2.**
