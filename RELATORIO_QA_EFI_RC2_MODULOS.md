# EvoluFísico 2 + EFI — RC2 de recuperação dos módulos

Data: 2026-10-24

## Diagnóstico
A primeira prévia RC1 havia sido construída sobre a base Alpha 0.2. Ela não corresponde ao runtime atual do EvoluFísico 2 e foi reprovada para testes operacionais.

## Correção realizada
- Nova base: `Evolufisico2/main`, versão 2.0.28 Pré-Beta, arquivo completo e motores existentes preservados.
- WidgetKit Alpha isolado, mantendo o modo Pro da versão principal.
- EFI RC1 (motor determinístico) integrado ao módulo Análises; 3 ou 4 avaliações; bloqueio de auditorias e identidade obrigatória.
- Correção de rolagem nos miniaplicativos: `touch-action: pan-y pinch-zoom`, continuidade de rolagem em listas, arraste nativo desativado em telas de toque. Botões de rearranjo permanecem.
- Arquivos de distribuição pública: `EvoluFisico2_EFI_RC2_FUNCIONAL.html` e `EvoluFisico2_EFI_RC2_FUNCIONAL.zip` (ZIP contém somente o HTML).
- A `main` do EvoluFísico 2 e a do Alpha não foram alteradas.

## Testes de integração executados
- Análise estática: 77 scripts JavaScript sem erros de sintaxe.
- Motor EFI: os três perfis sintéticos produziram análises; identificação incompatível provocou bloqueio.
- GitHub Actions / Chromium: **sucesso**, sem erros JavaScript coletados.
- Nove rotas de módulos existentes verificadas (Início, Organização, Avaliações, Evolução, Calculadora, Formulários, Análises, Cobranças e Configurações).
- WidgetKit e Dock iniciados, quatro indicadores EFI demonstrativos calculados.
- Clique real na Dock abriu Avaliações.
- Layout móvel sem overflow horizontal.
- Gesto de toque real (Chrome DevTools Protocol) movimentou a página **652 px** no teste.

[Relatório da execução automatizada](https://github.com/dutrafg/Evolufisico2/actions/runs/40101388591)

## Limitações
- RC2 é uma **prévia candidata para teste**, não liberação estável. Fluxos funcionais de todos os módulos, backup, geração de PDF, PWA offline e navegadores reais Android/Firefox ainda exigem homologação de regressão.
- A IA presente é o núcleo **determinístico** EFI. Modelo generativo, ONNX/WebGPU e pacote de pesos offline não estão incorporados.
- Na execução em arquivo `file://`, disponibilidade de persistência de dados pode variar por navegador; usar HTTPS/PWA no teste definitivo.
