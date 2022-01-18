# Curso de Git
### Autor: Bonieky Lacerda

#### Links úteis:

[Curso completo](https://www.youtube.com/watch?v=OuOb1_qADBQ)

[Meu Instagram](https://www.instagram.com/thaianramalho)

[Contato WhatsApp](https://wa.me/5532936180248)

[Instalar o GIT](https://www.git-scm.com)

[Site Github](https://github.com/)

[Guia para gerar chave SSH](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)

Por que o GIT foi criado?

    1 - problema: em caso de bug, é necessário voltar alterações nos arquivos, mas depois de salvo não era possível.

    2 - problema: não é possível trabalhar em equipe de forma eficiente.

    a partir desses problemas surgiu o versionamento.

Configurando o git:

    Usuário:

    git config --global user.name "Thaian Ramalho"
    git config --global user.email "thaianramalho32@gmail.com"

    Editor:

    git config --global core.editor vscode

Saber as informações cadastradas:

    git config user.name
    git config user.email
    git config --list


Criando um repositório:

    cd /Pasta
    mkdir /PastaDoCurso

Iniciando GIT (já estando na pasta do projeto):

    git init (este comando também cria uma pasta .git oculta)

Verificar o que foi modificado na pasta:

    git status

Adicionar arquivo ao git:

    git add -A (todos) ou git add "nome do arquivo"

Commit:

    git commit -am "mensagem do commit"

Lista de commits feitos:

    git log

Revertendo modificações:

    git reset --soft (voltar para o ultimo commit mas com as modificações preparadas, mas não commitadas)

    git reset --mixed (volta para o ultimo commit, mas com as modificações não preparadas)

    git reset --hard (volta para o ultimo commit e ignora o restante)

Branch:

    git branch (para ver os branchs)

    Criar branch:
    git branch "nome para criar"

    Trocar de branch:
    git checkout "nomedobranch" 

Ver o que foi alterado:

    git diff (ver as alterações de todos os arquivos da lista)

    git diff --name-only (ver apenas nomes dos arquivos modificados)

    git diff nomedoarquivo (ver apenas o que foi alterado naquele arquivo)

Voltar arquivo ao de origem do branch:

    git checkout HEAD --NomeDoArquivo

Enviar arquivo para o GitHub após commit:

    git push
    git push origin
    git push NomeDoRemote NomeDoBranch

Para ignorar arquivos (não serem adicionados no commit) basta criar um arquivo chamado ".gitignore" e dentro dele colocar o nome dos arquivos que não devem ser commitados.

Fazer um commit reverso:

    git revert --no-edit codigoDoCommit

Deletar branchs remotos:

    git push origin :NomeDoBranch

Deletar branchs locais:

    git branch -D NomeDoBranch

Obter arquivos do repositorio remoto para o local:

    git pull
    git pull origin
    git pull NomeDoRemote NomeDoBranch

Clonar projetos:

    git clone UrlDoProjeto

Contribuir com projetos de terceiros com fork:

    Basta clicar em Fork no GitHub
    Copiar a url do projeto em seu repositório
    Fazer suas alterações (add, commit, push)
    Entrar no projeto original e solicitar pull request.