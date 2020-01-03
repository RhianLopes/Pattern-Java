# Pattern-Java

## 💡 Ideia

O repositório Pattern-Java, foi criado com a ideia de ser um repositório com os padrões que devem ser seguidos em um projeto com o Back-End em Java, desde as mensagens de commit e branch, até a arquitetura que deve ser usada no java.

## 💻 Commit

As mensagens de commit devem seguir o seguinte padrão...

```
<tipo>(<escopo>): <assunto>
```
#### Exemplo:
```
feat(UserLogin): add the persistence data in the User Login
fix: ajusts all bugs on User persistence
```

### Tipo:

O Tipo se refere a que tipo de commit se trata, sejam eles...

- ```feat```: Novas funcionalidades ou novos Testes
- ```fix```: Ajuste de Bugs ou Testes
- ```refactor```: Melhoria de código ou aumento de Regra de Negócio
- ```remove```: Remoção de código

### Escopo:

O Escopo deve servir para referenciar uma Funcionalidade, Documento ou Arquitetura, ex: ```UserLogin, README, Order...```.

Deve ser escrito em [Inglês Americano](https://www.inglesnapontadalingua.com.br/2011/05/o-ingles-americano-tambem-tem-forma.html), excessão de casos onde se referência á alguma Técnologia ou Api externa em outra linguagem.

Deve ser escrito seguindo o padrão [CamelCase](http://java-hunters.blogspot.com/2014/12/o-padrao-camelcase.html) em sua escrita, excessão de casos onde se é modificado diversos arquivos e funcionalidades.

### Assunto:

Assunto deve também ser escrito em Inglês Americano, igualmente como o Escopo, e não devem ter nenhum tipo de acento em sua escrita.

O assunto deve resumir de maneira curta e clara o que foi feito, modificado ou removido no commit.

## 🏝 Branch

### Arquitetura

O projeto deve ter as seguintes estruras de branch...

```
o --> (master)
| 
| o --> (test [opcional]) 
| | 
| | o --> (develop)
| | |
| | |\
| | | | --> (feature/fix/refactor/remove)
| | | |
| | |/
| | |
| | |
| |/
| |
|/
|
o
```

#### 🔥 (master):

É a branch principal, ela deve ser protegida, protegida de commits diretamente nela, e deve ser a branch que ficará "Em Produção", ou seja, acessível ao usuário final via servidor.

#### 🔎 (test):

É a branch de homologação, branch responsável pela parte de qualidade de novas funcionalidades ou solução de Bugs, ela deve ser exatamente igual á branch ```master``` adicionada de novas funcionalidades ou soluções de Bugs que estarão sujeito a mudanças pela equipe de qualidade. A branch ```(test)``` é opcional, pois, a parte de qualidade não está presente em todos os projetos, então cabe por decisão da equipe a existência dela.

Outra decisão opcional, é o acesso da branch ```test``` para homologação, se referênciando se ela está em algum servidor público, privado ou localmente, deve ser decidido entre á equipe.

#### ⚙ (develop): 

É a branch principal para a equipe de desenvolvimento, ou seja, deve ser obrigatória. A ideia da existência dela é a do desenvolvedor realizar testes para verificar se aconteceu algum imprevisto com a nova funcionalidade ou solução, outro motivo de sua existência é o aguardo de outras partes da solução entre desenvolvedores. Obrigatóriamente ela deve ser cópia da branch ```test```, caso ela não exista deve ser utilizada a branch ```master``` para copiar.

É opcional seu acesso igualmente a branch ```test```, mas ao contrário da mesma, a branch ```develop``` se presente em algum servidor, deve ser acessada apenas pelos os desenvolvedores para realização de testes funcionais.

#### 🧱 (feature/fix/refactor/remove):

São as branchs responsáveis por funcionalidades, soluções e remoção de código. Para criação de uma nova branch com alguma das responsábilidades citadas, ela deve ser criada a partir da branch ```develop```, feita a solução, deve ser atualizada a mesma com base na branch ```develop```, em caso de conflitos, devem ser resolvidos e após isso aberto o Pull Request ou Merge Request diretamente via plataforma de versionamento de repositório.

Todas as branch não dever ser acessiveis via servidor, apenas localmente pelo Desenvolvedor responsável pela tarefa.

Em caso de dúvidas sobre como utilizar a ferramenta do Git ou a plataforma do GitHub, indico olhar meu repositório [Git](https://github.com/RhianLopes/Git), lá explico desde o inicio passo a passo para iniciantes na ferramenta em uma linguagem informal.

### 🎯 Padrão

Para a criação de branch deve ser seguido o seguinte padrão:

```
<tipo>/<escopo>
```

Exemplo:
```
feature/user-login-persistence
fix/user-order
```

#### Tipo: 

Os tipos dados as branchs devem ser os apresentados abaixo:

- ```feature```: Novas funcionalidades
- ```fix```: Ajuste em arquivos
- ```refactor```: Melhorias ou Reescritas
- ```remove```: Remoção de arquivos

#### Escopo:

O escopo deve possuir de maneira resumida, clara e curta, a qual abordagem se trata a branch. Deve ser escrita com as letras e palavras em caixa baixa, minúsculo, e deve ser separadas as palavras utilizando ```-``` traços.

### 🛒 Padrão para modificações

O padrão que deve ser seguido pelos desenvolvedores para a criação, modificação ou remoção de código, é a criação de uma branch a partir da ```develop```, após feito as modificações, deve ser atualizada sua branch com a branch ```develop```, em caso de conflitos, devem ser resolvidos, por fim, deve ser criado um Pull Request ou Merge Request.

#### Pull Request:

O Pull Request deve possuir o mesmo nome dado para a branch, ```feature/user-login-persistence```, em casos de alta complexidade no código, é obrigatória a descrição, mas em outros casos é opcional, podendo ser decidido entre a equipe. Em casos de modificações no PR, seja por code review, mudança de regra de negócio, etc... Deve ser adicionado ```WIP: ```, "Work In Progress", na frente do nome do PR:

Exemplo:
```
WIP: feature/user-login-persistence
```

Após devida correção e modificação adicionada no PR, deve ser removido o ```WIP: ``` no nome dado ao PR, retornando ao original.

#### Code Review:

O Code Review é uma prática muito importante entre á equipe em vários, segue o link para saber mais sobre o [Code Review](https://medium.com/trainingcenter/qual-o-real-valor-do-code-review-para-uma-equipe-de-desenvolvimento-f43f894c0a04), deve existir em todos os Pull Request, onde deve ser decidido um número minímo de views ou likes de um PR, a aprovação do equipe em si. Em casos extremos onde é necessária rápida aprovação ou em casos que é necessária a aprovação e o membro está sozinho, é permitida sim, a aprovação do PR sem Views ou Likes, mas o membro estará comprometido em corrigir, caso quebre a aplicação.





