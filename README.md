# GRIMÓRIO SQL
Bem-vindo! Aqui eu coloco tudo que eu to aprendendo nas minhas aulas de SQL pra eu lembrar se precisar!

## CRIAR TABELA
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
_drop table **NomeTable**_
```sql
  drop table Pessoa
```
## INSERIR VALORES
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
_FOREIGN KEY (**atributo**) REFERENCES **table**(**atributo**)_
```sql
  create table Pessoa(
  CPF        int PRIMARY KEY,
  nome        varchar(100),
  data_nasc   varchar(20),
  )

  create table compra(
  ID_Compra  int PRIMARY KEY,
  CPF        int,
  FOREIGN KEY (CPF) REFERENCES Pessoa(CPF)
  );
```
### SELECIONAR ENTIDADE
_SELECT **atributo1**, **atributo2**... from **NomeTable**_
```sql
  select Nome, Idade from Cliente where Idade > 18
```
