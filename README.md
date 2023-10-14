# Sistema de Controle Acadêmico

Este é um simples sistema de controle acadêmico em JavaScript que permite inserir dados de alunos e exibir uma tabela com informações sobre o desempenho acadêmico deles. Abaixo, você encontrará informações sobre como utilizar as funções disponíveis no código.

## Função `verificartabela()`

A função `verificartabela()` verifica se uma tabela com o ID 'tabela' já existe no documento HTML. Caso não exista, ela cria a tabela e adiciona os cabeçalhos (colunas) à mesma. Se a tabela já existir, ela apenas a retorna. Esta função é utilizada para garantir que a tabela exista antes de inserir um aluno nela.

## Função `inserirAlunoNaTabela(aluno)`

A função `inserirAlunoNaTabela(aluno)` insere os dados de um aluno na tabela. Ela recebe um objeto `aluno` com as seguintes propriedades:

- `matricula`: Número de matrícula do aluno.
- `nome`: Nome do aluno.
- `faltas`: Quantidade de faltas do aluno.
- `notab1`: Nota da primeira avaliação (B1).
- `notab2`: Nota da segunda avaliação (B2).
- `media`: Média parcial das notas do aluno.
- `notapr`: Nota da prova de recuperação (caso aplicável).
- `mediafinal`: Média final do aluno.
- `situacao`: Situação do aluno (aprovado, reprovado por falta, reprovado por nota).

Esta função insere uma nova linha na tabela com as informações do aluno.

## Função `inserirAluno(total_aulas)`

A função `inserirAluno(total_aulas)` permite a inserção de um novo aluno no sistema. Ela solicita informações ao usuário, como matrícula, nome, quantidade de faltas, notas das avaliações (B1 e B2), e, se necessário, a nota da prova de recuperação.

A função calcula a média parcial das notas e verifica a situação do aluno com base nas faltas e notas. Se o aluno tiver mais de 25% de faltas, ele será reprovado por falta. Caso contrário, se a média parcial for maior ou igual a 7, o aluno será aprovado. Se a média parcial for menor que 7, será solicitada a nota da prova de recuperação, e a média final será calculada.

- Se a média final for maior ou igual a 5, o aluno será aprovado.
- Caso contrário, o aluno será reprovado por nota.

A função então insere o aluno na tabela utilizando a função `inserirAlunoNaTabela(aluno)`.

**Exemplo de uso:**
1. Execute a função `inserirAluno(total_aulas)` para inserir um novo aluno no sistema.
2. Insira os dados do aluno quando solicitados.
3. Os dados do aluno serão exibidos na tabela no documento HTML.

Esse é um sistema básico para controle acadêmico que permite inserir e exibir informações sobre alunos.
