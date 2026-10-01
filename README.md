# Site da Monolito Sistemas

Site da marca e dos apps: o **Balcão PDV** (sistema de caixa) e o **Leitor de Bolso** (leitor de
PDF). É HTML puro, sem biblioteca e sem etapa de build.

```
index.html                  a marca e a vitrine dos apps
balcao/                     página do Balcão PDV (fotos em balcao/img)
leitor-de-bolso/            página do Leitor de Bolso e a política de privacidade dele
img/og.jpg                  imagem que aparece quando alguém compartilha o link
404.html                    página de endereço errado (links completos, porque vale para qualquer pasta)
```

## Contatos e links

Cada página tem um bloco `CONFIG` no fim do arquivo:

- **WhatsApp:** com DDD; o 55 do Brasil entra sozinho.
- **E-mail** e **Instagram** (só o nome, sem @).
- **Balcão:** download e loja online.
- **Leitor:** Google Play, APK e endereço do app no navegador.

Um campo vazio esconde o link que depende dele, em vez de levar a lugar nenhum.

## Acrescentar um app

1. Crie uma pasta com o nome do app (ex.: `meu-app/index.html`). Copie a faixa "Um app da
   Monolito" do topo das outras páginas e use a chave `mono-tema` para o tema claro/escuro.
2. Em `index.html`, dentro de `#listaApps`, acrescente um cartão `<a class="app">` antes do
   cartão "O próximo app".
3. Acrescente o link no rodapé, na lista "Apps".
4. Acrescente o endereço da página nova em `sitemap.xml`.

## Publicação

O GitHub Pages publica o que está na branch `main`: Settings → Pages → *Deploy from a branch* →
`main` / `/ (root)`. O endereço é **https://pablo107564-ops.github.io/monolito/**.

O endereço completo também aparece no `og:image`, `og:url` e `canonical` do topo de cada página
e no `sitemap.xml`/`robots.txt`. Se o site mudar de endereço (um domínio próprio, por exemplo),
troque em todos esses lugares.

A política do Leitor fica em
`https://pablo107564-ops.github.io/monolito/leitor-de-bolso/privacidade.html`. É a URL
pública que a Google Play pede na ficha do app.
