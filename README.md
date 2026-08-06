# Efeito Web Experience

Site institucional da Efeito Web, desenvolvido com React, Next.js App Router, Vinext, Vite, GSAP e Tailwind CSS.

O projeto está pronto para desenvolvimento local. As fontes usadas no layout ficam em `public/fonts`, portanto a interface não depende do Google Fonts ou de outro serviço externo para preservar sua identidade visual.

## Requisitos

- Node.js 22.13 ou superior
- npm 10 ou superior

Confira as versões instaladas:

```bash
node --version
npm --version
```

## Instalação

Extraia o ZIP, abra o terminal dentro da pasta `efeito-web-experience` e execute:

```bash
npm ci
```

O `npm ci` usa exatamente as versões registradas em `package-lock.json`. Se você alterar dependências no futuro, use `npm install` para atualizar o arquivo de lock.

## Executar em desenvolvimento

```bash
npm run dev
```

Abra no navegador o endereço informado no terminal, normalmente:

```text
http://localhost:5173
```

Para encerrar, pressione `Ctrl + C` no terminal.

## Gerar e executar a versão de produção

O comando abaixo funciona em Windows, macOS e Linux:

```bash
npm run build:local
npm run start
```

O endereço local será mostrado no terminal.

O projeto também mantém os comandos originais usados pelo ambiente de publicação do Sites. Eles dependem de Bash e utilitários GNU:

```bash
npm run build
npm run validate:artifact
```

No Windows, use Git Bash ou WSL apenas se precisar executar esses comandos específicos. Para desenvolvimento normal, `npm run dev` e `npm run build:local` são suficientes.

## Verificações

```bash
npm run lint:local
npm run test:local
```

## Estrutura principal

```text
efeito-web-experience/
├── src/
│   └── app/
│       ├── globals.css
│       ├── layout.tsx
│       └── page.tsx
├── public/
│   ├── fonts/
│   └── favicon.svg
├── worker/
├── build/
├── scripts/
├── tests/
├── package.json
├── package-lock.json
├── tsconfig.json
├── vite.config.ts
└── README.md
```

## Onde editar

- Conteúdo e componentes da página: `src/app/page.tsx`
- Estilos, responsividade e animações visuais: `src/app/globals.css`
- Metadados e estrutura HTML: `src/app/layout.tsx`
- Imagens, ícones e fontes locais: `public/`
- Dependências e comandos: `package.json`

## Variáveis de ambiente

O site atual não exige variáveis de ambiente, chaves de API, senhas ou tokens para funcionar localmente.

Se uma integração for adicionada futuramente, coloque os valores em um arquivo `.env.local`. Arquivos `.env*` já são ignorados pelo Git e não devem ser enviados para repositórios nem incluídos em novos pacotes ZIP.

## Observações

- Os botões de contato apontam para o WhatsApp da Efeito Web e exigem conexão com a internet ao serem usados.
- `node_modules`, arquivos de build, caches locais, credenciais e o histórico Git não fazem parte do ZIP.
- O identificador presente em `.openai/hosting.json` é apenas a configuração do projeto no Sites; não é uma senha nem um token.
