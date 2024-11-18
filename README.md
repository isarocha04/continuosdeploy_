# CI/CD e automação de infraestrutura

A adoção de práticas de CI/CD tem se destacado no desenvolvimento de software moderno. Essas práticas permitem que equipes de desenvolvimento entreguem software com mais eficiência e mais qualidade, reduzindo o tempo necessário para levar novas funcionalidades ao mercado.

## Integração contínua 

A integração contínua  automatiza a integração de códigos de diferentes desenvolvedores em um repositório compartilhado. Podemos fazer isso pela execução automática de testes sempre que houver alguma alteração no código, garantindo que modificações não quebrem funcionalidades já desenvolvidas. Esse processo melhora a eficiência, pois identifica problemas rapidamente.

## Desdobramento contínuo 

O desdobramento contínuo  automatiza a implantação de alterações aprovadas em ambientes de produção ou testes. Essa abordagem acelera a entrega de software e garante consistência, reduzindo riscos associados a implantações manuais.

### Benefícios do CI/CD

- **Maior agilidade**: o processo de entrega de software é simplificado e os ciclos de feedback são encurtados.
- **Automação**: reduz o esforço manual, permitindo que os desenvolvedores foquem em outras tarefas.
- **Melhoria na qualidade**: a adoção de testes contínuos aumenta a confiabilidade do código.

---

## GitHub Actions

Um workflow do GitHub Actions é uma configuração automatizada que permite executar tarefas específicas em um repositório do GitHub. É estruturado com base em arquivos YAML e é dividido em diversos elementos que trabalham para definir e executar processos como testes automatizados e integração contínua.

### Componentes de um Workflow no GitHub Actions

1. **Arquivos YAML**
   - Os workflows são configurados em arquivos com extensão `.yml` ou `.yaml`, localizados no diretório `.github/workflows/` do repositório.
   - Cada arquivo define as etapas e as condições para a execução do workflow.

2. **Jobs**
   - Os workflows são compostos por um ou mais "jobs". Cada job é um conjunto de passos executados de forma sequencial ou paralela.
   - Os jobs têm dependências entre si e podem ser configurados para rodar em diferentes ambientes.

3. **Steps**
   - Dentro de um job, os "steps" definem ações específicas que o workflow deve executar.
   - Podem incluir a execução de scripts, instalação de dependências ou comandos definidos diretamente no arquivo YAML.

4. **Actions**
   - As actions são componentes reutilizáveis que realizam tarefas específicas, como executar testes, compilar código ou fazer implantações.

5. **Triggers**
   - Os gatilhos definem quando um workflow deve ser executado:
     - **push**: Executa o workflow quando há alterações enviadas ao repositório.
     - **pull_request**: Executa o workflow ao criar ou atualizar um pull request.

6. **Runner**
   - O runner é a máquina (física ou virtual) onde os jobs do workflow são executados.
   - Pode ser um runner hospedado pelo GitHub ou configurado pelo próprio usuário.

7. **Variáveis de Ambiente**
   - Compartilham configurações entre os steps, como credenciais, URLs e outras informações sensíveis.

8. **Secrets**
   - Para proteger informações sensíveis, como tokens de autenticação ou chaves API, o GitHub Actions suporta o uso de "secrets".

9. **Contextos**
   - Fornecem informações úteis para os workflows, como detalhes sobre o repositório, commit ou pull request.

### Benefícios do GitHub Actions

- **Automação**: Facilita a execução de tarefas repetitivas, como os testes.
- **Flexibilidade**: Oferece suporte a diferentes linguagens e ambientes.
- **Integração**: Permite integração com outros serviços.

---

## AWS CloudFormation

O AWS CloudFormation é uma ferramenta de "Infrastructure as Code" que permite criar e gerenciar recursos da AWS de forma automatizada e organizada.

### Principais benefícios do AWS CloudFormation

1. **Automação completa**
   - Criação, configuração e atualização de recursos de forma automática.

2. **Versionamento e controle de mudanças**
   - Permite rastrear alterações e reverter configurações quando necessário.

3. **Gerenciamento de dependências**
   - Identifica automaticamente as dependências entre os recursos.

4. **Reprodutibilidade**
   - Permite recriar ambientes de forma consistente.

5. **Escalabilidade**
   - Suporta arquiteturas complexas e escaláveis.

### Aplicação com AWS CloudFormation

- Automatizar a criação de ambientes de teste e produção.
- Reutilizar o mesmo template para diferentes configurações.
- Evitar erros manuais comuns ao configurar recursos diretamente pelo console.

---

## Integração GitHub Actions com AWS CloudFormation e Amazon EC2

A integração de GitHub Actions, AWS CloudFormation e Amazon EC2 automatiza o ciclo de vida do desenvolvimento e da infraestrutura. Isso inclui desde a construção e teste do código até a implantação e gerenciamento da infraestrutura.

### Aplicação em projetos Reais

1. **Automação da Infraestrutura com CloudFormation**
   - Utilizando templates, a infraestrutura é criada de forma consistente e automatizada.

2. **Gerenciamento Centralizado**
   - Todas as etapas, desde a criação da infraestrutura até a implantação, são gerenciadas diretamente no repositório GitHub.

3. **Escalabilidade Automatizada**
   - Com o Amazon EC2 Auto Scaling, os workflows ajustam automaticamente a capacidade da infraestrutura com base na demanda.

