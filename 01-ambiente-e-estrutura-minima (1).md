# Capítulo 01 — Como a web funciona e a estrutura mínima de um documento

**Projeto:** SEI Plus  
**Referência:** SILVA, Maurício Samy. *Fundamentos de HTML5 e CSS3*. Rio de Janeiro: Novatec, 2015.  
**Escopo da leitura:** Capítulos 1 e 2 — Fundamentos de HTML5 e CSS3

---

## 1. O que a web é, na prática

Antes de escrever qualquer marcação, o primeiro capítulo estabelece que a web não é um programa instalado, e sim um acordo entre duas pontas: alguém pede um arquivo, outro alguém entrega. Tudo o que o SEI Plus fará depois — modelar um fluxo, guardar um modelo de documento — depende de entender esse acordo, porque é ele que permite que a ferramenta rode no navegador de qualquer estação de trabalho sem instalação e sem servidor próprio.

*   **Modelo cliente-servidor:** o navegador (cliente) solicita um recurso; o servidor responde com o arquivo. No SEI Plus, o cliente é o próprio navegador e os dados ficam no armazenamento local da máquina.
*   **Requisição HTTP:** o pedido é feito por um protocolo de texto. Um erro de caminho de arquivo aparece como resposta de recurso não encontrado, e não como erro de código.
*   **URL e domínio:** o endereço indica protocolo, máquina, caminho e arquivo. Publicar o projeto no GitHub Pages significa transformar esse endereço em um domínio estável e acessível.
*   **DNS:** o serviço que traduz o nome do domínio no endereço numérico da máquina que hospeda os arquivos.

## 2. Ambiente de trabalho

O ambiente adotado é deliberadamente mínimo: um editor de texto simples, um navegador e uma pasta de projeto organizada. Não há dependência de IDE proprietária nem de serviço em nuvem para escrever e testar a ferramenta.

*   **Editor:** VS Code como editor principal e Notepad++ como alternativa leve, ambos com realce de sintaxe e codificação UTF-8 sem BOM.
*   **Navegador:** Google Chrome como agente de usuário de referência, utilizando as ferramentas de desenvolvedor para inspecionar a marcação renderizada.
*   **Pasta do projeto:** nomes de arquivo em minúsculas, sem acentuação e sem espaços, para evitar falhas de caminho ao publicar o conteúdo em servidor estático.
*   **Extensão .html:** o arquivo é texto puro interpretado pelo navegador; não existe compilação nesta etapa do projeto.

## 3. O documento mínimo

O primeiro arquivo escrito no projeto é o contêiner de toda a aplicação. Ele não tem interface ainda, apenas a estrutura obrigatória que garante exibição correta de acentuação, idioma declarado e comportamento adequado em telas pequenas.

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SEI Plus - Modelagem Visual de Fluxos Processuais</title>
</head>
<body>
    <!-- Contêiner principal da aplicação web do SEI Plus -->
    <!-- Os elementos semânticos serão integrados na próxima etapa -->
</body>
</html>
```

*   **<!DOCTYPE html>:** declaração que informa ao navegador o padrão adotado, evitando o modo de compatibilidade legado.
*   **<html lang="pt-br">:** elemento raiz com o idioma do documento, informação usada por leitores de tela e por tradutores automáticos.
*   **<head>:** metadados não renderizados: codificação, viewport e título exibido na aba do navegador.
*   **<body>:** área renderizável, onde os elementos de interface serão inseridos.

## 4. Codificação, idioma e validação

A codificação UTF-8 sem BOM mostrou-se indispensável: sem ela, termos como “licitação” e “parecer” chegam ao navegador com caracteres corrompidos. O capítulo também introduz a validação como etapa do processo, e não como formalidade final.

*   **Codificação:** declarar charset no início do head e salvar o arquivo em UTF-8 sem BOM.
*   **Idioma:** lang no elemento raiz, condição para leitura correta por tecnologias assistivas.
*   **Validação:** verificação da marcação no validador do W3C a cada entrega, registrando as correções no relato do capítulo.

## 5. O que isso muda no SEI Plus

Com o contêiner definido, a ferramenta passa a ter um endereço técnico: uma página única, servida como arquivo estático, sem backend obrigatório. Essa decisão é o que sustenta a proposta de soberania digital do projeto — o fluxo processual e os modelos de documentos permanecem na máquina do servidor público, e a publicação se resume a arquivos versionados.

*   **Publicação:** hospedagem estática por GitHub Pages, sem custo de servidor e sem contrato de nuvem.
*   **Portabilidade:** o mesmo documento base serve à versão web e ao empacotamento futuro como extensão do navegador.
*   **Próximo passo:** dividir o contêiner em áreas semânticas (cabeçalho, navegação, conteúdo e painel de modelos).

---

*Registro publicado a partir do hub de referência do SEI Plus.*