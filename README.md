# battle-knights-aidlc-challenge

Devfile publico da workstation AI-DLC (GitHub Copilot CLI + AI-DLC da AWS) para o OpenShift Dev Spaces.

## Criar o workspace

No painel do Dev Spaces, **Create Workspace** com a URL:

```
https://github.com/leonardofvictor/battle-knights-aidlc-challenge
```

## Pre-requisitos

- Secret `copilot-token` (chave `GH_TOKEN`, PAT com permissao Copilot Requests) no seu namespace, criado antes de iniciar o workspace. Nunca commite o token.
- O cluster precisa alcancar `registry.access.redhat.com`, `registry.npmjs.org` e `github.com`.

A imagem e publica e generica. Ao iniciar, o `postStart` roda `workstation/scripts/post-start.sh`, que instala o Copilot CLI e o AI-DLC nas versoes de `workstation/versions.env`. Para conferir o ambiente, rode o comando `verify` do devfile.
