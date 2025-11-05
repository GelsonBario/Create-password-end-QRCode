# 🛠️ Gerador de Senhas e QR Code

Kit de utilidades para linha de comando, incluindo gerador de QR Code e senhas.

Este projeto é uma ferramenta de console interativa construída em Node.js que permite ao usuário gerar senhas seguras e criar QR codes.

## 🚀 Recursos Principais

### Menu Principal
* **Navegação em Loop:** O menu principal permite que o usuário utilize uma ferramenta e, em seguida, retorne ao menu para escolher outra, sem encerrar o programa.
* **Opção de Saída:** Inclui uma opção "Sair" dedicada para fechar o programa de forma limpa.

### 🔑 Ferramenta de Geração de Senha
* **Interatividade Total:** O usuário define interativamente o comprimento da senha e quais tipos de caracteres incluir (maiúsculas, minúsculas, números, símbolos).
* **Segurança Aprimorada:** Utiliza `crypto.randomInt()` para uma fonte de aleatoriedade criptograficamente segura, ideal para senhas.
* **Conveniência:** Oferece a opção de copiar a senha gerada diretamente para a área de transferência.

### 📱 Ferramenta de QR Code
* **Visualização Dupla:** Exibe o QR Code diretamente no terminal para visualização rápida.
* **Salvar como Imagem:** Permite que o usuário salve o QR Code gerado como um arquivo de imagem `.png` para uso posterior.

## 💻 Tecnologias Utilizadas

Este projeto utiliza diversas bibliotecas para fornecer uma experiência de usuário rica no terminal:

* **`chalk`:** Para estilizar e colorir a saída do console.
* **`clipboardy`:** Para copiar a senha gerada para a área de transferência.
* **`prompt`:** Para coletar de forma interativa as entradas do usuário (ex: comprimento da senha).
* **`qrcode`:** Para gerar e salvar os QR Codes como arquivos de imagem.
* **`qrcode-terminal`:** Para exibir os QR Codes diretamente no terminal.
* **`nodemon`:** (Dependência de desenvolvimento) Para reiniciar automaticamente o aplicativo durante o desenvolvimento.

## ⚙️ Instalação e Configuração

1.  **Clone o repositório:**
    ```bash
    git clone https://seu-repositorio-url/Create-passwor-end-QRCode.git
    cd Create-passwor-end-QRCode
    ```

2.  **Instale as dependências:**
    ```bash
    npm install
    ```

3.  **Crie o arquivo de ambiente:**
    Este projeto usa um arquivo `.env` para variáveis de ambiente. Crie um na raiz do projeto:
    ```bash
    touch .env
    ```
    *(O arquivo `.gitignore` já está configurado para ignorar o `.env`.)*

## ▶️ Como Executar

Você pode executar o projeto usando os scripts definidos no `package.json`:

* **Para produção:**
    ```bash
    npm start
    ```

* **Para desenvolvimento (com auto-reload):**
    ```bash
    npm run dev
    ```

## 📁 Estrutura de Arquivos Recomendada

O projeto está organizado da seguinte forma para manter a modularidade e clareza:
```
├── .env 
├── .gitignore 
├── package.json 
└── src/
├── index.js (Ponto de entrada principal) 
├── prompts/
│ ├── prompt-main.js (Lógica do menu principal)
│ └── prompt-qrcode.js (Perguntas para o QR Code)
└── services/ 
├── password/ 
│ ├── create.js (Lógica de criação da senha) 
│ └── handle.js (Orquestração da senha) 
└── qr-code/ 
├── create.js (Lógica de criação do QR Code) 
└── handle.js (Orquestração do QR Code)
```
