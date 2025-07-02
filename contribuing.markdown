# Como Contribuir para o Gerador de QR Code

Obrigado por seu interesse em contribuir para o projeto **Gerador de QR Code**! Este é um projeto open source simples construído com HTML, JavaScript e a biblioteca `qrcode.js`. Toda ajuda é bem-vinda, seja corrigindo bugs, sugerindo novas funcionalidades ou melhorando a documentação. Abaixo estão as diretrizes para contribuir.

## Como Contribuir

### 1. Reportando Bugs
Se você encontrar um problema, por favor, abra uma **issue** no repositório:
- Acesse a aba "Issues" no GitHub.
- Clique em "New Issue".
- Use o título para descrever o problema de forma clara (ex.: "QR Code não é gerado com URLs longas").
- No corpo da issue, inclua:
  - Uma descrição do bug.
  - Passos para reproduzir o problema.
  - Comportamento esperado e comportamento atual.
  - (Opcional) Capturas de tela ou logs do console.

### 2. Sugerindo Melhorias
Quer propor uma nova funcionalidade ou melhoria? Abra uma issue com a tag "enhancement":
- Descreva a funcionalidade que você gostaria de adicionar (ex.: "Adicionar opção para baixar o QR Code como imagem").
- Explique por que ela seria útil.
- Se possível, sugira uma ideia de como implementá-la.

### 3. Enviando Alterações no Código
Para contribuir com código, siga estes passos:
1. **Faça um Fork**: Clique no botão "Fork" no topo do repositório para criar uma cópia no seu perfil.
2. **Clone o Repositório**:
   ```bash
   git clone https://github.com/seu-usuario/qr-code-generator.git
   ```
3. **Crie uma Branch**: Use um nome descritivo para sua branch:
   ```bash
   git checkout -b minha-nova-funcionalidade
   ```
4. **Faça suas Alterações**: Edite os arquivos necessários (ex.: `index.html`, `qr_code_generator.js`, ou `styles.css`).
5. **Teste Localmente**: Abra o `index.html` em um navegador para garantir que tudo funciona.
6. **Commit suas Alterações**: Escreva mensagens de commit claras:
   ```bash
   git commit -m "Adiciona funcionalidade de download do QR Code"
   ```
7. **Envie para o GitHub**:
   ```bash
   git push origin minha-nova-funcionalidade
   ```
8. **Abra um Pull Request**: No GitHub, crie um Pull Request (PR) a partir da sua branch. Descreva:
   - O que foi alterado.
   - Por que a mudança é necessária.
   - Como você testou.

### Diretrizes de Código
- **Estilo**: Mantenha o código limpo e comente quando necessário para explicar a lógica.
- **Compatibilidade**: Teste em navegadores modernos (Chrome, Firefox, etc.).
- **Bibliotecas**: Se adicionar dependências, justifique a necessidade e prefira CDNs para facilitar a execução.
- **Validação**: Certifique-se de que o projeto continua funcionando após suas alterações.

### Exemplos de Contribuições
- Corrigir bugs no JavaScript (ex.: problemas com inputs inválidos).
- Adicionar estilos CSS para melhorar a interface.
- Implementar novas funcionalidades, como personalização do tamanho ou cor do QR Code.
- Melhorar a documentação no `README.md` ou adicionar traduções.

## Código de Conduta
Esperamos que todos os colaboradores sejam respeitosos e colaborativos. Seja gentil e construtivo ao interagir com a comunidade.

## Dúvidas?
Se precisar de ajuda, abra uma issue com a tag "question" ou entre em contato pela seção de Discussions (se ativada). Vamos trabalhar juntos para tornar este projeto ainda melhor!