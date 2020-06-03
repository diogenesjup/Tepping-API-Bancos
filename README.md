## Tepping-API-Bancos

<p>API para consulta da lista de bancos no Brasil</p>

> Endpoint
https://tepping-api-bancos.now.sh/bancos.json
<p>&nbsp;</p>

> Exemplo de retorno dos nós:
```
{
    "Code": "001",
    "Name": "BANCO DO BRASIL",
    "Document": "00.000.000/0001-91",
    "CreatedAt": "2017-04-19 15:52:42.400",
    "UpdatedAt": null,
    "DeletedAt": null,
    "IsDeleted": false
  }
```
<p>&nbsp;</p>

> Exemplo de chamada

```
              let bancos = [];

              async function listaBancos(){
                 
                 bancos = await fetch('https://tepping-api-bancos.now.sh/bancos.json').then(res => res.json());
                 
                 if(bancos.length>0){
                    console.log("Deu certo");
                    console.log(bancos);
                 }else{
                   console.log("Deu errado");
                 }
                 
              }

              listaBancos();
```
