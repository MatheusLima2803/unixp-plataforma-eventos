# UNIXP — Plataforma de Gestão e Comercialização de Ingressos Universitários

## 📌 Sobre o Projeto
O **UNIXP** é uma plataforma centralizada voltada para a divulgação, gerenciamento e comercialização de ingressos de eventos universitários. O ecossistema integra processos acadêmicos críticos, como a automação na emissão de certificados, resolvendo problemas crônicos de descentralização de informações e atrasos em validações de horas de extensão.

Este repositório contém o **Case de Engenharia de Requisitos e Design Centrado no Usuário (DCU)** do sistema.

---

## Equipe de Desenvolvimento
* Arnaldo Rocha
* Lucas Mota
* Matheus Marques
* Norton Almeida

---

## Análise de Mercado e Impacto
Atualmente, as informações de eventos acadêmicos e culturais ficam dispersas em redes sociais ou murais físicos. O UNIXP altera os seguintes processos de negócio:
* **Venda de Ingressos:** Transição do modelo físico para o digital com taxas reduzidas para estudantes.
* **Credenciamento:** Substituição de listas de papel por validação ágil via QR Code.
* **Certificação:** Automação da emissão de certificados com validade acadêmica através de integração direta com sistemas universitários (ex: **SIGAA**), otimizando processos de grandes eventos como o CONPEEX.

---

## Processo de Design (Design Centrado no Usuário - DCU)

### 1. Análise e Coleta de Dados
Foram aplicados questionários estruturados com o grupo responsável pelo pitch inicial para entender as dores do público-alvo (estudantes, atléticas e centros acadêmicos). Além disso, foi realizado um **Benchmarking** competitivo analisando lacunas em plataformas como *Sympla* e *Cheers*.

### 2. Perfis de Usuário & Personas
A plataforma opera sob três perfis distintos: **Participante** (discentes), **Organizador** (entidades acadêmicas) e **Funcionário** (apoio e credenciamento).

| Persona | Perfil | Dor Principal | Objetivo no UNIXP |
| :--- | :--- | :--- | :--- |
| **Acadêmica** (20 anos) | Aluno de Graduação | Demora e erros na emissão de horas de extensão | Obter certificados em PDF integrados ao SIGAA sem burocracia |
| **Organizadora** (22 anos) | Diretor de Atlética | Custos operacionais altos e falta de dados de engajamento | Reduzir custos de bilheteria e acessar relatórios de vendas |

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

## Interfaces e Modelagem

### Protótipo de Alta Fidelidade (Figma)
Você pode acessar o ambiente de design interativo do projeto diretamente no Figma:
Mobile:🔗 https://www.figma.com/proto/vZYXL81DfYG8ZsQBDmBokl/UniXP-IHC?node-id=1-1086&t=xSRUobxW3BChmApI-1
Desktop:

#### Telas do Sistema
*Exemplo das interfaces desenvolvidas aplicadas aos conceitos de IHC:*

![Home da Plataforma](assets/mockup_home.png)
*Legenda: Tela inicial com foco na experiência de busca do estudante.*

### Modelagem de Casos de Uso
![Diagrama de Casos de Uso](assets/diagrama_casos_uso.png)
