# Exercícios de Banco de Dados - Etapa 2

## CRUD - Cadastro geral

### Cadastre pelo menos 5 cursos: 

1. Front-End, carga horária 40h
2. Back-End, carga horária 80h
3. UX/UI Design, carga horária 30h
4. Figma, carga horária 10h
5. Redes de Computadores, carga horária 100h

**Atenção:** por enquanto, deixe o campo professor_id como nulo

```sql
INSERT INTO cursos (titulo, carga_horaria) VALUES ('Front-End', 40), ('Back-End', 80), ('UX/UI Design', 30), ('Figma', 10), ('Redes de Computadores', 100);

```
---

### Cadastre pelo menos 5 professores: 

1. Jon Oliva, área infra
2. Lemmy Kilmister, área design
3. Neil Peart, área design
4. Ozzy Osbourne, área desenvolvimento
5. David Gilmour, área desenvolvimento

**Atenção:** durante o cadastro dos professores, associe cada professor a um curso na ordem contrária dos registros. 

Exemplos: 

- O primeiro professor (Jon Oliva, infra) será atribuido ao último curso (Redes de Computadores)
- O segundo professor (Lemmy, design) será atribuido ao penúltimo curso (Figma)

```sql
INSERT INTO professores (nome, area_atuacao, curso_id) VALUES ('Pedro Silva', 'infra', 5), ('Ana Santos', 'design', 4), ('João Oliveira', 'design', 3), ('Sofia Rodrigues', 'desenvolvimento', 2), ('Miguel Pereira', 'desenvolvimento', 1);
```

---

### Atualize os dados do campo professor_id da tabela cursos, associando cada curso ao seu professor correspondente.


```sql
UPDATE cursos SET professor_id = 15 WHERE id = 1;
UPDATE cursos SET professor_id = 14 WHERE id = 2;
UPDATE cursos SET professor_id = 13 WHERE id = 3;
UPDATE cursos SET professor_id = 12 WHERE id = 4;
UPDATE cursos SET professor_id = 11 WHERE id = 5;
```

---

### Cadastre pelo menos 10 alunos distribuidos aleatoriamente dentre os cursos, com datas de nascimento variadas, notas baixas e altas (sempre entre 0.00 e 10.00).

```sql
INSERT INTO alunos (nome, data_nascimento, primeira_nota, segunda_nota, curso_id) VALUES ('Inês Costa', '1998-05-22', 5.00, 6.00, 1), ('Lucas Fernandes', '2002-12-09', 7.00, 8.00, 2), ('Carolina Almeida', '1999-01-01', 9.00, 10.00, 3), ('Guilherme Martins', '2008-11-21', 1.00, 2.00, 4), ('Maria Sousa', '2009-03-03', 3.00, 4.00, 5), ('André Ferreira', '2005-05-22', 5.00, 6.00, 1), ('Beatriz Ribeiro', '2003-12-27', 7.00, 8.00, 2), ('Tiago Moreira', '2000-06-25', 9.00, 10.00, 3), ('Laura Gomes', '2001-08-08', 1.00, 2.00, 4), ('Diogo Carvalho', '2010-09-10', 3.00, 4.00, 5);
```