# Aula IA no Pequeno Negócio (Sebrae RR)

- `index.html`: página com o prompt da calculadora (QR do slide "Crie a sua primeira ferramenta").
- `presente/`: página do presente (QR do slide final), com os downloads e o cadastro.

## Como ligar o cadastro na Azza Academy

Em `presente/index.html`, procure a parte CONFIGURAÇÃO DO CADASTRO e preencha:

- `CADASTRO_URL`: o endereço que recebe os cadastros (criado pela Azza Academy).
- `PLATAFORMA_URL`: a página de login da plataforma, usada se a resposta não trouxer link próprio.

Enquanto `CADASTRO_URL` estiver vazio, o formulário não envia nada e avisa a pessoa.

O formulário envia um POST em JSON: `nome`, `email`, `whatsapp`, `origem` (`aula-ia-no-pequeno-negocio-sebrae-rr`) e `enviado_em`.
A resposta esperada é `{"ok": true, "acesso_url": "...", "mensagem": "..."}`; com ela, a página mostra o botão
"Entrar na plataforma agora". Em caso de erro: `{"ok": false, "erro": "..."}`.

O passo a passo para a Azza Academy está em `cadastro-azza/prompt-para-liberar-na-azza.md`, na pasta da apresentação.
