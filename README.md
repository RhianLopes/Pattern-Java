# Pattern-Java

## 💡 Ideia

O repositório Pattern-Java, foi criado com a ideia de ser um repositório com os padrões que devem ser seguidos em um projeto com o Back-End em Java, desde as mensagens de commit e branch, até a arquitetura que deve ser usada no java.

## 💻 Commit

As mensagens de commit devem seguir o seguinte padrão...

```
<tipo>(<escopo>): <assunto>
```
Exemplo:
```
feat(UserLogin): add the persistence data in the User Login
fix: ajusts all bugs on User persistence
```

#### Tipo:

O Tipo se refere a que tipo de commit se trata, sejam eles...

- ```feat```: Novas funcionalidades
- ```fix```: Ajuste de Bugs ou Testes
- ```refactor```: Melhoria de código ou aumento de Regra de Negócio
- ```remove```: Remoção de código

#### Escopo:

O Escopo deve servir para referenciar uma Funcionalidade, Documento ou Arquitetura, ex: ```UserLogin, README, Order...```.

Deve ser escrito em [Inglês Americano](https://www.inglesnapontadalingua.com.br/2011/05/o-ingles-americano-tambem-tem-forma.html), excessão de casos onde se referência á alguma Técnologia ou Api externa em outra linguagem.

Deve ser escrito seguindo o padrão [CamelCase](http://java-hunters.blogspot.com/2014/12/o-padrao-camelcase.html) em sua escrita, excessão de casos onde se é modificado diversos arquivos e funcionalidades.

#### Assunto:

Assunto deve também ser escrito em Inglês Americano, igualmente como o Escopo, e não devem ter nenhum tipo de acento em sua escrita.

O assunto deve resumir de maneira curta e clara o que foi feito, modificado ou removido no commit.


