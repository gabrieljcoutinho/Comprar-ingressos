# Comprar ingresso

# Projeto e-Ticket - Sistema de Compra de Ingressos

Este documento descreve a estrutura funcional do arquivo HTML para o sistema de venda de ingressos.

---

## 1. Cabeçalho e Metadados
O arquivo utiliza a codificação **UTF-8** e é responsivo. As fontes importadas do Google Fonts são:
* **Chakra Petch**: Utilizada para títulos.
* **Inter**: Utilizada para textos de leitura.

Os estilos estão divididos entre um arquivo de **reset** e o arquivo de estilização principal (`style.css`).

---

## 2. Componentes da Interface

### Formulário de Compra
O formulário central permite a interação do usuário com os seguintes elementos:

* **Seleção (`select`)**: ID `#tipo-ingresso`. Possui as opções:
    * `inferior` (Cadeira inferior)
    * `superior` (Cadeira superior)
    * `pista` (Pista)
* **Quantidade (`input`)**: ID `#qtd`. Campo numérico com valor mínimo de 1 e máximo de 10.
* **Ação (`button`)**: Aciona a função JavaScript `comprar()` via evento `onclick`.

### Exibição de Disponibilidade
Uma seção que mostra o estoque atual de ingressos, identificada por IDs específicos para manipulação via DOM:

| Setor | ID do Elemento | Estoque Inicial |
|-------|---------------|-----------------|
| Pista | `qtd-pista` | 100 |
| Cadeira Superior | `qtd-superior` | 200 |
| Cadeira Inferior | `qtd-inferior` | 400 |

---

## 3. Lógica do Sistema
O sistema depende do arquivo `js/app.js` para realizar as seguintes tarefas:
1. Ler o valor do campo `#tipo-ingresso`.
2. Ler a quantidade do campo `#qtd`.
3. Validar se a quantidade solicitada é menor ou igual à disponível no respectivo ID de estoque.
4. Subtrair o valor e atualizar o texto na tela.

---

> **Nota:** Certifique-se de que os caminhos das imagens em `./assets/` e dos estilos em `./styles/` estejam corretos para o carregamento adequado da interface.

<img width="1600" height="810" alt="Image" src="https://github.com/user-attachments/assets/7c599cd7-6536-439b-a0d9-aef38bd0005e" />
