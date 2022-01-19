# Como corrigir o erro

- Você estava usando o git normalmente em sua máquina, mas na hora de dar um **pull** de um repositório do github e sincronizar seu trabalho você se deparou com o seguinte erro:

  > remote: Support for password authentication was removed on August 13, 2021. Please use a personal access token instead.

Não se desespere! Esse é um erro bastante simples de contornar e foi anunciado previamente pelo [Blog do Github](https://github.blog/2020-12-15-token-authentication-requirements-for-git-operations/).

O que acontece é que agora você não pode mais usar a sua senha para se autenticar na sua conta do Github (para operações com o GIT); precisa fazê-lo por meio de um **token**.

- Para gerar um token, é bem simples:
  1. Acesse sua conta do GitHub e clique em **Settings**.
  2. A seguir, vá em Developer Settings
  3. Clique em **Personal access tokens** e a seguir em **Generate new token**
  4. Dê um nome para seu token em **Note** e a seguir marque os checkboxes workflow e write.packages para habilitar as permissões
  5. Agora, você deve copiar o seu token
  6. A última etapa é adicionar o token recém copiado ao endereço do seu repositório remoto: ![github_setremote](https://www.doaction.com.br/user/pages/02.blog/como-corrigir-o-erro-support-for-password-authentication-was-removed-please-use-a-personal-access-token-instead/github_setremote.JPG)
  7. Pronto! Agora você pode seguir com seu trabalho.