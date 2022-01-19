1- Criando seu primeiro repositório no GitHub

2- Clonando seu repositório para maquina local
- criar uma pasta no c: "DIO"
- clicar na pasta com o botão direito e rodar git Bash Here
- ir no gitHub, no repositorio e copiar o link do repositorio na aba code-clone-HTTPS-copiar
- ir no gitBash e dar o comando git clone e colar o link do repositorio (se for na pasta criada ja vai ver o .git e o Readme.md)
- usar o comando cd (e o nome da pasta/)
- git status
- criar uma pasta dentro do repositório LOCAL com o nome introdução ao Git e ao GitHub
- dentro da pasta criar arquivo anotações para listar conteudo do curso
- ao usar git status ja vamos ver que teve a alteração da criação da nova pasta
- usar o comando git add . ou git add -A pra adicionar todos os arquivos
- usar git status ja entende que aquele arquivo seja considerado no controle de versão
- agora usar git commit -m "Inclusão das anotações do curso de Git/GitHub"(comentário)
- usar git status vai mostrar que tem um commit LOCAL e que precisa dar um Push
- usar comando git push origin main

DEVERIA DAR CERTO MAS NÃO...PEDE USUÁRIO E SENHA E DA ESSE ERRO
$ git push origin main
remote: Support for password authentication was removed on August 13, 2021. Please use a personal access token instead.
remote: Please see https://github.blog/2020-12-15-token-authentication-requirements-for-git-operations/ for more information.
fatal: Authentication failed for 'https://github.com/Geisalves54/dio-desafio-github-primeiro-repositorio.git/'


vER ARQUIVO CORRIGINDO O ERRO DE GIT PUSH

1- criar ou copiar o token
2- copiar o link do repositório
3- usar o comando git remote set-url origin e colocar 
git remote set-url origin https://[cole-o-token-aqui]@github.com/[url-do-repositorio]

Ex:
https://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@github.com/Geisalves54/dio-desafio-github-primeiro-repositorio.git
(https://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@github.com/Geisalves54/dio-desafio-github-primeiro-repositorio.git)


 
------

Rideto@kazoo7 MINGW32 /c/DIO
$ git clone https://github.com/Geisalves54/dio-desafio-github-primeiro-repositorio.git
Cloning into 'dio-desafio-github-primeiro-repositorio'...
remote: Enumerating objects: 6, done.
remote: Counting objects: 100% (6/6), done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 6 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (6/6), done.

Rideto@kazoo7 MINGW32 /c/DIO
$ cd dio-desafio-github-primeiro-repositorio/

Rideto@kazoo7 MINGW32 /c/DIO/dio-desafio-github-primeiro-repositorio (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        "Introdu\303\247\303\243o ao Git e ao GitHub/"

nothing added to commit but untracked files present (use "git add" to track)

Rideto@kazoo7 MINGW32 /c/DIO/dio-desafio-github-primeiro-repositorio (main)
$ git add .

Rideto@kazoo7 MINGW32 /c/DIO/dio-desafio-github-primeiro-repositorio (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   "Introdu\303\247\303\243o ao Git e ao GitHub/Anotacoes.md"


Rideto@kazoo7 MINGW32 /c/DIO/dio-desafio-github-primeiro-repositorio (main)
$ git commit -m "Inclusão das anotações do curso de Git/GitHub"
[main c324e2d] Inclusão das anotações do curso de Git/GitHub
 1 file changed, 7 insertions(+)
 create mode 100644 "Introdu\303\247\303\243o ao Git e ao GitHub/Anotacoes.md"

Rideto@kazoo7 MINGW32 /c/DIO/dio-desafio-github-primeiro-repositorio (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

Rideto@kazoo7 MINGW32 /c/DIO/dio-desafio-github-primeiro-repositorio (main)
$ git push origin main
remote: Support for password authentication was removed on August 13, 2021. Please use a personal access token instead.
remote: Please see https://github.blog/2020-12-15-token-authentication-requirements-for-git-operations/ for more information.
fatal: Authentication failed for 'https://github.com/Geisalves54/dio-desafio-github-primeiro-repositorio.git/'

Rideto@kazoo7 MINGW32 /c/DIO/dio-desafio-github-primeiro-repositorio (main)
$ git remote set-url origin https://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@github.com/Geisalves54/dio-desafio-github-primeiro-repositorio.git

Rideto@kazoo7 MINGW32 /c/DIO/dio-desafio-github-primeiro-repositorio (main)
$ git remote -v
origin  https://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@github.com/Geisalves54/dio-desafio-github-primeiro-repositorio.git (fetch)
origin  https://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@github.com/Geisalves54/dio-desafio-github-primeiro-repositorio.git (push)

Rideto@kazoo7 MINGW32 /c/DIO/dio-desafio-github-primeiro-repositorio (main)
$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 2 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 504 bytes | 504.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Geisalves54/dio-desafio-github-primeiro-repositorio.git
   4f44035..c324e2d  main -> main
