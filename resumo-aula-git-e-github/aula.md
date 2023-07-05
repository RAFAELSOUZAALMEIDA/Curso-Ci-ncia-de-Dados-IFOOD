
# Curso Ciencia de Dados IFOODPOTENCIATECH

Minha trilha para o Aprendizado no curso da [Digital Innovation One](https://www.dio.me/) nas area de:

## 📚 Aprendizado em :

- [Python](https://docs.python.org/pt-br/3/)
- [GitHub](https://docs.github.com/pt)
- [Git](https://git-scm.com/docs/git/)
- [Machine Learning](https://azure.microsoft.com/en-us/)
- [SQL](https://cloud.google.com/sql?hl=pt-br)


## 💻 Aulas :
- PRINCIPIOSDE DESENVOLVIMENTO DE SOFTWARE
- PYTHON PARA CIÊNCIA DE DADOS
- DESAFIO DE CÓDIGO EM PYTHON
- MODELAGEM DE DADOS E PROJETOS LÓGICOS COM SQL
- TÉCNICAS E FUNDAMENTOS DE MACHINE LEARNING 

## 📚 Resumo do Aprendizado

# Git e GitHub

# 📚 Materiais de Apoio:

- [Repositorio no github](https://github.com/elidianaandrade/dio-curso-git-github)
- [Slides Sobre Versionamento](https://academiapme-my.sharepoint.com/:p:/g/personal/renato_dio_me/EYjkgVZuUv5HsVgJUEPv1_oB_QWs8MFBY_PBQ2UAtLqucg?rtime=LEMwu59520g)
- [StarckOverFlow](https://stackoverflow.com/) (Importantissima documentação)


## Salvando Alterações no repósitorio local
## Desfazendo Alterações no Repositório remoto:

Controles Básicos:

- Adicionando o arquivo para área de preparação
```
git add   <arquivo>
git add . <inclui vários arquivos>
git log   <mostra o historico de commits>
```
- Inserindo dentro de um commit
```
git commit -m "mensagem que descreva o commit"
```
- Removendo versionamento indesejável
```
rm -rf <arquivo>
```
- Restaurando arquivos
```
git restore <arquivo> ele descarta todas as alterações 
```
- Alterando a mensagem do ultimo commit
```
git commit --amend -m "nova mensagem"
git commit --amend (abre editor) apertando "i" para sair aperte esc : w para escrever e q para sair
```
- Desfazendo commit e retornando ao anterior
```
git reset --soft  (hash do commit) adiciona na area de preparação
git commit -m "mensagem"

git reset --mixed (hash do commit) adiciona 
na area untrack fora da area de preparação
git add .
git commit -m "mensagem"

git reset --hard  (hash do commit) apaga os arquivos  

git reflog (Historico mais detalhado de todas as alterações
feitas)
```
- Observações importantes
**As alterações devem ser feitas antes de serem enviadas para o repositorio remoto
pode geram conflito, caso ja tenha enviado e queira desfazer ou reazer algo, o ideal e refazer a acão enviando um novo commit.**


## Enviando e Baixando Alterações com o Repositório Remoto:

- Primeira coisa a ser feita é conectar 
```
git remote add oringin <URL git>
```
- Não estando dentro da branch main será necessario forçar da Master para main com o seguinte comando 
```
git beanch -M main
```
- Comando responsavel por enviar as alterações do Repositório local para o Repositório Remoto
"-u origin main" significa que o git configura nossa branch "main" que vai estar no nosso repositorio remoto, que chamamos de origin como a branch up stream da nossa branch do repositorio local
```
git push -u origin main
```

## Usando web editor do github

- Para inicializar
clique em "." estando dentro do repositório
caracterizado como o visualcode
la você pode editar seus arquivos em uma outra maquina virtual

conseguindo tambem fazer seus commits por la mesmo pelo icone do visualcode.

## Baixando as Alterações do repositorio remoto  para o local:

- Usando o Comando:
```
git pull 
```
que mescla as alterações do repositorio remoto com as encontradas no repositorio local atualizando todas as alterações.

## Trabalhando com Branchs - Comandos úteis do dia a dia:

```
git pull "nada mais é que a junção de dois Comandos"

git fetch ( que baixa as alterações) + git merge (mescla as alterações)
```
- Baixando as alterações do repositorio remoto(origin) para a branch (main)
```
git fetch origin main
```
- Utilizando o comando:
```
git diff main origin/main
```
- Trazendo as diferenças entre as Branchs e os arquivos commitado 
```
git merge origin/main
```
- Esse comando vai trazer os arquivos da branh remota para a local, podendo ser util apenas para baixar o conteúdo sem ter a necessecidade de mesclar



- Comando util para clonar repositorio que tenha várias Branchs e você so quer clonar uma branch
```
git clone <URL do repositorio> -- branch<nome da branch> --single-branch
```
- Comando usando para arquivar as modificações na branch
```
git stash
```
- Comando para navegar entre as Branchs
```
git checkout <nome da branch>
```
- Comando usado para visualizar as modificações feitas com " git stash"
```
git stash list
```
- Para trazer as alterações listadas anteriormente e excluir as alterações mais recentes da lista com o comando git stash usamos o comando:
```
git stash pop
```
- Para manter as modificações da lista para um uso posterior do comando stash list usamos o comando 
```
git stash apply
```
