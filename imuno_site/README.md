# ImunoLab — Monitoria de Imunologia

Plataforma estática, responsiva e sem login, preparada para deploy na Vercel.

## Conteúdo incluído
- Eixos: Imunologia P1, Imunologia P2 e Imuno-Hemato.
- Texto extraído por página dos três PDFs, pesquisa textual e navegação por página.
- Visualizador dos PDFs originais incorporado à biblioteca (mantém imagens, diagramas e a paginação original).
- 27 flashcards iniciais com respostas explicadas.
- 18 questões de múltipla escolha com feedback, justificativa e resultado por simulado.
- Interface escura responsiva para desktop e dispositivos móveis.

## Rodar localmente
Requer Node.js 20 ou superior.

```bash
npm install
npm run dev
```

## Publicar na Vercel
1. Extraia o ZIP e envie a pasta do projeto para um repositório GitHub.
2. Na Vercel, escolha **Add New → Project** e importe o repositório.
3. A Vercel identifica Vite automaticamente. Build command: `npm run build`; output directory: `dist`.
4. Clique em **Deploy**. Não é necessário configurar variáveis de ambiente nem autenticação.

## Atualizar ou complementar conteúdo
- Os PDFs originais estão em `public/pdfs/`.
- O texto paginado extraído está em `src/materials.json`.
- Flashcards e questões estão no início de `src/main.jsx`, nos arrays `cards` e `questions`.
- Para substituir um PDF, mantenha o caminho/nome atual ou atualize o campo `pdf` correspondente em `src/materials.json`.

## Observações
Esta é uma primeira versão funcional e editável. O conteúdo é educacional, baseado nos materiais enviados; revise a precisão científica das questões e dos resumos antes de disponibilizar como material oficial da monitoria. O navegador do usuário precisa suportar visualização de PDF para exibir o leitor incorporado. Os dados de progresso não são enviados a servidores e não há conta/login.
