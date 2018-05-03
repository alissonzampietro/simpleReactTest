
# React test

* Considere o código fonte a seguir:
```javascript
import React, { Component } from "react"
import { render } from "react-dom"

class DrConsulta extends Component {
  constructor(props) {
    super(props)
    this.state = {
      paciente: ''
    }
  }

  handleInputChange = (e) => {
    this.state.paciente = e.target.value
  }

  render() {
    return (
      <div>
        <label>Nome do paciente:</label>
        <input type="text" onChange={this.handleInputChange} />
        <p>
          Bem vindo paciente { this.state.paciente }!
        </p>
      </div>
    )
  }
}

render(<DrConsulta />, document.getElementById("root"));

```

1. No código acima encontre o erro e corrija-o.
2. Ainda usando o código anterior, só mostre a mensagem de boas vindas quando houver valor no input.

* Considere a base:
```javascript
import React, { Component } from "react"
import { render } from "react-dom"

class ExameInput extends Component {
  render() {
    return (
      <div>
        <input />
      </div>
    )
  }
}

class DrConsulta extends Component {

  render() {
    return (
      <div>
        <p>
          Exames Favoritos:
          <button>Raio X</button>
          <button>Emograma</button>
          <button>Ultrassom</button>
        </p>
        <p>
          Exame Prescrito:
          <ExameInput />
        </p>
      </div>
    )
  }
}

render(<DrConsulta />, document.getElementById("root"))
```

3. Considerando o código fonte acima, crie uma aplicação que:
  - Ao clicar em um botão de exame favorito, o nome do exame deve aparecer no input;
  
  
4. Modifique o codigo seguindo as instruções abaixo:
  - Remova o campo "Exame Prescrito" de modo que fique a tela apenas os botões;
  - Conforme clicar nos botões exiba uma lista com o nome dos botões clicados, sem se repetir os nomes;
  - adicione um botão limpar para apagar a lista;
