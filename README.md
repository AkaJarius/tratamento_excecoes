# Tratamento de Exceções

## Problema exemplo:
Três métodos de resolver o problema abaixo:
- muito ruim
- ruim
- bom

![Problema exemplo e diagrama](https://github.com/user-attachments/assets/7eca394d-6c0e-47f1-84b8-d07082629355)

## Exemplos - saída no console

![exemplo1](https://github.com/user-attachments/assets/3cea90cd-c2ce-459f-b9c0-57bf82a5477f)

![exemplo2](https://github.com/user-attachments/assets/0bb404fa-c8ee-494d-afce-90241db77f28)

### Resumo do aprendizado:
- Solução 1 (muito ruim): lógica de validação no programa principal
- Lógica de validação não delegada à reserva
###
- Solução 2 (ruim): método retornando string
- A semântica da operação é prejudicada
- Retornar string não tem nada a ver com atualização de reserva
- E se a operação tivesse que retornar um string?
- Ainda não é possível tratar exceções em construtores
- Ainda não há auxílio do compilador: o programador deve "lembrar" de verificar se houve
erro
- A lógica fica estruturada em condicionais aninhadas
###
- Solução 3 (boa): tratamento de exceções
- Cláusula throws: propaga a exceção ao invés de trata-la
- Cláusula throw: lança a exceção / "corta" o método
- Exception: compilador obriga a tratar ou propagar
- RuntimeException: compilador não obriga
- O modelo de tratamento de exceções permite que erros sejam tratados de forma consistente e
flexível, usando boas práticas
- Vantagens:
      - Lógica delegada
      - Construtores podem ter tratamento de exceções
      - Possibilidade de auxílio do compilador (Exception)
      - Código mais simples. Não há aninhamento de condicionais: a qualquer momento que uma exceção for
      disparada, a execução é interrompida e cai no bloco catch correspondente.
      - É possível capturar inclusive outras exceções de sistema
