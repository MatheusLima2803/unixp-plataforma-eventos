# UNIXP — Plataforma de Gestão e Comercialização de Ingressos Universitários

## Sobre o Projeto
O **UNIXP** é uma plataforma centralizada voltada para a divulgação, gerenciamento e comercialização de ingressos de eventos universitários. O ecossistema integra processos acadêmicos críticos, como a automação na emissão de certificados, resolvendo problemas crônicos de descentralização de informações e atrasos em validações de horas de extensão.

Este repositório contém o **Case de Engenharia de Requisitos e Design Centrado no Usuário (DCU)** do sistema.

---

## Equipe de Desenvolvimento
* Arnaldo Rocha
* Lucas Mota
* Matheus Marques
* Norton Almeida

## Estrutura do Projeto e Documentação

O projeto foi dividido em entregas acadêmicas complementares. Você pode acessar os relatórios técnicos completos na pasta `docs` ou pelos links diretos abaixo:

* 📄 **[Parte 1 — Engenharia de Requisitos & UX](docs/unixp-parte1.pdf):** * **Análise de Mercado:** Levantamento de impactos e *benchmarking* competitivo com ferramentas consolidadas (*Sympla* e *Cheers*).
  * **Coleta de Dados:** Aplicação de questionários estruturados com foco na integração de regras de negócio (monetização e validação acadêmica via **SIGAA**).
  * **Modelagem de Usuários:** Criação de perfis, cenários de interação de ponta a ponta e personas estruturadas (Acadêmica e Organizadora).
  * **Especificação de Engenharia:** Levantamento de Requisitos Funcionais (RF) e Não Funcionais (RNF) com metas de eficiência inferiores a 2 segundos para transações críticas.

* 📄 **[Parte 2 — Guia de Estilo & Fundamentação de IHC](docs/unixp-parte2.pdf):**
  * **Design Responsivo Duplo:** Guia de estilo completo focado em **Desktop** (alta densidade de dados e dashboards para organizadores) e **Mobile** (alto contraste, *touch targets* ampliados e chips de busca rápida para estudantes).
  * **Princípios da Gestalt:** Aplicação prática de conceitos de *Proximidade*, *Similaridade* e *Continuidade* na organização visual de cards de eventos e gráficos de vendas.
  * **Diretrizes e Critérios de IHC:** Implementação de conceitos de visibilidade do status do sistema (badges semânticos), antecipação de necessidades (exibição imediata de QR Codes) e equilíbrio entre controle e liberdade (alternância de perfis de usuário).
  * **Acessibilidade e Usabilidade:** Conformidade com diretrizes da **WCAG/ISO**, garantindo contraste para leitura sob luz solar, design minimalista e multimodalidade de informação (combinação de cores, formas e textos para usuários daltônicos).

* 📄 **[Parte 3 — Métodos de Inspeção & Avaliação Heurística](docs/unixp-parte3.pdf):**
  * **Metodologia Aplicada:** Condução de uma Avaliação Heurística sistemática baseada nas **10 Heurísticas de Nielsen**, otimizando o ciclo de desenvolvimento com foco em baixo custo e alta eficiência diagnóstica.
  * **Fluxo de Auditoria:** Execução rigorosa dividida em *Preparação* (estudo de domínio), *Coleta Individual de Dados*, *Interpretação*, *Consolidação em Grupo* (juízo de relevância e severidade) e *Relato*.
  * **Mapeamento de Usabilidade:** Diagnóstico detalhado de problemas reais de interação nas versões Desktop e Mobile, cobrindo gravidades de nível 2 (pequeno) a nível 3 (grande).
  * **Plano de Correção:** Proposição de soluções de engenharia voltadas a máscaras de validação dinâmica, ativação condicional de botões em formulários e otimização de fluxos com o mínimo de cliques possíveis.

---
---

## Processo de Design (Design Centrado no Usuário - DCU)

### 1. Análise e Coleta de Dados
Foram aplicados questionários estruturados com o grupo responsável pelo pitch inicial para entender as dores do público-alvo (estudantes, atléticas e centros acadêmicos). Além disso, foi realizado um **Benchmarking** competitivo analisando lacunas em plataformas como *Sympla* e *Cheers*.

### 2. Perfis de Usuário & Personas
A plataforma opera sob três perfis distintos: **Participante** (discentes), **Organizador** (entidades acadêmicas) e **Funcionário** (apoio e credenciamento).

| Persona | Perfil | Dor Principal | Objetivo no UNIXP |
| :--- | :--- | :--- | :--- |
| **Acadêmica** | Aluno de Graduação | Demora e erros na emissão de horas de extensão | Obter certificados em PDF integrados ao SIGAA sem burocracia |
| **Organizadora** | Diretor de Atlética | Custos operacionais altos e falta de dados de engajamento | Reduzir custos de bilheteria e acessar relatórios de vendas |

### 3. Cenário de Interação (Exemplo)
> **Validação de Presença e Certificação Automática:** O participante apresenta o ingresso digital via QR Code no smartphone. O funcionário realiza a leitura pelo aplicativo e o sistema registra a entrada em tempo real. Após o encerramento do evento, o sistema cruza os dados e disponibiliza o certificado autenticado automaticamente no perfil do usuário.

---

## Engenharia de Requisitos

### Requisitos Funcionais (RF)
* **[RF001] Gestão de Acesso:** Cadastro e login integrado (Google/Gmail, Apple) e integração SIGAA para validação de estudantes UFG.
* **[RF002] Gerenciamento de Eventos:** Criação, categorização (cultural, acadêmico, esportivo) e controle de lotes/rascunhos.
* **[RF003] Operações de Venda:** Processamento de pagamentos via PIX e Cartão de Crédito.
* **[RF004] Controle e Certificação:** Check-in via QR Code e emissão automática de certificados com integração de horas.
* **[RF005] Monetização:** Planos de assinatura *UniXP+* (vantagens para alunos) e *UniXP PRO* (impulsionamento para organizadores).

### Requisitos Não Funcionais (RNF)
* **[RNF001] Segurança:** Proteção de dados sensíveis e níveis restritos de acesso administrativo.
* **[RNF002] Eficiência:** Tempo de resposta para transações críticas (compras e check-in) inferior a 2 segundos.
* **[RNF003] Usabilidade:** Interface responsiva, intuitiva e com forte destaque visual para chamadas de ação (CTA).
* **[RNF004] Confiabilidade:** Backup automático de ingressos/certificados e consistência em transações financeiras.

---

## Interfaces e Prototipagem (Figma)

O ambiente de design interativo e os fluxos de navegação da plataforma foram desenvolvidos no Figma. Você pode interagir com os protótipos de alta fidelidade clicando nos botões abaixo:

<a href="https://www.figma.com/proto/vZYXL81DfYG8ZsQBDmBokl/UniXP-IHC?node-id=0-1&t=xSRUobxW3BChmApI-1" target="_blank">
  <img src="https://img.shields.io/badge/Acessar%20Protótipo-Desktop%20💻-blue?style=for-the-badge&logo=figma&logoColor=white" alt="Protótipo Desktop">
</a>
<a href="https://www.figma.com/proto/vZYXL81DfYG8ZsQBDmBokl/UniXP-IHC?node-id=1-1086&t=xSRUobxW3BChmApI-1" target="_blank">
  <img src="https://img.shields.io/badge/Acessar%20Protótipo-Mobile%20📱-orange?style=for-the-badge&logo=figma&logoColor=white" alt="Protótipo Mobile">
</a>


