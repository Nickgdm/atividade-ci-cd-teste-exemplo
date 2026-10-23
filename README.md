# Exemplo de CI/CD para Testes com Jenkins e Docker

Projeto educacional para praticar integração contínua de testes Cypress usando Jenkins, Docker e arquivos de configuração versionados.

## Objetivos
- Conhecer a estrutura de um pipeline como código.
- Automatizar etapas de preparação e execução dos testes.
- Praticar execução reprodutível com containers.

## Tecnologias
- Jenkins
- Docker
- Cypress
- Node.js e npm
- Allure (artefatos de resultados presentes no repositório)

## Pré-requisitos
- Docker instalado.
- Jenkins configurado com acesso ao repositório.
- Node.js/npm disponível no ambiente de execução, quando não fornecido pelo container.

## Como executar
1. Revise o `Dockerfile`, `Jenkinsfile` e `docker-comandos.txt`.
2. Confira as portas, diretórios e dependências configuradas.
3. Configure um job Pipeline no Jenkins apontando para o repositório.
4. Execute o pipeline e examine os logs e resultados gerados.

Os comandos exatos dependem da configuração atual dos arquivos. Valide-os em ambiente local antes de usar em um pipeline compartilhado.

## Estrutura do projeto
```text
atividade-ci-cd-teste-exemplo/
├── .github/
├── cypress/
├── logs-cypress/
├── allure-results/
├── Dockerfile
├── Jenkinsfile
├── docker-comandos.txt
├── cypress.config.js
└── package.json
```

## Desafios práticos
Integrar dependências, containerização e execução de testes, além de analisar logs quando uma etapa do pipeline falha.

## Boas práticas adotadas
- Versionamento do pipeline junto ao código.
- Configuração de ambiente por arquivos.
- Armazenamento de logs e resultados para apoiar a análise.

## 📚 Aprendizados
A atividade permite praticar conceitos de CI/CD, execução automatizada de testes e containerização, além de compreender como logs e artefatos ajudam a diagnosticar falhas do pipeline.

## Considerações finais
Consulte os arquivos do projeto para confirmar a sequência de comandos, os caminhos e as condições de execução do pipeline.

---

## 🎓 Formação
Atividade desenvolvida durante a formação profissionalizante em **Quality Assurance (QA) pela EBAC — Escola Britânica de Artes Criativas e Tecnologia**.