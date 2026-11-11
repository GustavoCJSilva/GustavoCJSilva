<h1 align="center">Olá, eu sou o Gustavo Cesar 👋</h1>

<p align="center">
  <a href="https://github.com/GustavoCJSilva">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3200&pause=900&color=2F81F7&center=true&vCenter=true&width=620&lines=Desenvolvedor+Full-Stack+%2B+IA;APIs%2C+bancos+de+dados+e+integra%C3%A7%C3%B5es;Do+zero+ao+deploy+em+produ%C3%A7%C3%A3o;Transformando+aprendizado+em+projetos+reais" alt="Desenvolvedor Full-Stack + IA" />
  </a>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/gustavo-c%C3%A9sar-526791311/"><img src="https://img.shields.io/badge/LinkedIn-Gustavo%20Cesar-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="https://github.com/GustavoCJSilva"><img src="https://img.shields.io/badge/GitHub-GustavoCJSilva-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" /></a>
  <img src="https://komarev.com/ghpvc/?username=GustavoCJSilva&style=for-the-badge&color=2F81F7&label=Visitas" alt="Visitas ao perfil" />
</p>

---

## 🧑‍💻 Sobre mim

```ts
const gustavo = {
  cargo:        "Desenvolvedor Full-Stack + IA",
  foco:         ["Sistemas web", "APIs REST", "Integrações", "Cloud"],
  ambiente:     "Sistemas corporativos e infraestrutura em nuvem",
  principios:   ["Código limpo", "Segurança por padrão", "Soluções estáveis"],
  aprendendo:   ["Arquitetura de software", "Integração com APIs de marketplaces", "IA aplicada a processos"],
  frase:        "Desenvolvimento consistente, aprendizado contínuo e foco em soluções reais.",
};
```

- 🛠️ Construo e mantenho **sistemas web completos**: interface, API, banco de dados e deploy.
- 🔌 Gosto de **automatizar processos de negócio** e integrar sistemas por API.
- ☁️ Publico e configuro ambientes em **nuvem** (AWS e hospedagem gerenciada).
- 🤖 Uso **IA no fluxo de desenvolvimento** para entregar mais rápido, sem abrir mão da qualidade.

---

## 🧰 Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=java,dotnet,cs,php,python,nodejs&perline=6" alt="Backend" /><br/>
  <img src="https://skillicons.dev/icons?i=html,css,js&perline=6" alt="Frontend" /><br/>
  <img src="https://skillicons.dev/icons?i=postgres,mysql,aws,git,github,vscode&perline=6" alt="Dados, cloud e ferramentas" />
</p>

| Camada | Tecnologias |
|---|---|
| **Backend** | Java · .NET / C# · PHP 8 · Node.js · Python |
| **Frontend** | HTML5 · CSS3 · JavaScript (SPA sem framework) |
| **Banco de dados** | PostgreSQL · MySQL / MariaDB — modelagem relacional e documentos JSON |
| **Plataforma corporativa** | ![Salesforce](https://img.shields.io/badge/Salesforce-00A1E0?style=flat-square&logo=salesforce&logoColor=white) |
| **Cloud & Deploy** | AWS (instâncias e deploy) · Hostinger · LiteSpeed/Apache |
| **Integrações** | APIs REST · OAuth 2.0 · Webhooks com assinatura HMAC |

---

## 🚀 Projeto em destaque — Sistema de Devoluções

> Sistema web em produção usado pela operação de e-commerce para controlar **devoluções de marketplaces**, conferência no CD, disputas, estoque Full e transferências. Ele substituiu uma planilha compartilhada.

```mermaid
flowchart LR
    U["👤 Equipe<br/>(navegador)"] -->|HTTPS + cookie de sessão| SPA["SPA<br/>HTML · CSS · JS"]
    SPA -->|JSON| API["API REST<br/>PHP 8.3"]
    API --> DB[("MySQL")]
    API --> FS["📎 Anexos<br/>fora do webroot"]
    MP["🛒 Marketplaces<br/>Mercado Livre · Shopee · Amazon<br/>Magalu · Shein · TikTok Shop · Shopify"] -->|Webhooks| API
    CRON["⏱️ Cron"] -->|sincronização| API
    API -->|OAuth 2.0| MP
```

| Destaque | Como foi feito |
|---|---|
| 🔐 **Autenticação própria** | Sessões por token (cookie `HttpOnly`, `Secure`, `SameSite=Strict`), senhas com `password_hash` e bloqueio após tentativas erradas |
| 👥 **Permissões por usuário** | Perfis admin e usuário, com permissões granulares (criar, editar, anexar, excluir, backup) |
| ⚔️ **Concorrência otimista** | Detecta quando dois usuários editam o mesmo registro (HTTP 409) e evita sobrescrever dados |
| 🖼️ **Anexos de imagem** | Upload com validação de tipo, redução automática no navegador, galeria, visualizador e download |
| 🔄 **Atualização em tempo real** | Todos os usuários veem as mudanças sem recarregar a página |
| 🧹 **Retenção de dados** | Exclusão automática 60 dias após a conclusão, com aviso 5 dias antes e opção de fixar urgentes |
| 🔌 **Camada de integrações** | Conectores plugáveis por marketplace, credenciais cifradas (AES-256-GCM), webhooks e upsert sem duplicar |
| 📥 **Migração de dados** | Importação da planilha antiga em Python, com fotos baixadas e anexadas automaticamente |

`PHP 8.3` `MySQL` `JavaScript` `Python` `Node.js` `REST` `OAuth 2.0` `HMAC` `AES-GCM`

---

## 📊 Atuação técnica

| Domínio | O que faço na prática |
|---|---|
| **Desenvolvimento** | Construção e manutenção de páginas, sistemas e APIs |
| **Sustentação** | Correção de falhas, melhorias funcionais e evolução de sistemas legados |
| **Dados** | Modelagem, consultas e migração de dados em bancos relacionais |
| **Deploy** | Publicação e configuração de ambientes em nuvem |
| **Plataforma** | Ajustes e suporte técnico em sistemas empresariais (Salesforce) |

---

## 🎯 Próximos passos

- [x] Colocar em produção um sistema completo, com front, API, banco e deploy
- [x] Estruturar uma camada de integrações com marketplaces
- [ ] Conectar as APIs de Mercado Livre, Shopee, Amazon e outros marketplaces
- [ ] Aprofundar em arquitetura de software, testes automatizados e CI/CD
- [ ] Consolidar carreira como desenvolvedor full-stack

---

## 📈 Atividade no GitHub

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=GustavoCJSilva&theme=github-dark-blue&hide_border=true&locale=pt_BR" alt="Sequência de contribuições" /><br/><br/>
  <img src="https://ghchart.rshah.org/2F81F7/GustavoCJSilva" alt="Calendário de contribuições" width="95%" />
</p>

---

<p align="center">
  <i>Desenvolvimento consistente, aprendizado contínuo e foco em soluções reais.</i><br/><br/>
  <a href="https://www.linkedin.com/in/gustavo-c%C3%A9sar-526791311/">💼 Vamos conversar no LinkedIn</a>
</p>
