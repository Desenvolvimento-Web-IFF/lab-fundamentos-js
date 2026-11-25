# Lista de Compras — Laboratório de JavaScript e DOM

Projeto base para a prática de fundamentos de JavaScript *client-side*, manipulação do DOM e programação orientada a eventos.

## Como executar
Abra o arquivo `index.html` diretamente no navegador (duplo clique) e pressione **F12** (aba **Console**) para acompanhar a execução e depurar o código.

## Estrutura de Arquivos
- `index.html` — Estrutura semântica e elementos de interface (validado na W3C).
- `style.css` — Estilização base (inclui a classe `.alerta` para orçamento excedido).
- `app.js` — Arquivo onde toda a lógica da aplicação deve ser implementada.

## Contrato de Seletores (DOM)
| Seletor | Elemento | Finalidade |
| :--- | :--- | :--- |
| `#nome` | `<input type="text">` | Nome do item |
| `#preco` | `<input type="number">` | Preço unitário |
| `#quantidade` | `<input type="number">` | Quantidade do item (padrão: `1`) |
| `#btn-adicionar` | `<button>` | Dispara o cadastro do item |
| `#mensagem` | `<p>` | Exibe mensagens de erro de validação |
| `#qtd-itens` | `<strong>` | Quantidade de itens cadastrados (`itens.length`) |
| `#total` | `<strong>` | Soma dos subtotais (`preco * quantidade`) |
| `#saldo` | `<strong>` | Saldo restante (`LIMITE - total`) |
| `#desconto` | `<p>` | Exibe o valor com 10% de desconto quando o total passar de R$ 150,00 |
| `#status-orcamento` | `<p>` | Status visual do orçamento (alterna a classe `.alerta`) |
| `#lista` | `<ul>` | Container onde os itens (`<li>`) são renderizados |
| `#btn-desfazer` | `<button>` | Remove o último item adicionado (`itens.pop()`) |
| `#btn-limpar` | `<button>` | Limpa toda a lista e redefine o estado |

## Requisitos Obrigatórios
1. **Cadastro e Renderização:** Ler `#nome`, `#preco` e `#quantidade`, armazenar no array `itens`, renderizar na `#lista` com `createElement` + `textContent` e calcular o total (`preco * quantidade`).
2. **Validação:** Bloquear nome vazio, preço menor ou igual a zero (`Number.isNaN`) ou quantidade menor que `1`, exibindo aviso em `#mensagem`.
3. **Controle de Orçamento:** Limite fixo de **R$ 100,00**. Atualizar `#qtd-itens`, `#total` e `#saldo`. Ao ultrapassar o limite, alterar o texto de `#status-orcamento` para `"Orçamento estourado!"` e aplicar a classe `.alerta`.
4. **Desconto Progressivo:** Se o total ultrapassar **R$ 150,00**, exibir em `#desconto` o valor final com 10% de desconto; caso contrário, manter o campo vazio.
5. **Ações de Remoção:** Implementar `#btn-desfazer` (`itens.pop()`) e `#btn-limpar` (`itens = []`), atualizando a interface em ambos os casos.

## Validação e Entrega
- Verifique a ausência de erros na aba **Console** do DevTools (`F12`).
- Faça o commit e o push na pasta `labs/labXX/` do seu repositório Git e envie o link direto da pasta no Classroom.
