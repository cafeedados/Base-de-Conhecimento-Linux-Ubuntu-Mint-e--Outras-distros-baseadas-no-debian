# SPOTIFY INSTALLATION AND ERROR TREATMENT.

## INSTALLATION

## ERRORS

### ERROR IN DEEPIN - GPG key error: http://repository.spotify.com stable InRelease

I faced an error recently as soon as I was setting up spotfy, when I did the command ``` $ sudo apt update ``` I was faced with the following error:

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

After a search for solutions I managed to find a simple solution to this problem to run just do the following commands:

- FIRST:

```bash
 $ sudo apt install dirmngr
```


- SECOND:

```bash
 $ sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys <aqui voce digita a chave que esta dando error>
```

- THIRD:

```bash
 $ sudo apt update
```

And ready solved, it will download the most current version of Spotfy and will cease this error.

> Bank updated by Pedro Lourenço

<hr>