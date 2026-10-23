# EvoluFísico Alpha

Repositório de desenvolvimento **separado** da versão estável do EvoluFísico2.

## Como testar

Abra `index.html` no navegador (de preferência a partir de um servidor local, por exemplo `python -m http.server 8000`).

- **Pro:** mantém os módulos e a experiência original do aplicativo usado como base.
- **Moderno:** ativa o Dashboard com widgets, Dock Estendida e biblioteca de widgets.
- **Configurações → Personalização:** alterna entre Pro e Moderno.

A versão Alpha é um ambiente de homologação. Faça backup antes de importar dados reais; não utilize resultados em decisões clínicas sem validação.

## Estado e origem

A base de homologação é o HTML **EvoluFísico2 1.0.30 Pré-Beta**, com adaptações do Modo Moderno. Este repositório **não substitui nem sincroniza automaticamente** a branch `main` do repositório estável `dutrafg/Evolufisico2`.

## Principais decisões de UX

- Dock com os nove módulos originais, somente após a tela de abertura.
- Modo Moderno sem painel lateral, com navegação Estendida fixa.
- Início Moderno com widgets padrão dos módulos existentes.
- Pilhas disponíveis sob demanda, não pré-instaladas.
- Respeito aos temas claro e escuro, com preferências locais no navegador.

## Desenvolvimento

Modificações Alpha devem ocorrer **neste repositório**, não no estável. Não foi configurado deploy automático.
