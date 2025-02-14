# Estilos Padrão das Tags HTML

## ✨ O Que São os Estilos Padrão das Tags HTML?
As páginas da web já possuem um estilo básico sem precisar de CSS. Isso acontece porque os navegadores aplicam estilos padrão (**User Agent Styles**).  

Esses estilos definem:
- **Margens e espaçamentos**
- **Tamanhos de fontes e pesos**
- **Exibição da tag (block, inline, inline-block, etc.)**

Cada navegador pode ter pequenas variações nesses estilos, mas a base é semelhante.

---

## 🌟 Exemplo Prático de Estilos Padrão
Se criarmos um HTML simples **sem CSS**, os elementos já têm estilos aplicados pelo navegador:

```html
<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Estilos Padrão</title>
</head>
<body>
    <h1>Título Principal</h1>
    <p>Isso é um parágrafo. Note o espaço entre esta linha e a de cima.</p>
    <ul>
        <li>Item de lista 1</li>
        <li>Item de lista 2</li>
    </ul>
</body>
</html>
```

### 🔍 O que acontece sem CSS?
- `<h1>`: **Fonte maior e negrito**
- `<p>`: **Margem superior e inferior automática**
- `<ul>`: **Padding na esquerda**
- `<li>`: **Itens organizados verticalmente**

---

## 📊 Estilos Padrão de Algumas Tags Comuns

| **Tag**  | **Tipo de Display** | **Outros Estilos Padrão** |
|----------|-----------------|----------------------|
| `<h1> - <h6>` | **block** | Fonte maior, negrito, margem |
| `<p>` | **block** | Margem acima e abaixo |
| `<a>` | **inline** | Cor azul e sublinhado |
| `<ul>, <ol>` | **block** | Padding na esquerda |
| `<li>` | **block** | Recuo dentro da lista |
| `<img>` | **inline-block** | Sem margem, largura definida pela imagem |
| `<button>` | **inline-block** | Borda e padding aplicados |
| `<input>` | **inline-block** | Padding interno e borda padrão |

---

## 📝 Como Visualizar os Estilos Padrão no Navegador?
Você pode abrir o **DevTools (F12)** e inspecionar um elemento:
1. **Clique com o botão direito** → "Inspecionar elemento"
2. No painel, veja a aba **"Styles"**
3. Role até ver **"User Agent Styles"**

Aqui está um exemplo de como os navegadores aplicam estilos ao `<h1>`:

```css
h1 {
  display: block;
  font-size: 2em;
  font-weight: bold;
  margin: 0.67em 0;
}
```

---

## ✅ Como Resetar os Estilos Padrão?
Se quiser remover os estilos padrão e começar do zero, pode usar um **CSS Reset**:

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

---

## 📝 **Conclusão**
- Os navegadores aplicam **estilos básicos automaticamente**
- Cada tag tem um **tipo de exibição** e **estilos padrão**
- Você pode usar **DevTools** para ver esses estilos
- Pode usar um **reset CSS** para remover os estilos padrão

---

Se quiser explorar mais, tente inspecionar diferentes elementos no DevTools e veja como os navegadores os estilizam! 🚀
# Diferença entre `inline` e `inline-block`

A diferença entre **inline** e **inline-block** está no comportamento do elemento em relação ao fluxo do documento e como ele trata largura e altura.

---

## 📌 **Inline (`display: inline`)**  
Os elementos `inline`:
- ✅ Ocupam **apenas o espaço necessário** no conteúdo.
- ✅ **Não permitem** definir `width` e `height`.
- ✅ Mantêm os elementos na **mesma linha**, sem quebras.

### **Exemplo:**  
```html
<span style="background: yellow;">Texto inline</span> 
<span style="background: lightblue;">Outro inline</span>
```
🔹 Os dois `<span>` ficam na mesma linha e a largura se ajusta ao conteúdo.

---

## 📌 **Inline-block (`display: inline-block`)**  
Os elementos `inline-block`:
- ✅ Também ficam **na mesma linha** que outros elementos.
- ✅ **Permitem definir** `width`, `height`, `margin` e `padding`.
- ✅ São mais fáceis de estilizar do que `inline`.

### **Exemplo:**  
```html
<span style="display: inline-block; width: 150px; height: 50px; background: yellow;">Bloco inline</span>
<span style="display: inline-block; width: 100px; height: 50px; background: lightblue;">Outro bloco</span>
```
🔹 Aqui os elementos têm **tamanhos definidos**, mas continuam na mesma linha.

---

## 🌟 **Resumo**
| **Propriedade** | **Inline** | **Inline-block** |
|---------------|------------|----------------|
| Ocupa apenas o tamanho do conteúdo | ✅ | ✅ |
| Pode definir `width` e `height` | ❌ | ✅ |
| Pode ter `margin` e `padding` externo | ❌ (apenas lateralmente) | ✅ |
| Permite elementos na mesma linha | ✅ | ✅ |

💡 **Dica**: Use `inline-block` quando precisar alinhar elementos horizontalmente **mas ainda quiser controlar tamanhos e espaçamentos**.

---

Se quiser explorar mais, tente inspecionar diferentes elementos no DevTools e veja como os navegadores os estilizam! 🚀

