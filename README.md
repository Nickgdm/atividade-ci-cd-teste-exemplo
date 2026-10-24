# Exemplo de CI/CD para Testes com Jenkins e Docker

Projeto educacional para praticar integração contínua de testes Cypress usando Jenkins, Docker e arquivos de configuração versionados.

## Objetivos
- Conhecer a estrutura de um pipeline como código.
- Automatizar a instalação de dependências e a execução dos testes.
- Praticar execução reprodutível e análise de resultados.

## Tecnologias
- Jenkins
- Docker
- Cypress
- Node.js e npm
- Allure

## Pré-requisitos
- Jenkins configurado com acesso ao repositório.
- Agente Windows para executar o `Jenkinsfile` atual, pois ele utiliza comandos `bat`.
- Node.js/npm disponíveis no agente e ferramenta Jenkins NodeJS configurada com o nome `nodejs`.
- Docker instalado para as atividades de containerização descritas nos arquivos do projeto.

## Como executar pelo Jenkins
1. Configure um job do tipo **Pipeline** apontando para este repositório.
2. Confirme que o agente é Windows ou adapte os comandos do Jenkinsfile ao sistema operacional usado.
3. Execute o job e verifique o console output para acompanhar `npm install` e `npm test`.
4. O comando `npm test` executa `npx cypress run --browser chrome`; confirme que o Chrome e as dependências necessárias estão disponíveis no agente.

## Execução local
Na raiz do projeto, com Node.js/npm instalados:

```bash
npm install
npm test
```

Para gerar ou abrir relatórios Allure, consulte os scripts disponíveis no `package.json` e confirme que existem resultados em `allure-results`.

## Arquivos principais
- `Jenkinsfile`: pipeline para agente Windows.
- `Dockerfile` e `docker-comandos.txt`: arquivos de apoio às atividades com Docker.
- `cypress.config.js` e `cypress/`: configuração e testes Cypress.
- `logs-cypress/` e `allure-results/`: diretórios de logs/resultados presentes no repositório.

## Desafios práticos
Integrar dependências e execução automatizada, configurar o agente corretamente e analisar logs quando uma etapa do pipeline falha.

## Boas práticas adotadas
- Versionamento do pipeline junto ao código.
- Configuração de ambiente por arquivos.
- Armazenamento de logs e resultados para apoiar a análise.

## 📚 Aprendizados
A atividade permite praticar conceitos de CI/CD, execução automatizada de testes e configuração de pipeline, além de compreender como logs e artefatos ajudam a diagnosticar falhas.

## Considerações finais
A configuração do Jenkinsfile deve corresponder ao sistema operacional do agente. Antes de executar o fluxo com Docker, confira os comandos e os requisitos definidos nos arquivos do projeto.

---

## 🎓 Formação
Atividade desenvolvida durante a formação profissionalizante em **Quality Assurance (QA) pela EBAC — Escola Britânica de Artes Criativas e Tecnologia**.
