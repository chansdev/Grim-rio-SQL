# GRIMÓRIO SQL
Bem-vindo! Aqui eu coloco tudo que eu to aprendendo nas minhas aulas de SQL pra eu lembrar se precisar!

## CRIAR TABELA
```sql
  drop table Pessoa(
  CPF        int PRIMARY KEY,
  nome        varchar(100),
  data_nasc   varchar(20),
  sexo        varchar(50),
  tipo_sang   varchar(2),
  )
```
## INSERIR VALORES

```sql
  insert into Pessoa values(00000000000, "Nome Sobrenome", "00/00/0000", "sexo", "O-")
```
