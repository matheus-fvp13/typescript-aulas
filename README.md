# TypeScript Aulas

## O que é?
**TypeScript (TS)** é um **superset** para o **JavaScript (JS)**.

### Mas afinal, o que é um superset?
Para ficar mais fácil de entender, vamos fazer uma analogia com o personagem **Homen de Ferro**.

Podemos comparar o JS com o Tony Stark antes de se tornar o Homem de Ferro. Ele é brilhante, inovador e tem muitas habilidades, mas às vezes suas ações podem ser imprevisíveis e propensas a erros. Tony Stark, assim como o JS, é altamente capaz, mas às vezes sua natureza humana pode levar a resultados inesperados.

O TS pode ser comparado a armadura do homem de ferro que o Tony Stark utiliza para combater os vilões. Desse modo o traje do Homem de Ferro aprimora as habilidades do Tony Stark, assim como o TS melhora o JS adicionando um sistema de tipos robusto, fornecendo uma camada de segurança e prevenção de erros que o JS puro muitas vezes não oferece. 

### Vantagens do TypeScript
- O TypeScript é fortemente tipado, ou seja, suas variaveis possuem tipos. Isso traz um feedback mais rapido ao programador em caso de erros durante a etapa de desenvolvimento.
- Podemos criar interfaces e Enums.
- Pode ser usado em qualquer lugar em que o JS é aceito.
- Documentação oficial: ['https://www.typescriptlang.org/'](https://www.typescriptlang.org/)

### Uma comparação entre o JS e o TypeScript
No JS não é possivel saber o que vai acontecer com o código durante a etapa de desenvolvimento.
```javascript
    function ligar(heroi) {
        console.log("Ligando para :" + heroi.telefone); /*heroi.telefone -> undefined*/
    }

    ligar({
        nome:     "Steve Rogers",
        vulgo:    "Capitão América",
        /*telefone: "11 56789045"*/
    });
```

No TS temos maior controle sobre o nosso código e conseguimos ter um feedback em tempo de desenvolvimento o que evita problemas futuros quando um projeto se torna muito grande.
```typescript
    type Hero = {
        nome: string;
        vulgo: string;
        telefone: string;
    };

    function ligarPara(heroi: Hero) {
        console.log("Ligando para :" + heroi.telefone); /*erro em tempo de desenvolvimento*/
    }

    ligarPara({
        nome:     "Matheus",
        vulgo:    "Iron man",
        /*telefone: "11 3334456"*/
    })
```

