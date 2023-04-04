<h1 align="center">API ServeRest</h1>

<i><h4 align="center">Servidor REST utilizado para o challenge final da trilha de Postman da Compass UOL</h4></i>


<p align="center">
 <img alt="Logo do ServeRest" src="https://user-images.githubusercontent.com/29241659/115161869-6a017e80-a076-11eb-9bbe-c391eff410db.png" height="120">
</p>

Com o ServeRest podemos estudar uma variedade de assuntos, mas para o desafio especifico focaremos em estudar
- Verbos *GET, POST, PUT* e *DELETE*
- Testes de API manuais
- Testes de API automatizados


<b><h2 align="center">Ambientes disponíveis para rodar o Servidor</h2></b>

<table align="center">
  <tr>
    <td align="center">Online em serverest.dev<br/><a href="#online"><img alt="Texto serverest.dev" src="https://user-images.githubusercontent.com/29241659/97096352-49b1b380-1641-11eb-9b0a-5bb72e1b3882.png" height="80"></a></td>
    <td align="center">Local com NPM<br/><br/><a href="#localmente-com-npm"><img alt="Logo do NPM" src="https://user-images.githubusercontent.com/29241659/97096283-4bc74280-1640-11eb-920a-1c145b0c39d4.png" height="60"></a></td>
  </tr>
</table>

<p align="center">
 <img alt="Print do ServeRest iniciado no terminal" src="https://user-images.githubusercontent.com/29241659/97097145-fa24b500-164b-11eb-9a1f-f9cae275ec98.png" height="124">
</p>

## Consumindo o ServeRest

O ServeRest está disponível de forma [online](https://serverest.dev) e no [npm](https://www.npmjs.com/package/serverest).

As duas opções possuem as mesmas rotas, regras, dados pré-cadastrados e documentação. 

Ressalta-se que no online os dados cadastrados são removidos diariamente. Já no ambiente local basta reiniciar o ServeRest.


### Acessando o ambiente Online

Acesse **<https://serverest.dev>**. Nesse link será disponível visualizar a documentação e as rotas disponíveis para esse servidor.

O ServeRest online possui monitoramento constante do status e tempo de atividade para garantir que esteja sempre disponível.

### Localmente com NPM

Execute o seguinte comando no terminal:

```sh
npx serverest@latest
```

<details><summary><i>Abra para ver detalhes de configuração do ServeRest com NPM</i></summary>

## Configuração

Para visualizar as configurações que são possíveis de serem feitas execute o comando:

```sh
npx serverest -h
```

![Informação de opções e exemplos fornecidos no terminal](https://user-images.githubusercontent.com/29241659/84348644-d45eae00-ab8b-11ea-89a4-d8cda3b32b74.png)

#### Segurança (`--nosec`)

Por default, o _ServeRest_ irá fazer as seguintes alterações no cabeçalho, que podem ser desabilitadas com `npx serverest --nosec`:

**Cabeçalhos adicionados:**
- `Strict-Transport-Security: max-age=15552000; includeSubDomains`
- `X-Content-Type-Options: nosniff`
- `X-DNS-Prefetch-Control: off`
- `X-Download-Options: noopen`
- `X-Frame-Options: SAMEORIGIN`
- `X-XSS-Protection: 1; mode=block`

**Cabeçalho removido:**
- `X-Powered-By: Express`

Utilize esse comportamento nos seus testes, validando a presença/ausência desses cabeçalhos.

> Para saber mais leia o [checklist de segurança de API](https://github.com/shieldfy/API-Security-Checklist#api-security-checklist)

---

</details>

