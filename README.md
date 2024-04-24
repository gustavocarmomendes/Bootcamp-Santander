# 📅 DIO | Bootcamp - Santander | Anotações

Este repositório foi criado para armazenar todas as anotações, resumos, etc... Sobre o que foi passado de acordo com o Bootcamp.

## 🧠 1 - Princípios de Desenvolvimento de Software Colaborativo


#### 👨‍💻 Versionamento de Código em Git e GitHub:

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
$ git config --list
```

**Configurando seu nome de usuário e e-mail (globalmente)**

```
$ git config --global user.name "Gustavo do Carmo Mendes"
$ git config --global user.email gustavosmensey@gmail.com
```

**Configurando o nome da Branch padrão**

```
$ git config --global init.defaultBranch main
```

*Normalmente por padrão a Branch padrão se chama Master, porém atualmente estão utilizando mais o nome "Main", por isso fizemos esta modificação.*

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
& git add .
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

## Referências
- [Digital Innovation One](https://www.dio.me)
- [Instrutora do Curso de Git - Elidiana Andrade](https://github.com/elidianaandrade)
- [Informações retiradas do Repositório](https://github.com/elidianaandrade/dio-curso-git-github)
