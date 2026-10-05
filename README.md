# Aula IA no Pequeno Negócio (Sebrae RR)

- `index.html`: página com o prompt da calculadora (QR do slide "Crie a sua primeira ferramenta").
- `presente/`: página do presente (QR do slide final), com downloads, prompts e o cadastro.

## Como ligar o cadastro na plataforma da Azza

Abra `presente/index.html`, procure `CADASTRO_URL` e cole o endereço que recebe os cadastros
(webhook da plataforma da Azza, n8n, Make, Zapier ou Google Apps Script). Enquanto estiver vazio,
o formulário não envia nada e avisa a pessoa que o cadastro está sendo configurado.

O formulário envia um POST em JSON com: `nome`, `email`, `whatsapp`, `cidade`, `negocio`, `aceite`,
`origem` (`aula-ia-no-pequeno-negocio-sebrae-rr`) e `enviado_em`.
Para Google Apps Script, troque `CADASTRO_MODO` para `'no-cors'`.
