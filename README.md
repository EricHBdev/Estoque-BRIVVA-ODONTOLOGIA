# Estoque-BRIVVA-ODONTOLOGIA
# Sistema de Controle de Estoque Odontológico

Sistema web desenvolvido para facilitar o controle de materiais e insumos utilizados em consultórios odontológicos.

A ideia do projeto é ajudar na organização do estoque, permitindo acompanhar as quantidades disponíveis, datas de vencimento e materiais que precisam ser comprados.

O sistema também contará com sugestões automáticas de reposição, evitando a falta de materiais durante os atendimentos.

## Funcionalidades

### Controle de estoque
- Cadastro, edição e exclusão de materiais.
- Adição de fotos dos produtos.
- Controle de quantidades disponíveis.
- Definição da quantidade máxima de cada material.
- Visualização da porcentagem disponível no estoque.
- Controle de lotes e datas de vencimento.

### Lista de compras
- Adicionar materiais à lista de compras.
- Definir e alterar quantidades.
- Remover itens da lista.
- Marcar materiais como comprados.
- Finalizar listas de compras.

### Sugestões de reposição

O sistema compara a quantidade disponível de cada material com a quantidade máxima cadastrada e sugere o que precisa ser reposto.

**Exemplo:**

| Material | Disponível | Máximo | Comprar |
|---|---|---|---|
| Luvas (caixas) | 2 | 10 | 8 |
| Máscaras (caixas) | 3 | 5 | 2 |
| Resina composta (seringas) | 4 | 10 | 6 |
| Anestésico (caixas) | 5 | 5 | 0 |

As sugestões poderão ser adicionadas diretamente à lista de compras.

### Login e segurança
- Cadastro de usuários.
- Login com e-mail e senha.
- Recuperação de senha.
- Acesso individual aos materiais e listas de compras.

## Tecnologias

O projeto utilizará o Supabase como plataforma de backend.

- **PostgreSQL:** banco de dados relacional.
- **Supabase Auth:** autenticação dos usuários.
- **Supabase Storage:** armazenamento das fotos dos materiais.
- **Row Level Security (RLS):** controle de acesso aos dados.

## Modelagem do banco de dados

O banco de dados será organizado em cinco entidades:

- **Usuário:** informações dos usuários cadastrados.
- **Produto:** cadastro dos materiais odontológicos.
- **Lote:** quantidades disponíveis e datas de vencimento.
- **Lista de Compras:** organização dos materiais que precisam ser comprados.
- **Item da Lista:** materiais adicionados à lista e suas quantidades.

## Cálculo do estoque

O sistema calculará automaticamente a porcentagem disponível de cada material.

**Fórmula:**

`(Quantidade atual / Quantidade máxima) × 100`

Por exemplo, se o estoque máximo de luvas for de 10 caixas e houver apenas 2 disponíveis, o sistema mostrará 20% de estoque e sugerirá a compra de mais 8 caixas.

## Status do projeto

**Em desenvolvimento.**

O projeto está na fase de planejamento e modelagem do banco de dados. As funcionalidades serão implementadas gradualmente.

## Sobre o projeto

Estou desenvolvendo este sistema para aplicar meus conhecimentos em desenvolvimento web e banco de dados, buscando criar uma ferramenta que facilite a organização e o controle de materiais odontológicos no dia a dia de um consultório.
