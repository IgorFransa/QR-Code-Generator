# Minha Primeira Experiência Criando um Gerador de QR Code com HTML e JavaScript

## Introdução
Este foi meu primeiro projeto usando HTML e JavaScript para criar um **Gerador de QR Code**. Meu objetivo era construir uma página web simples onde o usuário pudesse inserir um texto (como um URL) e gerar um QR Code que pudesse ser escaneado. Foi uma experiência desafiadora, e neste documento compartilho como desenvolvi o projeto, os obstáculos que enfrentei e o que aprendi no processo.

## O Projeto
O projeto consiste em uma aplicação web que permite ao usuário digitar um texto ou URL em um campo de entrada, clicar em um botão e gerar um QR Code dinamicamente. Usei a biblioteca `qrcode.js` para gerar o QR Code e manipulei o DOM com JavaScript para tornar a página interativa.

### Tecnologias Utilizadas
- **HTML**: Para estruturar a página com um campo de entrada, um botão e um elemento para exibir o QR Code.
- **JavaScript**: Para capturar o input do usuário, chamar a biblioteca `qrcode.js` e manipular o DOM.
- **CSS** (opcional): Para estilizar a página e torná-la mais amigável.
- **Biblioteca qrcode.js**: Para gerar o QR Code com base no texto fornecido.

## Como Comecei
Comecei criando um arquivo HTML básico com um título, um campo de entrada (`<input>`), um botão para gerar o QR Code e um `<div>` para exibir o QR Code. Incluí a biblioteca `qrcode.js` via CDN para facilitar. Aqui está um exemplo do código HTML que usei como base:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Gerador de QR Code</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js"></script>
</head>
<body>
    <h1>Gerador de QR Code</h1>
    <input type="text" id="textoInput" placeholder="Digite um texto ou URL">
    <button onclick="gerarQRCode()">Gerar QR Code</button>
    <div id="qrcode"></div>
    <script src="qr_code_generator.js"></script>
</body>
</html>
```

No arquivo `qr_code_generator.js`, implementei a lógica para capturar o texto do input e gerar o QR Code usando a biblioteca `qrcode.js`. Um exemplo simplificado do código JavaScript:

```javascript
function gerarQRCode() {
    const texto = document.getElementById('textoInput').value.trim();
    const qrcodeDiv = document.getElementById('qrcode');

    if (texto === '') {
        alert('Por favor, digite um texto ou URL!');
        return;
    }

    // Limpa o QR Code anterior, se houver
    qrcodeDiv.innerHTML = '';

    // Gera o novo QR Code
    new QRCode(qrcodeDiv, {
        text: texto,
        width: 128,
        height: 128
    });
}
```

## Desafios Enfrentados
1. **Entender a Biblioteca `qrcode.js`**: Como iniciante, precisei ler a documentação da biblioteca para entender como integrá-la e passar o texto do input corretamente.
2. **Manipulação do DOM**: Aprender a limpar o conteúdo de um `<div>` antes de gerar um novo QR Code foi um desafio, já que QR Codes anteriores permaneciam na página.
3. **Validação de Entrada**: Percebi que, sem verificar o input, o usuário poderia tentar gerar um QR Code vazio, o que causava erros. Adicionei uma validação simples para evitar isso.
4. **Depuração**: Algumas vezes, o QR Code não aparecia porque o caminho do CDN ou o ID do elemento estavam incorretos. Usei o console do navegador para identificar esses problemas.

## O Que Aprendi
- **Uso de Bibliotecas Externas**: Aprendi integrar uma biblioteca JavaScript (como `qrcode.js`) em meu projeto e usar suas funcionalidades.
- **Interatividade com JavaScript**: Entendi como capturar eventos de clique e manipular elementos HTML dinamicamente.
- **Resolução de Problemas**: Pesquisar erros no console e buscar respostas em fóruns
- **Validação de Dados**: Descobri a importância de validar inputs para evitar comportamentos errados na aplicação.

## Próximos Passos
Quero melhorar o projeto com as seguintes funcionalidades:
- Adicionar estilos CSS para tornar a interface mais atraente.
- Permitir que o usuário faça o download do QR Code como uma imagem.
- Adicionar opções para personalizar o tamanho ou a cor do QR Code.
- Implementar um histórico de QR Codes gerados, talvez salvando-os no `localStorage`.

## Conclusão
Minha primeira experiência criando um gerador de QR Code com HTML e JavaScript foi incrível! Apesar dos desafios, ver o QR Code sendo gerado dinamicamente na tela e funcionando ao ser escaneado foi muito gratificante. Esse projeto me motivou a continuar aprendendo sobre desenvolvimento web e a explorar mais bibliotecas e funcionalidades. Recomendo a outros iniciantes experimentarem projetos simples como este para entender melhor HTML, JavaScript e a construção de interfaces interativas.
