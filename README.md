/* Todos os elementos da página */
* {
    margin: 0;
    padding: 0;
}

/* Elementos com o ID "titulo" */
#titulo {
    font-family: sans-serif;
    color: #380B61;
    margin-left: 7%;
} 

/* Elementos com o ID "subtitulo" */
#subtitulo {
    font-family: sans-serif;
    color: #380B61;
    margin-left: 10%;
} 

#check{
    display: inline-block;
}

/* Elementos de tag <fieldset>*/
fieldset {
    border: 0;
}

/* Elemento de tag <body> */
body{
    background-color: #F0F8FF;
    font-family: sans-serif;
    font-size: 1em;
    color: #59429d;
    margin-left: 36%;
    margin-top: 2%;
    justify-content: center;
}

/* Elementos de tags <body>, <input>, <Select>, <textarea> e <button> */
input, select, textarea, button {
    font-family: sans-serif;
    font-size: 1em;
    color: #59429d;
    border-radius: 5px;
}

/* Elementos de classe "grupo" nos estados das pseudoclasses "before" e "after" */
.grupo:before, .grupo:after {
    display: table;
}

/* Elementos de classe "grupo" no estado da pseudoclasse "after" */
.grupo:after {
    clear: both;
}

/* Elementos de classe "campo" */
.campo {
    margin-bottom: 1em;
}

/* Elementos de classe "campo" de tag <label> */
.campo label {
    margin-bottom: 0.2em;
    color: #59429d;
    display: block;
}

/* Elementos de classe "campo" ou "grupo" de tag <fieldset> */
fieldset.grupo .campo {
    float:  left;
    margin-right: 1em;
}

/* Elementos de classe "campo" das tags <input> com atributo text e email, da tag <select> e da tag <textarea>*/
.campo input[type="text"], .campo input[type="email"], .campo select, .campo textarea {
    padding: 0.2em;
    border: 1px solid #59429d;
    box-shadow: 2px 2px 2px rgba(0,0,0,0.2);
    display: block;
}

/* Elementos de classe "campo" de tag <select> e <option>*/
.campo select option {
    padding-right: 1em;
}

/* Elemento de classe "campo" com tag <input>, <select> e <textarea> tocas com estado da pseudoclasse "focus"*/
.campo input:focus, .campo select:focus, .campo textarea:focus {
    background: #E0E0F8;
}

/* Elemento de classe "botao" */
.botao {
    font-size: 1.2em;
    background: #59429d;
    border: 0;
    margin-bottom: 1em;
    color: #ffffff;
    padding: 0.2em 0.6em;
    box-shadow: 2px 2px 2px rgba(0,0,0,0.2);
    text-shadow: 1px 1px 1px rgba(0,0,0,0.5);
    position: absolute;
    top: 90%;
    left: 50%;
    margin-right: -50%;
    transform: translate(-50%, -50%)
}

/* Elemento de classe "botao" com o estado da pseudoclasse "hover" */
.botao:hover {
    background: #CCBBFF;
    box-shadow: inset 2px 2px 2px rgba(0,0,0,0.2);
    text-shadow: none;
}

/* Elementos de classe botão e de tag <select> */
.botao, select{
    cursor: pointer;
} 
 112  formulario.html 
@@ -0,0 +1,112 @@
<!doctype html>
<html>

    <head>
        <!-- Metadados -->
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

        <!-- CSS -->
        <link rel="stylesheet" type="text/css" href="formulario.css" media="screen">

        <!-- Título da página (aparece na aba) -->
        <title>Cadastro</title>
    </head>

    <body>  

        <!-- Cabeçalho com título e subtítulo (ambos com css de id "titulo") -->
        <div>
            <h1 id="titulo">Cadastro de DEVs</h1>
            <p id="subtitulo">Complete suas informações</p>
            <br>
        </div>

        <!-- Início do formulário -->
        <form>

            <fieldset class="grupo">
                <!-- Campo do nome com legenda "nome" e css de classe "campo" -->
                <div class="campo">
                    <label for="nome"><strong>Nome</strong></label>
                    <input type="text" name="nome" id="nome" required>
                </div>

                <!-- Campo do sobrenome com legenda "sobrenome" e css de classe "campo" -->
                <div class="campo">
                    <label for="sobrenome"><strong>Sobrenome</strong></label>
                    <input type="text" name="sobrenome" id="sobrenome" required>
                </div>
            </fieldset> 

            <!-- Campo de email com-->
            <div class="campo">
                <label for="email"><strong>Email</strong></label>
                <input type="email" name="email" id="email" required>
            </div>

            <!-- Campo de desenvolvimento web com 3 opções de botões selecionáveis (radio button) e css de classe "campo" -->
            <div class="campo">
                <label><strong>De qual lado da aplicação você desenvolve?</strong></label>
                <label>
                    <input type="radio" name="devweb" value="frontend" checked>Front-end
                </label>
                <label>
                    <input type="radio" name="devweb" value="backend">Back-end
                </label>
                <label>
                    <input type="radio" name="devweb" value="fullstack">Fullstack
                </label>
            </div>

            <!-- Campo de senioridade com 3 opções para escolha (select option) e css de classe "campo" -->
            <div class="campo">
                <label for="senioridade"><strong>Senioridade</strong></label>
                <select id="senioridade" required>
                  <option selected disabled value="">Selecione</option>
                  <option>Júnior</option>
                  <option>Pleno</option>
                  <option>Sênior</option>
                </select>
            </div>

            <fieldset class="grupo">
                <!-- Campo de tecnologias para escolha de 1 ou mais opções para marcar (checkbox) e css de classe "campo" -->
                <div id="check">
                    <label><strong>Selecione as tecnologias que utiliza:</strong></label><br><br>
                    <input type="checkbox" id="tecnologia1" name="tecnologia1" value="HTML">
                    <label for="tecnologia1"> HTML</label>
                    <input type="checkbox" id="tecnologia2" name="tecnologia2" value="CSS">
                    <label for="tecnologia2"> CSS</label>
                    <input type="checkbox" id="tecnologia3" name="tecnologia3" value="JavaScript">
                    <label for="tecnologia3"> JavaScript</label>
                    <input type="checkbox" id="tecnologia4" name="tecnologia4" value="PHP">
                    <label for="tecnologia4"> PHP</label>
                    <input type="checkbox" id="tecnologia5" name="tecnologia5" value="C#">
                    <label for="tecnologia5"> C#</label>
                    <input type="checkbox" id="tecnologia6" name="tecnologia6" value="Python">
                    <label for="tecnologia6"> Python</label>
                    <input type="checkbox" id="tecnologia7" name="tecnologia7" value="Java">
                    <label for="tecnologia7"> Java</label>
                </div>
            </fieldset>

            <!-- Caixa de texto -->
            <div class="campo">
                <br>
                <label for="experiencia"><strong>Conte um pouco mais da sua experiência: </strong></label>
                <textarea rows="6" style="width: 26em" id="experiencia" name="experiencia"></textarea>
            </div>

            <!-- Botão para enviar o formulário -->
            <button class="botao" type="submit" onsubmit="">Concluído</button>            

        </form>

    </body>

</html>



