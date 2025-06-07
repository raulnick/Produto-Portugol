# 🧪 Cadastro de Produtos Químicos 
## Este programa foi criado para cadastrar produtos químicos, validando as informações e organizando os dados corretamente. Ele também mostra os produtos válidos e fornece um relatório final com os erros.

## 🔁 Estrutura Principal
### O programa funciona dentro de um laço de repetição infinito com enquanto (verdadeiro), exibindo sempre um menu principal com 3 opções:
- [1] Cadastrar novo produto
- [2] Exibir produtos válidos
- [0] Sair

## ✅ Cadastro de Produto
Quando escolhemos a opção [1], o programa solicita os seguintes dados:
- Nome do produto
- Preço (deve ser maior que zero)
- Código da categoria (0 a 5)

Em seguida, ele verifica se os dados são válidos.

*✔ Produto Válido*
- Se tudo estiver certo:
- O nome, preço e categoria são salvos em vetores específicos.
*O programa mostra uma mensagem de sucesso.*

*❌ Produto Inválido*
Se o preço for menor ou igual a zero ou a categoria estiver fora do intervalo de 0 a 5:

- O produto é rejeitado.
- Uma mensagem de erro é mostrada.
*O erro é salvo em um vetor de erros.*

## *📦 Variáveis importantes*
### *codigo++* 
- O número do produto
Explicação simples para a turma:
Pense no codigo como a etiqueta do produto. Cada vez que você cadastra um novo item, seja válido ou inválido, você precisa mudar a etiqueta para o próximo número.

Por isso usamos:

```bash
codigo++
```
O ++ significa "aumenta 1". Então se o código era 3, ele vira 4. Isso garante que os produtos tenham um número sequencial, como: Produto 1, Produto 2, Produto 3, etc.

#### *totalValidos++*
- A posição nos vetores
Toda vez que cadastramos um produto válido, precisamos salvar ele na próxima posição dos vetores de nome, preço e categoria.

Exemplo:

```bash
nomesValidos[totalValidos] = nome
precosValidos[totalValidos] = preco
categoriasValidas[totalValidos] = "Medicinal"
totalValidos++
```
- Se totalValidos vale 0, então o primeiro produto vai na posição 0. Depois aumentamos com totalValidos++ para que o próximo produto vá na posição 1, depois 2, e assim por diante.

## 🧾 Exibir produtos válidos
- Quando o usuário escolhe a opção [2], o programa percorre o vetor de produtos válidos e exibe todos os nomes, categorias e preços já cadastrados corretamente.

## 📊 Relatório Final
- Ao sair do programa ([0]), é exibido um resumo com:

Quantos produtos válidos foram cadastrados
Quantos foram rejeitados
Os motivos de erro para os inválidos