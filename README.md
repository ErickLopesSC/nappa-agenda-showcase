<!--
  SHOWCASE PRIVADO — apenas documentação; nenhum código-fonte.
  Quando as capturas existirem, salvar em docs/screens/ e descomentar a seção de demonstração.
-->

<div align="center">

# Nappa Agenda

**Agenda digital da clínica multidisciplinar NAPPA (UNIFESO): pacientes, profissionais e horários em um fluxo único.**

![Status](https://img.shields.io/badge/c%C3%B3digo-privado-4B5563?style=flat-square&logo=github&logoColor=white)
![.NET](https://img.shields.io/badge/.NET%209-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![C#](https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=csharp&logoColor=white)
![React](https://img.shields.io/badge/React%2019-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)

</div>

> **Nota:** o código-fonte é mantido em repositório **privado**. Este repositório publica apenas a documentação do produto e da arquitetura, para fins de portfólio.

---

## 📌 O problema

A clínica multidisciplinar **NAPPA** da UNIFESO recebe pacientes de várias especialidades — psicologia, pedagogia, fonoaudiologia — e o agendamento era controlado manualmente. Isso gera conflito de horários, fila de espera opaca e dificuldade de enxergar a ocupação dos profissionais.

O sistema digitaliza o fluxo completo: cadastro de pacientes, agenda por profissional, controle de disponibilidade e acompanhamento dos atendimentos.

---

## ✨ Funcionalidades

- Autenticação com **JWT** e perfis distintos de acesso
- Cadastro e gestão de pacientes
- Agenda por profissional, com controle de disponibilidade
- Visualização de horários e organização do fluxo de atendimento
- API REST documentada
- Monorepo com backend, frontend e testes automatizados

---

## 🏗️ Arquitetura

```mermaid
flowchart LR
    A["React 19 + Vite<br/>TypeScript"] -->|REST + JWT| B["ASP.NET Core<br/>API"]
    B --> C[("PostgreSQL")]
    B --> D["Testes<br/>xUnit"]
```

**Backend (camadas):** `NAPPA.Api` · `NAPPA.Application` · `NAPPA.Domain` · `NAPPA.Infrastructure` · `NAPPA.Api.Tests`
**Frontend:** React 19 · Vite · TypeScript · React Router · Axios · Lucide

---

## 🧰 Stack

| Área | Tecnologia |
|---|---|
| Backend | C# · .NET 9 · ASP.NET Core |
| Frontend | React 19 · Vite · TypeScript |
| Banco | PostgreSQL |
| Autenticação | JWT |
| Infra local | Docker Compose |
| Testes | xUnit (controllers e services) |

---

## 🧠 Decisões técnicas

- **Monorepo** — frontend e backend evoluem juntos, com um único histórico de decisões.
- **Camadas explícitas no backend** — Api, Application, Domain e Infrastructure separadas, com testes por camada.
- **JWT + perfis** — permissões diferentes para paciente, profissional e administração.
- **Docker Compose** — banco e API sobem com um comando; credenciais por variável de ambiente.

---

<!-- DEMONSTRAÇÃO (descomentar quando houver mídia em docs/screens/):
## 📸 Demonstração

| Fluxo | Mídia |
|---|---|
| Login | `docs/screens/login.png` |
| Agenda por profissional | `docs/screens/agenda.png` |
| Novo agendamento | `docs/screens/novo-agendamento.png` |
| Meus agendamentos | `docs/screens/meus-agendamentos.png` |
-->

## 👥 Equipe

- **Eduardo Leal** — [@dudu4leal](https://github.com/dudu4leal)
- **Yuri Domingues** — [@yuridomingues](https://github.com/yuridomingues)
- **Anna Pitzer** — [@Anna-Pitzer](https://github.com/Anna-Pitzer)
- **Erick Lopes dos Santos Carvalho** — [@ErickLopesSC](https://github.com/ErickLopesSC)

**Showcase mantido por** Erick Lopes — [LinkedIn](https://www.linkedin.com/in/erick-lopes-2k02/)
