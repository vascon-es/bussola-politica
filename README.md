# Minha Bússola Política

Quiz de 30 perguntas, em linguagem simples, para quem não acompanha política e quer um
ponto de partida antes de votar. No fim, ele mostra com qual de três planos de governo
as suas respostas mais se parecem: **PT**, **Missão** ou **PL**.

Leva uns 7 minutos, funciona no celular e não pede cadastro.

## Como usar

- **Online:** abra a página publicada pelo GitHub Pages (veja "Publicar" abaixo).
- **No seu computador:** baixe o `index.html` e abra no navegador. Não precisa instalar nada.

## Como funciona

- Cada pergunta tem três alternativas, uma inspirada em cada plano. A ordem é embaralhada
  e o nome do partido não aparece durante o quiz.
- O resultado é a porcentagem de respostas suas que coincidem com cada plano. Perguntas
  puladas não entram na conta.
- Três réguas mostram o seu jeito de pensar: Estado × mercado, prevenção × mão dura e
  mudança gradual × reformas profundas.
- No fim aparece a lista de todas as suas respostas, com o plano correspondente.

## Limites — leia antes de confiar no resultado

- **As alternativas são resumos simplificados**, não citações dos planos de governo. Elas
  refletem a leitura de quem escreveu o quiz e podem conter erros ou omissões.
- **Só três planos estão aqui.** Existem outros candidatos e partidos.
- **Plano de governo é promessa**, não garantia do que será feito.
- O quiz não recomenda voto. Use o resultado como ponto de partida e leia as propostas
  originais, que ficam registradas no site do TSE:
  [divulgacandcontas.tse.jus.br](https://divulgacandcontas.tse.jus.br).

Achou uma alternativa que não representa bem um plano? Abra uma *issue* ou um *pull
request* apontando o trecho do documento original.

## Privacidade

Tudo roda no seu navegador. Não há servidor, cadastro, anúncios nem rastreamento. As
respostas ficam salvas só no seu aparelho (`localStorage`), para você poder parar e
continuar depois, e são apagadas ao clicar em **Refazer**. A única conexão externa é com o
Google Fonts, para carregar as letras.

## Publicar (GitHub Pages)

No repositório: **Settings → Pages → Build and deployment → Source: Deploy from a branch**,
escolha a branch `main` e a pasta `/ (root)`, e salve. Em um ou dois minutos o quiz fica em
`https://SEU_USUARIO.github.io/bussola-politica/`.

### Render

O `render.yaml` publica o quiz como site estático gratuito: no
[painel do Render](https://dashboard.render.com), **New → Blueprint**, escolha este
repositório e clique em **Apply**. Cada `git push` na `main` publica de novo.

## Contribuir

O app é um único arquivo, `index.html`. As perguntas ficam na lista `Q`, no fim do arquivo:

```js
{t:'Tema', q:'Pergunta?', h:'Dica', ax:'eco', v:{A:-1,B:.7,C:1},
 o:{A:'alternativa do PT', B:'alternativa do Missão', C:'alternativa do PL'}}
```

`ax` e `v` são opcionais e posicionam a resposta em uma das três réguas (`eco`, `sec`, `rit`),
de -1 a 1.

## Licença

[MIT](LICENSE).
