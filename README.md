<div align="left">
  <table>
    <tr>
      <td style="background-color: #f0f0f0; padding: 10px; border-radius: 5px;">
        <span style="font-weight: bold; color: #000000; font-size: 20px;">Manual do GitHub</span>
        <img src="https://cdn.jsdelivr.net/npm/devicon/icons/github/github-original.svg" alt="GitHub Logo" width="40" height="40" style="vertical-align: middle; margin-left: 10px;">
      </td>
    </tr>
  </table>
</div>
         
## Introdução ao GitHub

### O que é o GitHub?

<p align="justify">
GitHub é uma plataforma de hospedagem de código-fonte que permite o controle de versão usando o Git. Ele facilita a colaboração em projetos de software, permitindo que desenvolvedores de todo o mundo trabalhem juntos de maneira eficiente.
</p>


### História do GitHub

<p align="justify">
Lançamento:
O GitHub foi fundado em 2008 por Tom Preston-Werner, Chris Wanstrath e PJ Hyett. Ele começou como uma plataforma de hospedagem de código baseada em Git, permitindo que desenvolvedores colaborassem em projetos de software, rastreassem mudanças e gerenciassem o código-fonte de forma eficiente.
</p>

E em 2010 houve a introdução de o que hoje é uma grande função: o pull request.

<p align="justify">
Um grande incidente de segurança:
Em 2012, o GitHub sofreu um ataque de negação de serviço distribuído (DDoS), que interrompeu temporariamente seus serviços. Esse ataque foi um lembrete de que a segurança cibernética é uma preocupação constante para plataformas online, especialmente aquelas que hospedam dados críticos de código-fonte.
</p>

<p align="justify">
Aquisição pela Microsoft:
Em junho de 2018, a Microsoft anunciou a aquisição do GitHub por US$ 7,5 bilhões em ações. Essa aquisição foi uma surpresa para muitos na comunidade de desenvolvedores, pois o GitHub sempre foi visto como uma empresa independente e uma defensora fervorosa do software de código aberto.
</p>

<p align="justify">
E hoje o GitHub consiste em uma plataforma robusta para desenvolvimento de software colaborativo e um papel crucial no mundo do desenvolvimento de software, facilitando a colaboração entre desenvolvedores e impulsionando a inovação. Seu incidente de segurança em 2012 foi um desafio significativo, mas a plataforma se recuperou e continuou a prosperar. Sua aquisição pela Microsoft em 2018 foi um ponto de virada importante em sua história, mas o GitHub continua sendo uma plataforma essencial para a comunidade de desenvolvedores em todo o mundo.
</p>

### Principais Funcionalidades e Benefícios

* 🚀 Controle de versão eficiente com Git.
* 🤝 Colaboração fácil com pull requests.
* 🌐 Hospedagem de projetos open-source.
* 🔗 Integrações com diversas ferramentas de desenvolvimento.
* ⚙️ Automação de fluxos de trabalho com GitHub Actions

## Configuração Inicial

### Criando uma Conta no GitHub

1. Acesse o [GitHub](https://github.com/).
2. Clique em **_Sing up_**.

<h1 align="center">
    <img alt= "singup" title="singup" src="assets\gifs\singup.gif"/>
</h1>

3. Preencha o formulário com seus dados pessoais.
4. Verifique seu e-mail e complete a configuração da conta.

### Instalando o Git e Configurando no GitHub

#### 1. Instalação do Git 

+ Caso utilize o Windows, acesse o site oficial do [Git](https://git-scm.com/) <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/git/git-plain-wordmark.svg" alt="Git" width="50" height="50">

<h1 align="center">
    <img alt= "gitDownload" title="gitDownload" src="assets\gifs\gitDowload.gif"/>
</h1>

+ No MacOS use: 
```
brew install git
```

+ No Linux: use o gerenciador de pacotes da sua distribuição ou para Devian/Ubuntu:
```
sudo apt install git
```

#### 2. Configuração Inicial:

+ Abra um Git Bash e configure seu usuário Git em seu sistema do seguinte modo:
```
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@example.com"
```

#### 3. Criando uma chave SSH:

+ É uma boa prática o usuário possuir uma **_SSH key_**, que pode ser criada da seguinte maneira:
    + Selecione a pasta desejada para salvar sua **key**, comum por ser a pasta do usuário do sistema, e então abra o Git Bash.
    + No Git Bash execute a seguinte linha de comando, substituindo o email usado no exemplo pelo seu endereço de email GitHub.
    ```
    ssh-keygen -t ed25519 -C "your_email@example.com"
    ```
    + No prompt, digite uma frase secreta segura. Se não desejar uma frase secreta apenas pressione _enter_ para continuar e gerar sua **key**
    ```
    > Enter passphrase (empty for no passphrase): [Type a passphrase]
    > Enter same passphrase again: [Type passphrase again]
    ```
    + Por fim, será gerado o endereço de sua **SSH** e ao acessar as configurações em seu perfil do GitHub, acesse a aba  SSH and GPG keys e adicione uma nova **_SSH Key_**
        <div class="row">
            <img width= "40%" height = "auto" alt= "siteOption" title="siteOption" src="assets\gifs\siteOption.gif"/>&nbsp;
            <img width= "40%" height = "auto" alt= "newSSH" title="newSSH" src="assets\gifs\newSSH.gif"/>
        </div>
    + Adicione um título à sua **Key** e o texto gerado no espaço requisitado.




### Primeiros passos: criando e clonando repositórios

#### 1. Criando um Repositório: 
+ Agora já logado, no GitHub, clique em **_New Repository_**.

<h1 align="center">
    <img alt= "repository" title="repository" src="assets\gifs\repository.gif"/>
</h1>

+ Dê um nome ao repositório e clique em **_Create repository_**.

#### 2. Clonando um Repositório:

+ Para clonar um repositório o usuário pode escolher se clonará por **HTTPS** ou usando uma chave **SSH**, se tiver configurado em seu sistema uma chave **SSH**, é um método mais recomendado.
+ Copie a **URL** fornecida pelo repositório:
    <h1 align="center">
        <img width= "50%" height = "auto" alt= "repoClone" title="repoClone" src="assets\gifs\repoClone.gif"/>
    </h1>
+ E por fim, em sua pasta previamente criada e selecionada, a qual deseja clonar o repositório, execute o Git Bash e o seguinte comando:
```
git clone https://github.com/usuario/repositorio.git
```

## Comandos Básicos do Git

### Estrutura de um repositório Git

<p align="justify">
 Um repositório Git contém todos os arquivos e histórico de mudanças de um projeto e a estrutura de um repositório Git é organizada de forma a gerenciar versões do código e facilitar o trabalho colaborativo.
 </p>

#### Sendo assim a estrutura básica de um Repositório Git consiste em:
1. Diretório de Trabalho (Working Directory):
    + Este é o local onde você trabalha com os arquivos e diretórios do seu projeto. É aqui que você faz alterações no código.
2. Área de Preparação (Staging Area ou Index):
    + É um espaço intermediário onde as alterações são armazenadas antes de serem confirmadas (committed). Você adiciona arquivos à área de preparação.
3. Repositório Local (.git):
    + É um diretório oculto dentro do diretório do seu projeto que contém todos os dados do repositório Git, incluindo a história completa das mudanças, configurações e objetos Git.
4. Repositório Remoto:
    + É uma versão do seu repositório armazenada em um servidor remoto, como GitHub, GitLab ou Bitbucket. Os repositórios remotos são usados para colaborar com outros desenvolvedores.

### Iniciando um repositório
#### Para iniciar um Repositório, é necessário um:
 ```
 git init
 ```
#### na devida pasta selecionada pelo usuário.

#### Os principais comandos em um repositório constam com os seguintes comando de terminal:
+ Adicionar arquivos:
    ```
    git add .
    ```
+ Commitar mudanças:
    ```
    git commit -m "Mensagem do commit"
    ```
+ Enviar para o repositório remoto:
    ```
    git push origin main
    ```
+ E, por fim, puxar mudanças do repositório remoto:
    ```
    git pull
    ```
### Gerenciamento de **_Branches_**

#### Uma prática fundamental para o desenvolvimento de software colaborativo e organizado consiste no gerenciamento de **_branches_**. Pois, permitem que você trabalhe em diferentes funcionalidades, correções de bugs ou experimentos isoladamente, sem afetar o código principal do projeto até que estejam prontos para serem integrados.

#### Conceitos Básicos:
1. Branch (Ramificação):
    + Uma branch é uma linha de desenvolvimento separada dentro do repositório. O Git cria uma branch chamada main ou master por padrão, que geralmente é a linha principal de desenvolvimento.
2. Head:
    + **HEAD** é um ponteiro especial que aponta para o commit atual ou branch atual em que você está trabalhando.

#### Operações Comuns com Branches:
1. Criar e Mudar para uma Nova Branch:
    + Para criar e alternar para uma nova branch:
        ```
        git checkout -b <nome-da-branch>
        ```
    + Ou com o novo comando switch:
        ```
        git switch -c <nome-da-branch>
        ```
2. Mesclar Branches (Merge):
    + Para integrar as mudanças de uma branch em outra, use:
        ```
        git merge <nome-da-branch>
        ```
        Isso mescla as mudanças da <nome-da-branch> na branch atual.
3. Rebase:
    + O rebase aplica suas mudanças sobre a base de outra branch, criando um histórico linear:
        ```
        git rebase <nome-da-branch>
        ```
4. Excluir uma branch:
    + Após uma branch ser mesclada, você pode excluí-la:
        ```
        git branch -d <nome-da-branch>
        ```
    + E para forçar a exclusão (se a branch não foi mesclada), cuidado pode ser um comando perigoso:
        ```
        git branch -D <nome-da-branch>
        ```

#### Gerenciar branches eficientemente ajuda a manter um histórico de mudanças limpo e facilita a colaboração entre vários desenvolvedores, permitindo a integração contínua e o desenvolvimento ágil.

## Trabalho Colaborativo

### Clonando e forkeando repositórios
Como já demonstrado o trabalho colaborativo por repositórios consiste na clonagem do repositório por meio de um git clone e por forks.

Forkar um repositório é uma pratica bem comum. Pois, permite colaborar em projetos de código aberto, trabalhar em funcionalidades e correções de forma isolada, submeter pull requests, explorar e aprender com o código de outros desenvolvedores, personalizar projetos para uso específico e criar um backup do projeto. É uma prática essencial para contribuir sem afetar o repositório original e manter uma cópia própria para desenvolvimento e testes.

#### Como forkar um repositório? 
1. Fork no GitHub:
    + Vá até o repositório que você deseja forkar.
    + Clique no botão "Fork" no canto superior direito da página.
    + Escolha a conta onde deseja criar o fork (se você tiver acesso a várias organizações).
    <div class="row">
            <img width= "40%" height = "auto" alt= "siteOption" title="siteOption" src="assets\gifs\forking.gif"/>&nbsp;
            <img width= "42%" height = "auto" alt= "newSSH" title="newSSH" src="assets\gifs\creatingFork.gif"/>
        </div>
2. Clonar o Fork para o seu Computador:
    + Após forkar o repositório, clone-o para seu ambiente de desenvolvimento local:
        ```
        git clone https://github.com/seu-usuario/nome-do-repositorio.git
        ```
3. Configurar o Repositório Original como Upstream:
    + Para manter seu fork atualizado com o repositório original, adicione-o como um repositório remoto chamado upstream:
        ```
        cd nome-do-repositorio
        git remote add upstream https://github.com/original-usuario/original-repositorio.git

        ```
4. Manter seu Fork atualizado:
    + Para buscar as últimas mudanças do repositório original e integrá-las ao seu fork:
        ```
        git fetch upstream
        git checkout main
        git merge upstream/main
        ```
5. Fazer Mudanças e Enviar Pull Requests:
    + Faça suas alterações e commits em branches no seu fork.
    + Envie um pull request do seu fork para o repositório original, detalhando as mudanças e o motivo delas.

### Pull requests: como criar e gerenciar?

#### Criar e gerenciar pull requests (PRs) é um aspecto crucial do fluxo de trabalho colaborativo em Git. Agora, como criar um pull request?
<div align="center">
    <img width= "60%" src= "assets\images\pullRSexample.png">
</div>

1. Depois de todo passo-a-passo da criação de um fork, primeiramente, vá para o seu repositório fork no GitHub.
2. Clique no botão "Compare & pull request" que aparece após você enviar a branch.
<div align="center">
    <img width= "60%" src= "assets\images\github-create-new-pull-request.png">
</div>
3. Preencha o título e a descrição do PR, detalhando as mudanças feitas e o motivo delas.
4. Escolha a branch de destino no repositório original (geralmente main ou master).
5. Clique em "Create pull request".

#### Gerenciando um Pull Request

+ Um fluxograma que representa muito bem o gerenciamento de pull requests pode ser o exemplo a seguir:
<div align="center">
    <img width= "100%" src= "assets\images\prsManagement.png">
</div>

#### Sendo:
1. Revisar Feedback e Fazer Mudanças Adicionais:
    + Os mantenedores do projeto original revisarão seu PR e poderão solicitar mudanças. Faça as mudanças solicitadas na mesma branch do PR:
        ```
        git add .
        git commit -m "Endereça feedback do PR"
        git push origin minha-nova-funcionalidade
        ```
2. Sincronizar com o Repositório Original:
    + Se o repositório original tiver novas mudanças, você deve mantê-lo atualizado no seu fork:
        ```
        git fetch upstream
        git checkout minha-nova-funcionalidade
        git rebase upstream/main
        git push origin minha-nova-funcionalidade --force
        ```
3. Resolução de Conflitos:
    + Se houver conflitos durante o rebase, resolva-os manualmente, adicione os arquivos corrigidos e continue o rebase:
        ```
        git add .
        git rebase --continue
        git push origin minha-nova-funcionalidade --force
        ```
4. Fechar ou Mesclar o PR:
    + Após aprovação, o mantenedor do projeto original pode mesclar seu PR. Caso seu PR não seja mais necessário, você pode fechá-lo.

5. Por fim, excluir a Branch local e remota:
    + Após o PR ser mesclado, você pode excluir a branch local e remota para manter seu repositório limpo:
        ```
        git branch -d minha-nova-funcionalidade
        git push origin --delete minha-nova-funcionalidade
        ```

### Revisão de código e merge de pull requests

#### Além de todo o processo citado do pull request, existe a necessidade da revisão de código. Pois, revisão de código e o merge de pull requests são etapas cruciais no fluxo de trabalho colaborativo em Git, assegurando a qualidade e a integridade do código antes que ele seja integrado ao repositório principal.

<div align="center">
    <img width= "60%" src= "assets\images\PR_review_process.png">
</div>

#### Onde: 
+ Os revisores designados recebem uma notificação sobre um novo pull request (PR).
+ Revise seu código: 
    + Certifique-se de que o código faz o que é esperado e resolve o problema descrito.
    + Verifique a legibilidade, organização, aderência às convenções de codificação e boas práticas.
    + Confirme se há testes adequados para as mudanças e se todos os testes passam.
    + Avalie se o código introduz vulnerabilidades de segurança ou problemas de performance.
+ E por fim, se o código estiver bom, aprove o PR. No GitHub, marque a revisão como **_"Approved"_**.

#### Merge de Pull Requests
Existem ainda no GitHub, diferentes opções de merge. Sendo:
+ **Merge Commit**: Cria um commit de merge que une as duas branches.
+ **Squash and Merge**: Condensa todos os commits do PR em um único commit antes de mesclá-los.
+ **Rebase and Merge**: Reaplica os commits do PR na base da branch de destino, criando um histórico linear.
<div align="center">
    <img width= "60%" src= "assets\images\merge-types.png">
</div>

### Por fim, Resolvendo Conflitos:
#### Resolver conflitos de merge é uma parte essencial do trabalho com Git, especialmente em ambientes de desenvolvimento colaborativo. Conflitos de merge ocorrem quando há mudanças concorrentes nas mesmas partes de um arquivo em diferentes branches.
#### E como funciona esse passo-a-passo?

+ Primeiro, como perceber quando ocorrem?
    + Conflitos geralmente ocorrem durante operações de merge (git merge), rebase (git rebase) ou pull (git pull) quando Git não consegue automaticamente reconciliar mudanças concorrentes.

    <div align="center">
        <img width= "60%" src= "assets\images\conflictExample.png">
    </div>

+ Identifique-os:
    + Quando um conflito ocorre, o Git interrompe o processo de merge ou rebase e marca os arquivos conflitantes. Você verá mensagens como estas:
        ```
        Auto-merging arquivo-exemplo.txt
        CONFLICT (content): Merge conflict in arquivo-exemplo.txt
        Automatic merge failed; fix conflicts and then commit the result.
        ```
+ E como resolver?
    + 1. Listar Arquivos Conflitantes: use **_git status_** para listar os arquivos que estão em conflito:
    + 2. Abra os arquivos marcados como conflitantes. O Git insere marcadores especiais no arquivo para indicar as áreas conflitantes.
    + 3. Edite os arquivos para resolver os conflitos. Remova os marcadores de conflito.
    + 4. Por fim, após resolver o conflito adicione-o à área de preparação:
        ```
        git add arquivo-exemplo.txt
        ```
    + 5. E finalize o Merge ou Rebase:
        + Se estiver em merge:
        ```
        git commit -m "Resolve conflitos durante o merge da branch-merge"
        ```
        + Se estiver em rebase:
        ```
        git rebase --continue
        ```
## Funcionalidades Avançadas

<div align="left">
  <table>
    <tr>
      <td style="background-color: #00FFFF; padding: 10px; border-radius: 5px;">
        <span style="color: #000000; font-size: 20px;">GitHub Actions</span>
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/githubactions/githubactions-original.svg" alt="GitHub Logo" width="40" height="40" style="vertical-align: middle; margin-left: 10px;">
      </td>
    </tr>
  </table>
</div>

#### Resumidamente, o GitHub Actions consiste em uma ferramenta de automação que permite a criação  de fluxos de trabalho personalizados diretamente no repositório do GitHub. Com ela, é possível automatizar tarefas como CI/CD (integração contínua e entrega contínua), testes, deploys e muito mais.

<div align="center">
        <img width= "80%" src= "assets\images\githubActions.png">
</div>

+  É composto pela estrutura básica de um Workflow, onde:
    + Workflows do GitHub Actions são definidos em arquivos YAML que ficam dentro do diretório .github/workflows no seu repositório.
+ Um exemplo de Workflow:
    ```
    name: CI

    on: [push]

    jobs:
        build:
            runs-on: ubuntu-latest

            steps:
            - name: Check out code
            uses: actions/checkout@v2

            - name: Set up Node.js
            uses: actions/setup-node@v2
            with:
                node-version: '14'

            - name: Install dependencies
            run: npm install

            - name: Run tests
            run: npm test
    ```

#### Funcionalidades Avançadas
+ Além do básico, GitHub Actions oferece diversas funcionalidades avançadas:

    <div align="center">
            <img width= "80%" src= "assets\images\secrets.png">
    </div>

    + 🔐 Secrets: Armazene informações sensíveis, como tokens de acesso, e utilize-as nos workflows.
    + 📈 Matrizes de Jobs: Execute jobs em diferentes ambientes ou com diferentes configurações.
    + 🎯 Ações Personalizadas: Crie suas próprias ações para reutilizar em múltiplos workflows.
    + 💾 Cache: Utilize cache para otimizar os tempos de build.

### Issues e Projects: Gerenciamento de Tarefas e Projetos

<div align="center">
    <img width= "80%" src= "assets\images\gitHubIssues.png">
</div>

#### Issues: São usadas para rastrear bugs, melhorias, tarefas ou quaisquer itens que precisem ser tratados. Podem ser organizadas com labels, milestones e assignees.

#### Projects: Ferramenta de gerenciamento de projetos que permite organizar issues, pull requests e notas em um quadro Kanban ou em uma tabela.

+ Exemplo de Uso:
    + Criando uma Issue:
        +   1. Vá para a aba "Issues" no repositório.
            2. Clique em "New Issue".
            3. Preencha o título e a descrição, e adicione labels, assignees e milestones conforme necessário.
    + Criando um Project:
        +   1. Vá para a aba "Projects".
            2. Clique em "New Project".
            3. Escolha um template (Board ou Table).
            4. Adicione cards que representam issues, pull requests ou notas.

### GitHub Pages: criando sites estáticos com GitHub

#### O GitHub Pages é um serviço oferecido pelo GitHub que permite criar e hospedar sites estáticos diretamente de um repositório GitHub. É uma ferramenta poderosa para desenvolvedores que desejam publicar sites simples, como portfólios, documentações de projetos, blogs e outros tipos de conteúdos estáticos

+ Possui uma configuração básica, sendo o passo-a-passo:
    1. Crie um repositório com o nome ``<username>.github.io``.
    2. Adicione os arquivos do seu site (HTML, CSS, JavaScript).
    3. Vá para a aba **_Settings_** do repositório.
    4. Na seção **_GitHub Pages_**, escolha a branch a ser publicada (geralmente main ou gh-pages).
    5. Por fim, acesse o site em ``https://<username>.github.io``.
    <div align="center">
        <img width= "80%" src= "assets\images\gitHubPages.png">
    </div>

### Integrações e APIs

#### Outra funcionalidade avançada que o GitHub oferece, são diversas integrações com ferramentas externas e APIs que permitem automação e a personalização do fluxo de trabalho.

#### Sendo as principais integrações: 
+ CI/CD: Jenkins, CircleCI, Travis CI.
+ Gerenciamento de Projetos: Trello, Jira.
+ Comunicação: Slack, Microsoft Teams.

#### O GitHub possui duas principais APIs:
+ REST API
+ GraphQL API

#### Muito usadas para automação de criação de issues, onde podemos usar como exemplo a automatização da criação de issues em um repositório GitHub baseado em um evento externo, como um erro reportado em um sistema de monitoramento.
+ Exemplificando em Python uma utilização da REST API:
    ```
    import requests

    # Configurações
    token = 'seu_token_de_acesso'
    repo = 'usuario/repo'
    url = f'https://api.github.com/repos/{repo}/issues'
    headers = {
        'Authorization': f'token {token}',
        'Accept': 'application/vnd.github.v3+json'
    }

    # Dados da issue
    issue_data = {
        'title': 'Erro no sistema de monitoramento',
        'body': 'Descrição detalhada do erro...',
        'labels': ['bug']
    }

    # Criar a issue
    response = requests.post(url, headers=headers, json=issue_data)
    if response.status_code == 201:
        print('Issue criada com sucesso.')
    else:
        print(f'Erro ao criar a issue: {response.content}')
    ```
#### Além também de utilizações como:
+ Extração de Dados de Contribuidores
+ Integração com Ferramentas de CI/CD
+ Monitoramento de Pull Requests
+ Gestão de Repositórios

<div align="center">
    <img width= "80%" src= "assets\images\apiExample.png">
</div>

## 🤝 Boas práticas e Dicas

### Escrevendo bons commits e mensagens
1. Ao fazer um commit é sempre necessário a adição de uma mensagem, desse modo precisamos de mensagens claras e objetivas:
    + Resuma: A primeira linha deve resumir a mudança em 50 caracteres ou menos.
    + Desenvolva: Use o corpo da mensagem para explicar o "porquê" e não apenas o "o que".
    + Use Verbos no Imperativo: Exemplo: "Adicione função de login".
2. Realize commits pequenos e frequentes:
    + Commits frequentemente e com pequenas mudanças são mais indicados, pois outras pessoas os analisarão.
    + Isso facilita o rastreamento de erros e revisões de código.
3. Referencie Issues e Pull Requests:
    + Utilize palavras-chave como "fixes #issue-number" para vincular automaticamente commits a problemas ou pull requests.
4. Siga um Padrão de Mensagem:
    + É comum a adoção de uma convenção de commits, como a [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/), para uniformidade.
    <div align="center">
        <img width= "80%" src= "assets\images\conventional.png">
    </div>

### Estrutura Organizacional de Repositórios
#### Um repositório pode ser acessado por milhares ou até milhões de pessoas, tenha em mente isso. Logo, é necessário que seu repositório possua uma divisão lógica.
+ Organize o código em diretórios que façam sentido para o projeto (e.g., src, tests, docs).
+ Inclua um arquivo README detalhado no repositório principal e subdiretórios se necessário, descrevendo seu propósito.  
+ Mantenha uma pasta docs para documentação extensa, se aplicável.
+ Armazene scripts em uma pasta scripts ou similar.
+ Utilize pastas de configuração (config) para arquivos de configuração.

### Segurança e Permissões

#### Gerenciamento de Acesso:

1. Controle de forma cuidadosa quem tem acesso de escrita e leitura ao repositório.
2. Utilize equipes e permissões no GitHub para gerenciar acessos.

#### Segredos e Credenciais:

1. Nunca inclua segredos ou credenciais diretamente no repositório.
2. Use ferramentas como GitHub Secrets para armazenar informações sensíveis.

#### Verificação de Código:

1. Configure revisões de pull request obrigatórias.
2. Utilize ferramentas de análise estática e linters para manter a qualidade do código.

#### Branch Protection:

1. Proteja branches importantes, como main ou master, para impedir push direto.
2. Requer reviews e testes automáticos antes de permitir merges.

### Uso de Templates e Arquivos de Configuração

1. .gitignore:
    + Inclua um arquivo .gitignore para excluir arquivos desnecessários (e.g., binários, builds, configurações locais).

2. README.md:
    + Escreva um README claro e informativo com instruções de instalação, uso, e contribuição.
    + Inclua badges de status de build, cobertura de testes, e outras métricas importantes.
    
3. Templates de Issues e Pull Requests:
    + Crie templates para issues e pull requests para padronizar o feedback e submissões.
    + Utilize .github/ISSUE_TEMPLATE e .github/PULL_REQUEST_TEMPLATE.

4. Contributing Guidelines:
    + Adicione um arquivo CONTRIBUTING.md com diretrizes para contribuidores.

5. Licenciamento:
    + Inclua um arquivo LICENSE para especificar os termos sob os quais o código pode ser usado.


# Referências
### Este manual foi escrito para ajudar possíveis novos usuários e usuários intermediários do GitHub. A fim de facilitar de maneira didática o uso, com base nas seguintes referências.
+ [Conventional Commits Specification](https://www.conventionalcommits.org/en/v1.0.0/)
+ [Git Documentation](https://git-scm.com/doc)
+ [GitHub Docs](https://docs.github.com/pt)
+ [Open Source Guides](https://opensource.guide/best-practices/)
+ [GitHub Features](https://github.com/features)

## Autores
| [<img src="assets/images/profile.jpg" width=115 > <br> <sub> Pedro Kall </sub>](https://github.com/pedrokall) | [<img src="assets\images\lucasProfile.png" width=110 > <br> <sub> Lucas Lima </sub>](https://github.com/LuscaLN) | 
| :---: | :---: |


