# Redação do Projeto: Portfólio Pessoal & Jogos Educativos
**Aluna:** Mayara Barboza Silva  
**Programa:** Programa Trilhas (FAPEMA / SECTI)  
**Trilha:** Desenvolvimento Front-end  
**Repositório:** [https://github.com/mayarabarbosasilva1999-sudo/portifolio-mayara](https://github.com/mayarabarbosasilva1999-sudo/portifolio-mayara)  
**Site Publicado:** [https://mayarabarbosasilva1999-sudo.github.io/portifolio-mayara/](https://mayarabarbosasilva1999-sudo.github.io/portifolio-mayara/)  

---

## 1. Introdução e Objetivo do Desafio

O presente projeto consolida os conhecimentos práticos adquiridos nos módulos de **Fundamentos da Web (HTML5)**, **CSS: Estilização e Layout**, e **Controle de Versão com Git e GitHub** do Programa Trilhas. 

O objetivo principal foi construir uma página de apresentação pessoal e profissional (portfólio) responsiva, intuitiva e acessível, baseando-se estritamente nas diretrizes visuais e arquiteturais disponibilizadas no protótipo do Figma. Além de apresentar a biografia e trajetórias da desenvolvedora — que une a formação em Enfermagem pela Universidade Estadual do Maranhão (UEMA) e a formação em UX/UI Designer pelo Programa Trilhas —, o projeto expandiu seu escopo técnico ao incorporar uma suíte de **16 jogos educativos interativos** voltados ao aprendizado infanto-juvenil, divididos em quatro áreas fundamentais do conhecimento: Matemática, Língua Portuguesa, Ciências e Lógica de Programação.

---

## 2. Decisões Arquiteturais e Estrutura do Projeto

A arquitetura do projeto foi planejada sob os princípios de **modularidade**, **manutenibilidade** e **performance sem dependências externas pesadas (Vanilla Web)**.

### 2.1. Estruturação Semântica em Páginas (Multi-Page Architecture)
Optou-se por uma arquitetura multi-page onde cada responsabilidade de conteúdo reside em um documento semanticamente bem definido:
- **`index.html` (Página Inicial):** Ponto de entrada limpo com foco no perfil da desenvolvedora, fotografia pessoal otimizada, links principais de navegação, ícones de redes sociais e crédito institucional.
- **`sobre.html` (Sobre Mim):** Apresentação aprofundada da trajetória profissional e acadêmica (UEMA e Trilhas UX/UI), propósito de atuação em saúde digital, matriz de competências técnicas e canais de contato.
- **`projetos.html` (Galeria de Projetos):** Grid 2x2 responsivo que funciona como vitrine central para os ecossistemas de projetos desenvolvidos.
- **`certificados.html` (Acesso a Certificados):** Interface de redirecionamento integrado para o repositório em nuvem no Google Drive, com preview visual temático.

### 2.2. Modularização dos Módulos Educativos
Para os projetos práticos, adotou-se uma estrutura de pastas hierárquica e auto-contida:
- Cada disciplina (`matematica/`, `portugues/`, `ciencias/`, `programacao/`) dispõe de uma página-hub (`index.html`) que lista as aplicações disponíveis e contextualiza os objetivos pedagógicos.
- Cada jogo foi implementado como uma aplicação independente em seu próprio diretório, facilitando atualizações isoladas, testes unitários de interface e permitindo futura componentização.

---

## 3. Design System e Implementação Visual (Figma to Code)

A estilização foi orientada a reproduzir com rigor métrico o layout do Figma:

1. **Paleta de Cores e Gradiente Mesh:**
   - O fundo da aplicação reproduz o degradê suave e moderno com múltiplos pontos focais radiais (`radial-gradient` sobrepostos), mesclando tons de lilás (`#c4a6e9`), rosa suave (`#ecafe8`) e azul translúcido (`#d6dff7`) com fundo fixo (`background-attachment: fixed`), garantindo uma estética suave e profissional.
   - Os cartões e botões utilizam a cor `#ebdceb` com contorno de contraste moderado (`#7d6b82`), preservando a harmonia cromática do design de referência.

2. **Tipografia e Escala:**
   - Utilização da família tipográfica **Inter** (via Google Fonts), padronizando a legibilidade em diferentes densidades de tela e mantendo hierarquias visuais claras entre títulos (`h1`, `h2`), descrições e botões.

3. **Responsividade (Mobile-First & Fluid Grid):**
   - Implementação de layouts baseados em **CSS Flexbox** e **CSS Grid**. No desktop, a grade de projetos organiza-se no formato bidimensional 2x2; em dispositivos móveis (`max-width: 580px`), as regras de Media Queries reorganizam o fluxo para coluna única (1fr), evitando rolagem horizontal indesejada e garantindo ergonomia ao toque.

4. **Rodapé e Assinatura:**
   - Implementação da seção de rodapé com ícones vetoriais inline em SVG para GitHub, LinkedIn e E-mail, acompanhados da linha de crédito oficial: *"Feito com ❤ por Mayara Barboza Silva"*.

---

## 4. Engenharia e Lógica Interativa (JavaScript & Web Audio)

Os 16 jogos educativos foram construídos utilizando **JavaScript Moderno (ES6+)**, explorando conceitos fundamentais de desenvolvimento Front-end:
- **Manipulação Dinâmica do DOM:** Criação dinâmica de elementos, renderização de matrizes para o caça-palavras e labirinto, e embaralhamento randômico de arrays para alternativas múltiplas.
- **Sistemas de Estado e Feedback:** Controle de pontuação, sequências de acertos (*combos*), temporizadores decrescentes e contagem de vidas/tentativas.
- **Efeitos Sonoros Nativos com Web Audio API:** Em vez de carregar arquivos externos de áudio (como MP3), foram desenvolvidos osciladores nativos sintetizados via código (`OscillatorNode` e `GainNode`), emitindo frequências agudas e harmônicas para acertos e tons graves para erros. Essa abordagem garante carregamento instantâneo, independência de rede e zero consumo de banda adicional.

---

## 5. Ferramentas Utilizadas

| Ferramenta | Finalidade no Projeto |
| :--- | :--- |
| **HTML5** | Estruturação semântica, acessibilidade e SEO básico. |
| **CSS3** | Estilização avançada, mesh gradient, Flexbox, Grid e Media Queries. |
| **JavaScript (ES6+)** | Lógica de programação, interatividade e integração com Web Audio API. |
| **Git** | Sistema de controle de versão distribuído e histórico de commits. |
| **GitHub & GitHub Pages** | Hospedagem de código-fonte e publicação contínua em nuvem (deploy do site estático). |
| **Visual Studio Code (VS Code)** | Ambiente de desenvolvimento integrado para escrita e depuração de código. |
| **Figma** | Ferramenta de UI/UX utilizada para inspeção de tipografia, cores e espaçamentos. |
| **Google Drive** | Armazenamento e disponibilização dos certificados de conclusão e workshops. |

---

## 6. Conclusão e Aprendizados

O desenvolvimento deste portfólio representou uma experiência prática completa do ciclo de vida de uma aplicação Front-end — desde a interpretação de especificações no Figma, estruturação e componentização semântica, até a publicação em ambiente de produção via GitHub Pages.

A integração de temas de saúde e educação através dos jogos educativos evidencia a aplicabilidade do Design Centrado no Usuário (UX/UI) aliado à engenharia Front-end, resultando em uma solução robusta, funcional e alinhada às expectativas acadêmicas e de mercado do Programa Trilhas.
