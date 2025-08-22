# Modelo de Relatório — FAPEMA / UEMA

Este repositório contém um modelo LaTeX para relatórios de Projetos de Iniciação da Universidade Estadual do Maranhão (UEMA) — Proponentes FAPEMA.

## Conteúdo do repositório

- **`modelo.tex`**  
  Arquivo principal em LaTeX que serve como base de relatório, com formatação pronta, seções estruturadas etc.

- **`referencias.bib`**  
  Banco de referências no formato BibTeX para citações dentro do relatório.

- **`imagens/`**  
  Diretório com figuras utilizadas no relatório (placeholder).

---

## Como usar

### 1. Clonar o repositório

```bash
git clone https://github.com/Kiamisa/Modelo-Relatorio-FAPEMA-UEMA.git
cd Modelo-Relatorio-FAPEMA-UEMA
```

### 2. Opção A — Compilar localmente com um editor LaTeX

Você pode usar um editor como **TeXstudio**, **TeXworks**, **TeXmaker**, ou **TeXEditor** (caso prefira):

1. Abra o arquivo `modelo.tex` no editor.
2. Certifique-se de que o seu sistema LaTeX (por exemplo, TeX Live, MiKTeX) esteja instalado.
3. Se estiver usando **biblatex + biber**, basta compilar assim:

   * `pdflatex modelo.tex`
   * `biber modelo` (ou `bibtex modelo`, dependendo do estilo)
   * `pdflatex modelo.tex`
   * `pdflatex modelo.tex` (novamente, se necessário)
4. Quando pronto, você verá o PDF com texto, figuras e referências formatadas.

### 3. Opção B — Usar no Overleaf (online)

1. Acesse [Overleaf](https://www.overleaf.com) e faça login (ou crie uma conta gratuita).
2. Clique em **“New Project”** > **“Upload Project”**.
3. Faça o upload de **todos os arquivos e pastas** do repositório (`modelo.tex`, `referencias.bib`, pasta `imagens/`, etc.).
4. O Overleaf irá sincronizar o projeto; basta clicar em **Recompile**.
5. O sistema cuidará automaticamente da compilação (XeLaTeX, pdfLaTeX etc.) e exibirá o PDF final.

---

## Personalizações

* **Estilo bibliográfico**: você pode alterar o estilo no preâmbulo do LaTeX — por exemplo:

  ```latex
  \usepackage[style=apa, backend=biber]{biblatex}
  ```
* **Referências**: edite o arquivo `referencias.bib` para inserir suas próprias citações.
* **Imagens**: substitua os arquivos na pasta `imagens/` e ajuste `\includegraphics{}` conforme necessário.
* **Formato de documento**: você pode alterar o documentclass (por exemplo, `article`, `report`, `memoir`), margens, fontes e header/footer conforme a necessidade institucional.

---

## Estrutura resumida

| Seção             | Descrição                                          |
| ----------------- | -------------------------------------------------- |
| `modelo.tex`      | Documento base para uso no Overleaf ou local.      |
| `referencias.bib` | Base de dados BibTeX para citações bibliográficas. |
| `imagens/`        | Local para inserir ou substituir figuras.          |
| Compilação local  | Use TeXstudio, TeXworks ou similar + biber/BibTeX  |
| Uso no Overleaf   | Upload do projeto completo e recompilação online   |

---

## Licença

Este projeto está licenciado sob a **MIT License** — veja o arquivo [LICENSE](LICENSE) para mais detalhes.
Isso significa que você pode **usar, copiar, modificar e distribuir** livremente, desde que mantenha o aviso de copyright.

---

### Dicas rápidas

* (Local) Se a bibliografia não aparecer, verifique se você executou Biber ou BibTeX corretamente.
* (Overleaf) Use o log de compilação para detectar erros como nomes de arquivos incorretos ou pacotes faltando.
* (Ambos) Sempre compile duas vezes após inserir novas citações ou referências para garantir atualizações corretas.
