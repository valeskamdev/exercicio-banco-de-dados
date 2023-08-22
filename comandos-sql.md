********# BD - Comandos SQL

## Criar banco de dados

```sql
CREATE DATABASE tecinternet_escola_valeska CHARACTER SET utf8mb4;
```

## Criar tabelas

```sql
CREATE TABLE cursos (
    id TINYINT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    titulo VARCHAR(30) NOT NULL,
    carga_horaria TINYINT NOT NULL,
    professor_id TINYINT NULL
);

CREATE TABLE professores (
    id TINYINT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    nome VARCHAR(50) NOT NULL,
    area_atuacao ENUM('design', 'desenvolvimento', 'infra') NOT NULL,
    curso_id TINYINT NOT NULL
);

CREATE TABLE alunos (
    id TINYINT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    nome VARCHAR(50) NOT NULL,
    data_nascimento DATE NOT NULL,
    primeira_nota DECIMAL(4,2) NOT NULL,
    segunda_nota DECIMAL(4,2) NOT NULL,
    curso_id TINYINT NOT NULL
);
```

## Criar relacionamentos

```sql
ALTER TABLE professores ADD FOREIGN KEY (curso_id) REFERENCES cursos(id);
ALTER TABLE alunos ADD FOREIGN KEY (curso_id) REFERENCES cursos(id);
ALTER TABLE cursos ADD FOREIGN KEY (professor_id) REFERENCES professores(id);
```


