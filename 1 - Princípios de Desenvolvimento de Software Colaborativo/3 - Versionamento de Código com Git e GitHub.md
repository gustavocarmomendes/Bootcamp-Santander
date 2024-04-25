# 👨‍💻 Versionamento de Código em Git e GitHub:

*Repositório criado para gravar as anotações do Curso de Git & GitHub*

**O que é versionamento de código?**

```
É um Sistema que controla todas as versões do seu código principal, como por exemplo,
podemos pegar o código-fonte principal(main) e cada um trazer para a sua máquina local,
com isso iremos salvando as atualizações e depois mesclando, sem atrapalhar um ao outro,
ou ter que depender do mesmo.
```

 **Tipos de Sistema de Controle de Versão:**
 - VCS Centralizado (CVCS) | Ex: CVC, Subversion.
 - VCS Distribuído (DVCS)  | Ex: Git, Mercurial.


| VCS Distruibuido               | Informações Completas |
| ----------------- | ---------------------------------------------------------------- |
| Clona o repositório completo, o que incluí as versões       | Cada clone é como um Backup |
| Possibilita um fluxo de trabalho flexível       | Possibilidade de trabalar sem conexão à rede. |


**O que é Git?**

```
É um sistema de controle de versão distribuído, gratuito e open source, capaz de criar
ramificações(branchings) e fusões(merging) eficientes. Além de ser leve e rápido.
```

**Configurando o Git**

```
$ git config
```

**Configurando seu nome de usuário e e-mail (globalmente)**

```
$ git config --global user.name "Gustavo do Carmo Mendes"
$ git config --global user.email gustavosmensey@gmail.com
```

**Configurando o nome da Branch principal**

```
$ git config --global init.defaultBranch main
```
*Normalmente por padrão a Branch padrão se chama Master, porém atualmente estão utilizando mais o nome "Main", por isso fizemos esta modificação.*

**Configurando o acesso no Git**

*Para fazer isso você pode tentar clonar um repositório seu com:*

```
$ git clone link-repositório
```

*Com isso ele vai pedir seu usuario do github, após inserir ele vai pedir uma senha, na qual temos que criar um token para isso*

```
Perfil -> Settings -> Developer Settings -> Personal acess Token ->
Tokens (classic) - > Generate new token -> Generate new token (classic)
```
*Ali você irá definir o nome do seu token, o tempo que deseja que ele fique ativo e as permissões que aquele token terá.*

**Para salvar seu token no Git, existem duas formas**

Caso divida o computador com alguém e queira deixar salvo temporariamente utilize:
```
$ git config --global credential.helper cache
```
Caso não divida o computador com ninguém e queira salvar permanentemente, utilize:

```
$ git config --global credential.helper store
```


**Criando Repositório**

- Você pode clonar um repositório já existente.
- Transformando uma pasta(diretório local) que não está sob controle de versão em um repositório Git.

**Para iniciar um repositório Git, acesse a pasta que deseja e abra o prompt do Git**

```
$ git init
```

**Crie um repositório(de preferência com o mesmo nome) no GitHub e copie o link HTTPS, vamos conectar o repositório remoto com o local**

```
$ git remote add origin link-do-repositório
```

**Após fazer qualquer alteração no projeto, veja o status com**

```
$ git status
```

**Caso tenha informações que ainda não foram publicadas, utilize**

```
$ git add .
```

*O "." é utilizado para adicionar todas as informações diretas, sem precisar adicionar item por item.*

**Após isso só faltará comitar**

```
$ git commit -m"mensagem para ser enviada no commit"
```

**EXTRA**

**Caso queira modificar a mensagem enviada no último commit, utilize**

```
$ git commit --amend -m"nova mensagem"
```

**Caso tenha comitado errado e precise restaurar desde a última versão, utilize os códigos:**

```
$ git reset
```

```
$ git reset --soft
```

```
$ git reset --mixed
```

```
$ git reset --hard
```

*Só utilize o último caso precise utilizar como se fosse um Backup, pois irá trazer a última versão e as atualizações que você teria feito, não existirá mais.*

**Para trazer os commits do repositório remoto para o local, utilize:**
```
$ git pull
```

**Para enviar os commits feitos no repositório local para o servidor, utilize:**

```
$ git push
```

***CRIANDO RAMIFICAÇÕES (BRANCHS)***

**Para criar uma Branch da verão principal**

```
$ git checkout -b nome-branch
```

**Para voltar para a Branch principal (Main), use:**

```
$ git checkout nome-da-main
```

*Lembrando que a main tem como nome padrão Master, porém utilizamos no curso como main, e isso pode alterar dependendo da Empresa*

**Mostra todos os últimos commits feitos por cada branch, desde a principal às ramificações**

```
$ git branch -v
```

**Utilizamos esse código para mesclar com a branch principal**

```
$ git merge nome-da-branch
```

**Mostra todas as Branchs criadas naquele repositório**

```
$ git branch
```

**Exclui a branch**

```
$ git branch -d nome-branch
```

**Utilizando caso você deseja clonar essa Branch do repositório
remoto no repositório local**

```
$ git clone link-https --branch nome-branch --single-branch
```

**Caso esteja mexendo no repositório local e alguém enviou um commit para o servidor, utilize isso (opcional)**

*Traz os commits feito no nosso repositório remoto porém não mescla com o nosso repositório
local.*

```
$ git fetch origin main
```

*Mostra o conteudo commitado no repositório remoto*

```
$ git diff main origin/main
```

*Mescla o conteudo que você trouxe comitado, com o seu repositório local*

```
$ git merge origin/main
```


## 🔍 Referências
- [Digital Innovation One](https://www.dio.me)
- [Instrutora do Curso de Git - Elidiana Andrade](https://github.com/elidianaandrade)
- [Informações retiradas do Repositório](https://github.com/elidianaandrade/dio-curso-git-github)
