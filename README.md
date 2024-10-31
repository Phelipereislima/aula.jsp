<%@ page language="java" contentType="text/html; charset=UTF-8" pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulario de Cadastro</title>
</head>
<body>
    <form action="grava.jsp" name="form1">
        <fieldset>
            <legend>Formulario de Cadastro</legend>
            <label for="txtNome">Nome:</label>
            <input type="text" name="txtNome" id="txtNome">
            <br><br>

            <label for="txtIdade">Idade</label>
            <input type="text" id="txtIdade" name="txtIdade">
            <br><br>

            <label for="txtEmail">Email</label>
            <input type="text" id="txtEmail" name="txtEmail">
            <br><br>

            <input type="button" value="salvar" onclick="verificar()">                 
        </fieldset>

    </form>

    <script>
     function verificar(){
      
         var nome = document.getElementById("txtNome").value;
        if( nome.length < 3 || nome.trim() == "" ){
            document.write("nome invalido");
        }

        var idade = document.getElementById("txtIdade").value;
        if(idade.length==0 || isNaN(idade)){
        document.write("idade invalida");
        }

        var email = document.getElementById("txtEmail").value;
        if(email.indexof("@") < 0 ){
            document.write("email invalido");
        }
    }
    </script>

</body>
</html>****
