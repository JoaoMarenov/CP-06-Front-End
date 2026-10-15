# Checkpoint 6 — Vibecoding

## Contexto e tecnologia

O workspace recebido continha somente `prompt.md`. Não foram encontrados PDF do checkpoint, materiais da disciplina, exemplos, modelos, código existente ou `package.json`. Assim, não foi possível confirmar uma tecnologia exigida pela professora. O portfólio foi criado com HTML, CSS e JavaScript, sem dependências, por ser uma opção estática e simples de compreender para este escopo.

O conteúdo apresenta campos provisórios onde faltavam dados pessoais, tecnologias estudadas, projetos e perfis. Nenhum repositório, endereço de e-mail ou projeto real foi presumido.

## Estrutura criada

- `index.html`: apresentação, sobre, habilidades/aprendizado, projetos, contato e rodapé.
- `styles.css`: paleta, tipografia, cartões, estados de foco, breakpoints e preferência por movimento reduzido.
- `script.js`: menu adaptado para celular, com suporte a clique, navegação por link e tecla Escape.
- `favicon.svg`: ícone vetorial local.
- `README.md`: instruções locais e publicação estática.
- `REFERENCIAS.md`: cinco referências consultadas e decisões de adaptação.
- `HISTORICO_PROMPTS.md`: cópia literal do prompt-base e registro das mensagens e ações.
- `evidencias/`: capturas do projeto em desktop, celular e tela estreita.

## Identidade visual

| Cor | Código | Função |
|---|---|---|
| Fundo principal | `#F8FAFC` | Fundo claro da página |
| Superfícies | `#FFFFFF` | Cartões e seções em destaque |
| Texto principal | `#1E293B` | Títulos e texto sobre fundo claro |
| Destaque | `#2563EB` | Links, ações e marcadores |
| Texto secundário | `#64748B` | Descrições e informações de apoio |
| Bordas | `#E2E8F0` | Separadores e contornos discretos |

Foi usada uma pilha de fontes sem serifa do sistema (`Inter`, `Segoe UI`, `Arial`), sem download externo. A composição usa bastante espaço, cartões simples e detalhes gráficos feitos em CSS.

## Rodadas de desenvolvimento

### Rodada 1 — Estrutura e conteúdo

Foram montadas as seções principais e a navegação por âncoras. Como os projetos e as tecnologias específicas não foram fornecidos, os cartões indicam campos a completar; os contatos aparecem como texto, sem links fictícios.

### Rodada 2 — Identidade visual

Foi aplicada a paleta clara do briefing, com destaque azul, hierarquia tipográfica e cartões com bordas suaves. As referências e as adaptações estão descritas em `REFERENCIAS.md`.

### Rodada 3 — Responsividade

O CSS inclui ajustes para tablet, celular e telas estreitas, além de menu recolhido em telas menores. Também inclui estados de foco visíveis e `prefers-reduced-motion`.

### Rodada 4 — Verificações funcionais

Resultados reais após as verificações executadas nesta sessão:

- A página foi servida localmente por `python -m http.server`; a rota principal respondeu HTTP 200.
- `node --check script.js` terminou sem erros de sintaxe.
- Os 10 links internos têm alvos existentes; não foram encontrados IDs duplicados.
- A largura foi inspecionada com emulação explícita de viewport no Chrome em 320, 390, 768 e 1440 pixels. O documento não ultrapassou a largura do viewport.
- No menu móvel, clique abriu o menu e atualizou `aria-expanded`; o link para `#projetos` navegou ao destino e fechou o menu; Escape também fechou o menu e devolveu o foco ao botão.
- Em desktop, Escape não moveu o foco para o botão móvel oculto.
- A página não usa imagens rasterizadas nem links externos funcionais. A ilustração é feita em CSS e os perfis não fornecidos aparecem como texto provisório.
- O console registrou inicialmente um 404 de recurso causado pela ausência de ícone da página. Foi criado `favicon.svg` e ligado no HTML. Após recarregar e limpar o log anterior, CSS e JavaScript responderam 304 por cache, o ícone respondeu 200 e não houve novos erros no console.
- Uma captura inicial por linha de comando não aplicou a largura CSS móvel como esperado. A verificação foi repetida com dimensões explícitas no Chrome DevTools Protocol; as capturas finais estão em `evidencias/`.
- As capturas conferidas foram [desktop](evidencias/desktop.png), [tablet — primeiro viewport](evidencias/tablet-viewport.png), [celular](evidencias/mobile.png), [celular — primeiro viewport](evidencias/mobile-viewport.png) e [tela estreita de 320 px](evidencias/narrow-viewport.png).

### Correção identificada durante o QA

**Rodada:** 4 — testes funcionais

**Problema encontrado:** o navegador registrava 404 por não haver um ícone local declarado.

**Prompt de correção:** nenhum; foi uma correção autônoma da ferramenta, sem novo prompt do usuário.

**Resultado:** resolvido.

**Como foi verificado:** `favicon.svg` respondeu HTTP 200 e um novo carregamento não registrou erros no console.

**Aprendizado:** conferir os recursos solicitados pelo navegador, além de testar a estrutura principal da página.

**Evidência:** capturas em `evidencias/`.

### Revisão antes do QA

Na revisão do conteúdo, uma localização sem confirmação foi removida. Também foi ajustado o tratamento de Escape para só focar o botão quando o menu móvel está aberto. A informação acadêmica permaneceu baseada no briefing; os dois comportamentos foram verificados no navegador.

## Registro de correções

Não foram inventados erros ou prompts de correção. Até este registro, não houve uma rodada posterior solicitada pelo usuário para corrigir um problema específico. A ficha abaixo fica disponível para uma correção futura:

**Rodada:** [número]

**Problema encontrado:** [descrever o problema observado]

**Prompt de correção:** [copiar o texto exato enviado]

**Resultado:** [resolveu totalmente / parcialmente / não resolveu]

**Como foi verificado:** [descrever a verificação realizada]

**Aprendizado:** [o que poderia ter sido explicado melhor]

**Evidência:** [adicionar captura de tela, se necessário]

## Reflexão para completar

Responder após revisar e personalizar o portfólio:

- O que ficou parecido com a ideia inicial?
- Quais decisões visuais foram mais importantes?
- Quais problemas apareceram durante os testes?
- Quais prompts ajudaram a resolvê-los?
- O que aprendi ao escrever instruções mais específicas?
- O que ainda mudaria no projeto?

## Repositório e deploy

Não há repositório GitHub nem deploy configurado no workspace. O `README.md` contém os passos para executar localmente e publicar os arquivos estáticos no GitHub Pages.

## Pendências pessoais e acadêmicas

- Confirmar se HTML, CSS e JavaScript correspondem ao conteúdo pedido na disciplina, pois os materiais da professora não estavam disponíveis.
- Substituir `[seu nome]` e os demais campos provisórios.
- Adicionar apenas tecnologias, projetos e perfis reais.
- Inserir capturas de tela do projeto final, caso sejam solicitadas na entrega.
- Revisar a captura final após preencher os dados pessoais e acadêmicos.
