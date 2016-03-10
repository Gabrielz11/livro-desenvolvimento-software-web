#Formulários HTML e PHP
A criação de um formulário é realizada através das definições (marcações) da linguagem HTML. Para que os dados digitados nos formulários possam ser enviados para um script PHP, são utilizados os métodos (verbos) **GET** e **POST**. 

A seguir é apresentado um exemplo de criação de um formulário em HTML. 
```html
<html>
<body>
    <form name="form1">
        <input name="textNome" type="text">
        <input name="btnEnviar" type="submit" value="Enviar">
    </form>
</body>
</html>
```

No código HTML apresentado anteriormente, foi criado um formulário com nome `form1`; uma caixa de texto `txtNome` e um botão para envio dos dados de nome `btnEnviar`. O atributo `type`  define o tipo do controle HTML que está sendo criado. Para definição da caixa de texto, foi definido o valor `text` para o atributo `type`, enquanto que para um botão, responsável pelo envio dos dados, foi definido o valor `submit`.

##Método GET
O método GET cria um **array** de chaves e valores *(exemplo, chave1=>valor1, chave2=>valor2, ..., chaven=>valorn)*, em que as chaves correspondem aos nomes dos controles dos formulários e os valores correspondem aos dados de entradas fornecidos pelo usuário. 

O atributo `method` define o método de envio dos dados do formulário, conforme exemplificação a seguir:

```html
<html>
<body>
    <form name="form1" method="GET">
        <input name="textNome" type="text">
        <input name="btnEnviar" type="submit" value="Enviar">
    </form>
</body>
</html>
```

Uma vez que o usuário informar algum valor no campo de texto do formulário e clicar no botão **Enviar**, um array de **chave=>valor** será criado e passado via URL. Este array é também chamado de **Query String**. 

Supondo que o usuário digite **John** no campo de texto e clique no botão **Enviar**, o seguinte array será criado e enviado pela URL: 
**?textNome=John&btnEnviar=Enviar**. O caracter **?** separa a URL base do array com os valores. Cada par *chave=>valor* é separado pelo caráter **&**. Por exemplo, se página carregada fosse *index.php*, e estivesse dentro da pasta exemplo, então a URL base poderia ser * http://localhost/exemplo/index.php* . 



