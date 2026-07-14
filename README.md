# 🔴 Nível 4 — Vue Router (Navegação)

## 🎯 Objetivo do nível
Múltiplas páginas, navegação entre rotas, rotas dinâmicas.

---

## 🧩 Desafio 10 — Mini-site com 3 páginas

### Requisitos
- [ ] Crie 3 views: `HomeView.vue`, `SobreView.vue`, `ContatoView.vue`
- [ ] Configure as 3 rotas no `router/index.js`
- [ ] Adicione um menu de navegação usando `<RouterLink>` (não use `<a href>` comum!)
- [ ] O conteúdo de cada página troca usando `<RouterView>`, sem recarregar a página inteira

### Conceitos praticados
`createRouter()` · `<RouterLink>` · `<RouterView>` · SPA vs navegação tradicional

### Critério de "pronto"
Você navega entre as 3 páginas pelo menu sem ver a página recarregar (sem "piscar" o navegador).

---

## 🧩 Desafio 11 — Rota dinâmica

### Requisitos
- [ ] Crie uma lista de produtos (pode reaproveitar do Nível 2) na `HomeView`, onde cada item é um link para `/produto/:id`
- [ ] Crie uma `ProdutoDetalheView.vue` que lê o `id` da URL usando `useRoute()`
- [ ] Exiba os dados do produto correspondente àquele `id` (pode ser de uma lista fixa no código por enquanto)

### Conceitos praticados
Rotas com parâmetros (`:id`) · `useRoute().params`

### Critério de "pronto"
Ao clicar em um produto específico na lista, você vai para uma URL única (ex: `/produto/3`) mostrando os dados daquele produto específico.

---

## 🧩 Desafio 12 — Navegação programática

### Requisitos
- [ ] Reaproveite o formulário de cadastro do Desafio 9
- [ ] Após salvar com sucesso, redirecione automaticamente para outra rota (ex: `/produtos`) usando `useRouter().push(...)`
- [ ] Crie um guard simples: se o usuário tentar acessar `/produtos` sem ter "logado" (simule com uma variável booleana simples por enquanto), redirecione para `/login`

### Conceitos praticados
`useRouter()` · `router.push()` · `router.beforeEach()`

### Critério de "pronto"
Ao salvar o formulário, você é redirecionado automaticamente. Ao tentar acessar `/produtos` "deslogado", você cai em `/login`.
