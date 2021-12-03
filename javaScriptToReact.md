# Java Script para React

### Conhecimentos necessários para melhor uso do React.

* Código abaixo pega um elemento com ID root no html e insere uma string.

```
const $root = document.querySelector(#root)
$root.textContent = "Heliezer"
```

### Component JS

* Component é um elemento do HTML que pode ser reutilizado em diversas paginas do seu sistema.
* Um component deve ser isolado para reutilização.


* Função Criada para ser exportada.

```

function NomeFuncao(){
    return `
        <article>
            Dados Article
        </article>
        `:
}

export default NomeFuncao;
```

* Importando o Card no HTML.
  * Não utilize .innerHTML para renderizar o HTML/Elemento em tela por questões de segurança.
  * Em beforeend ver explicação no MDN sobre Element.insertAdjacentElement().
```

import NomeFuncao from 'caminhoComponent';

const $htmlNomeFuncao = NomeFuncao();
const $root = document.querySelector(#root)

$root.insertAdjacentElement("beforeend", $htmlNomeFuncao);

```