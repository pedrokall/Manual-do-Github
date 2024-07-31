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

+ Caso utilize o Windows, acesse o site oficial do [Git](https://git-scm.com/)

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
        <img width= "40%" height = "auto" alt= "repository" title="repository" src="assets\gifs\siteOption.gif"/>&nbsp;
        <img width= "40%" height = "auto" alt= "repository" title="repository" src="assets\gifs\newSSH.gif"/>
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

+ Para clonar um repositório o usuário pode escolher se clonará por HTTPS ou usando uma chave SSH, se tiver configurado em seu sistema uma chave SSH, é um método mais recomendado.

