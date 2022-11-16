from flask import Flask, render_template

meusite = Flask(__name__)


#criar a 1° pagina do meu site
# route-> meusite.com/paginainicial
# função -> o que você quer exibir na página
#atribuir uma nova funcionalidade a seguir http://127.0.0.1:5000

@meusite.route("/")
def homepage():
    return render_template("homepage.html")

@meusite.route("/historia")
def historia():
    return render_template("historia.hml")

@meusite.route("/hitorias")
def historias ():
    return render_template("historias.html")

#debug=TRUE é para o site reniciar só pq estou arrrumando ele ainda
#agora aqui  iremos colocar o meu site no ar

if __name__ == "__main__":
   meusite.run(debug=True)

# servidor o heroku

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>central de historias</title>
</head>
<body>
 <h1>Guerra Fria </h1>
<h3>A Guerra Fria foi um conflito político-ideológico que foi travado entre Estados Unidos (EUA) e União Soviética (URSS), entre 1947 e 1991. O conflito travado entre esses dois países foi responsável por polarizar o mundo em dois grandes blocos, um alinhado ao capitalismo e outro alinhado ao comunismo.

Ao longo da segunda metade do século XX, a polarização mundial resultou em uma série de conflitos de pequena e média escala em diferentes locais do mundo. Esses conflitos contavam, muitas vezes, com o envolvimento indireto de EUA e URSS, a partir do financiamento, da disponibilização de armas e do treinamento militar.

Contudo, nunca houve um confronto aberto entre americanos e soviéticos, sobretudo pela possibilidade de destruição do planeta em larga escala caso houvesse um conflito entre os dois. Apesar dos discursos afiados e da intensa atuação estratégica para manter sua zona de influência, americanos e soviéticos foram cautelosos ao extremo e evitaram um conflito contra o outro.</h3>
</body>
</html>
