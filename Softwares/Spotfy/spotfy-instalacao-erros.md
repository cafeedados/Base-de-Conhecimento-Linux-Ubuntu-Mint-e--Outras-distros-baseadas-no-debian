# SPOTFY INSTALAÇÃO E TRATAMENTO DE ERROS.

## INSTALAÇÃO


## ERROS 

### ERRO NO DEEPIN - Erro da chave GPG: http://repository.spotify.com stable InRelease


Eu enfrentei um erro recentemente assim que eu estava configurando o spotfy, quando eu fazia o comando ``` $ sudo apt update ``` eu me deparava com o seguinte erro:

```bash
Err:12 http://repository.spotify.com stable InRelease                          
  As assinaturas a seguir não puderam ser verificadas devido à chave pública não estar disponível: NO_PUBKEY 4773BD5E130D1D45
Ign:17 https://dl.bintray.com/getinsomnia/Insomnia  InRelease               
Obter:18 https://dl.bintray.com/getinsomnia/Insomnia  Release [815 B]
Lendo listas de pacotes... Pronto
W: Erro GPG: http://repository.spotify.com stable InRelease: As assinaturas a seguir não puderam ser verificadas devido à chave pública não estar disponível: NO_PUBKEY 4773BD5E130D1D45
E: The repository 'http://repository.spotify.com stable InRelease' is not signed.
N: Updating from such a repository can't be done securely, and is therefore disabled by default.
N: See apt-secure(8) manpage for repository creation and user configuration details.

```

Após uma busca por soluções consegui achar uma solução simples para esse problema para corrir basta fazer os seguintes comandos:

- PRIMEIRO:

```bash
 $ sudo apt install dirmngr
```

-SEGUNDO:

```bash
 $ sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys <aqui voce digita a chave que esta dando error>
```

TERCEIRO:

```bash
 $ sudo apt update
```

E pronto resolvido, ele irá baixar a versão mais atual do Spotfy e irá cessar esse error.

> Banco atualizado por Pedro Lourenço
<hr>