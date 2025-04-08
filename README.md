# GRIMÓRIO SQL
Bem-vindo! Aqui eu coloco tudo que eu to aprendendo nas minhas aulas de SQL pra eu lembrar se precisar!

## CRIAR TABELA
Criando uma tabela chamada Pessoa
_create table **NomeTable**_
```sql
  create table Pessoa(
  CPF        int PRIMARY KEY,
  nome        varchar(100),
  data_nasc   varchar(20),
  sexo        varchar(50),
  tipo_sang   varchar(2),
  )
```
## DELETAR TABELA
Deletando a tabela Pessoa
_drop table **NomeTable**_
```sql
  drop table Pessoa
```
## INSERIR VALORES
Inserindo valores na tabela Pessoa
_insert into **NomeTable** values(**valoresEmOrdem**)_
```sql
  create table Pessoa(
  CPF        int PRIMARY KEY,
  nome        varchar(100),
  data_nasc   varchar(20),
  sexo        varchar(50),
  tipo_sang   varchar(2),
  )
  insert into Pessoa values(00000000000, "Nome Sobrenome", "00/00/0000", "sexo", "O-")
```
## CHAVE ESTRANGEIRA
Indicando que o atributo CPF pertence a tabela Pessoa
_FOREIGN KEY (**atributo**) REFERENCES **table**(**atributo**)_
```sql
  create table compra(
  ID_Compra  int PRIMARY KEY,
  CPF        int,
  FOREIGN KEY (CPF) REFERENCES Pessoa(CPF)
  );
```
## PUXAR INFORMAÇÕES
### Selecionando por Atributos
Selecionando atributos nome e idade da tabela cliente. Você seleciona quantos atributos você quiser
_SELECT **atributo1**, **atributo2**... from **NomeTable**_
```sql
  select Nome, Idade from Cliente
```
Selecionando clientes maiores de idade
_SELECT **atributo1**, **atributo2**... from **NomeTable** where **condição**_
```sql
  select Nome, Idade from Cliente where Idade > 18
```
Selecionando pessoas que tem tipo sanguíneo positivo
_SELECT **atributo1**, **atributo2**... from **NomeTable** where **atributiN** like **condição**_
```sql
  select Tipo_Sang from Pessoa where Tipo_Sang like "+%"
```
### Comandos do like
**%**: Selecionar alguma parte específica da informação<br>
Começa com a
```sql
  select atributo from table where atributo like "a%"
```
Termina com a
```sql
  select atributo from table where atributo like "%a"
```
Indica um caracter que pode ser qualquer coisa
```sql
  select pais from pessoa where pais like "Bra_il"
```
**Todas essas condições podem ser combinadas**

### UPDATE
Usado para manutenção
```sql
  update nome_table set modificação where ;
```

### DELETE
Usado para deletar cúpulas
```sql
  delete from nome_table where atributo = condição;
```

### ALTER TABLE
**add**: Adiciona uma coluna na tabela
```sql
  alter table nome_table add nome_atributo tipo;
```

**drop column**: Deleta uma coluna da tabela
```sql
  alter table nome_table drop column nome_coluna;
```

**rename column**: Renomeia uma coluna da table
```sql
  alter table nome_table rename column nome_antigo to nome_novo;
```

**alter column**: Altera o tipo de valor de uma coluna
```sql
  alter table nome_table alter column nome_coluna novo_tipo;
```

**add primary**: Adiciona uma chave primária se não houver alguma
```sql
  alter table nome_table add PRIMARY KEY (nome_coluna);
```
