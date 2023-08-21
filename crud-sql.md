# CRUD - Cadastro geral

## INSERT

```sql
INSERT INTO cursos (titulo, carga_horaria) VALUES ('Front-End', 40), ('Back-End', 80), ('UX/UI Design', 30), ('Figma', 10), ('Redes de Computadores', 100);

INSERT INTO professores (nome, area_atuacao, curso_id) VALUES ('Pedro Silva', 'infra', 5), ('Ana Santos', 'design', 4), ('João Oliveira', 'design', 3), ('Sofia Rodrigues', 'desenvolvimento', 2), ('Miguel Pereira', 'desenvolvimento', 1);

INSERT INTO alunos (nome, data_nascimento, primeira_nota, segunda_nota, curso_id) VALUES ('Inês Costa', '2000-01-01', 5.00, 6.00, 1), ('Lucas Fernandes', '2000-02-02', 7.00, 8.00, 2), ('Carolina Almeida', '2000-03-03', 9.00, 10.00, 3), ('Guilherme Martins', '2000-04-04', 1.00, 2.00, 4), ('Maria Sousa', '2000-05-05', 3.00, 4.00, 5), ('André Ferreira', '2000-06-06', 5.00, 6.00, 1), ('Beatriz Ribeiro', '2000-07-07', 7.00, 8.00, 2), ('Tiago Moreira', '2000-08-08', 9.00, 10.00, 3), ('Laura Gomes', '2000-09-09', 1.00, 2.00, 4), ('Diogo Carvalho', '2000-10-10', 3.00, 4.00, 5);
```

## UPDATE

```sql
UPDATE cursos SET professor_id = 15 WHERE id = 1;
UPDATE cursos SET professor_id = 14 WHERE id = 2;
UPDATE cursos SET professor_id = 13 WHERE id = 3;
UPDATE cursos SET professor_id = 12 WHERE id = 4;
UPDATE cursos SET professor_id = 11 WHERE id = 5;
```