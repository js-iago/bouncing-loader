# 🔵 Bouncing Loader

Animação simples de **preloader em estilo bouncing dots** (bolinhas pulando), ideal para mostrar carregamentos de forma leve e moderna em sites e aplicações web.

---

## ✨ Demonstração

Você pode testar o loader localmente abrindo o arquivo `index.html` no navegador.

---

## 📁 Estrutura do Projeto

```
bouncing-loader/
├── index.html       # Estrutura HTML do loader
├── style.css        # Estilos CSS da animação
└── README.md        # Este arquivo de documentação
```

---

## 🚀 Como Usar

1. Copie o HTML do loader para dentro da sua página onde desejar exibir o preloader.
2. Inclua o CSS no seu arquivo principal ou importe como folha de estilo.
3. Customize cores, tamanho e tempo de animação como quiser!

---

## 💡 Exemplo de Uso

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Preloader</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="preloader">
        <div id="status">
            <div class="bouncing-loader">
                <div></div>
                <div></div>
                <div></div>
            </div>
        </div>
    </div>
</body>
</html>

```

```css
#preloader {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: #f6f7fb;
    z-index: 9999;
}

#status {
    position: absolute;
    width: 80px;
    height: 80px;
    top: 50%;
    left: 50%;
    margin: -40px 0 0 -40px;
}

.bouncing-loader {
    display: flex;
    justify-content: center;
}

.bouncing-loader > div {
    width: 13px;
    height: 13px;
    margin: 32px 3px;
    border-radius: 50%;
    background: #727CF5;
    animation: bouncing-loader .6s infinite alternate;
}

.bouncing-loader > div:nth-child(2) {
    animation-delay: .2s;
    background: #FA5C7C;
}

.bouncing-loader > div:nth-child(3) {
    animation-delay: .4s;
    background: #0ACF97;
}

@keyframes bouncing-loader {
    100% {
        opacity: .1;
        transform: translate3d(0, -16px, 0);
    }
}

```

---

Se quiser, já pode colar esse conteúdo no seu `README.md`, salvar e rodar:

```bash
git add README.md
git commit -m "Atualiza README com exemplo e estrutura completa"
git push