<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>LEER Filosofía | Un viaje por las grandes preguntas</title>

<style>
:root{
    --verde:#294d40;
    --verde-claro:#3f6d5c;
    --dorado:#b49355;
    --crema:#f5f0e5;
    --blanco:#fffdf8;
    --texto:#1d2924;
    --gris:#6b746f;
    --linea:#d6cfbf;
}

*{
    box-sizing:border-box;
}

html{
    scroll-behavior:smooth;
}

body{
    margin:0;
    background:var(--crema);
    color:var(--texto);
    font-family:Georgia, "Times New Roman", serif;
    line-height:1.7;
}

/* ---------- GENERAL ---------- */

.container{
    width:min(1050px, 92%);
    margin:auto;
}

button{
    font-family:Arial, sans-serif;
    cursor:pointer;
}

.btn{
    border:none;
    border-radius:30px;
    padding:14px 25px;
    background:var(--verde);
    color:white;
    font-weight:bold;
    transition:.25s;
}

.btn:hover{
    background:var(--verde-claro);
    transform:translateY(-2px);
}

.btn-outline{
    background:transparent;
    border:1px solid var(--verde);
    color:var(--verde);
}

.btn-outline:hover{
    background:var(--verde);
    color:white;
}

.kicker{
    font-family:Arial,sans-serif;
    font-size:12px;
    font-weight:bold;
    letter-spacing:3px;
    text-transform:uppercase;
    color:var(--dorado);
}

/* ---------- HERO ---------- */

.hero{
    min-height:92vh;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;
    padding:40px 20px;

    background:
    radial-gradient(
        circle at center top,
        #fffdf8 0%,
        var(--crema) 65%,
        #e5ddcd 100%
    );
}

.logo{
    font-family:Arial,sans-serif;
    font-weight:bold;
    letter-spacing:6px;
    color:var(--verde);
    font-size:20px;
}

.hero h1{
    font-size:clamp(48px,8vw,90px);
    line-height:.95;
    margin:25px 0;
}

.hero-subtitle{
    font-size:clamp(20px,3vw,29px);
    font-style:italic;
    color:var(--gris);
    max-width:720px;
    margin:0 auto 30px;
}

/* ---------- SECTIONS ---------- */

section{
    padding:90px 0;
}

.section-title{
    font-size:45px;
    line-height:1.1;
    margin:10px 0 20px;
}

.intro{
    max-width:750px;
    font-size:20px;
    color:var(--gris);
}

/* ---------- TIMELINE ---------- */

.timeline{
    position:relative;
    margin:70px auto;
}

.timeline::before{
    content:"";
    position:absolute;
    top:0;
    bottom:0;
    left:50%;
    width:3px;
    background:var(--linea);
    transform:translateX(-50%);
}

.timeline-item{
    width:50%;
    padding:20px 50px;
    position:relative;
}

.timeline-item:nth-child(even){
    margin-left:50%;
}

.timeline-dot{
    position:absolute;
    top:40px;
    right:-11px;

    width:22px;
    height:22px;

    border-radius:50%;
    background:var(--dorado);
    border:5px solid var(--crema);
}

.timeline-item:nth-child(even) .timeline-dot{
    left:-11px;
}

.timeline-card{
    border:1px solid var(--linea);
    background:var(--blanco);
    padding:22px;
    border-radius:18px;

    cursor:pointer;

    transition:.25s;
}

.timeline-card:hover{
    transform:translateY(-5px);
    border-color:var(--dorado);
    box-shadow:0 12px 30px rgba(0,0,0,.07);
}

.timeline-year{
    color:var(--dorado);
    font-family:Arial,sans-serif;
    font-size:11px;
    letter-spacing:2px;
    font-weight:bold;
}

.timeline-name{
    font-size:28px;
    font-weight:bold;
}

.timeline-question{
    color:var(--gris);
    font-style:italic;
}

/* ---------- MODULE ---------- */

.module{
    display:none;

    background:var(--blanco);
    border:1px solid var(--linea);

    padding:45px;
    border-radius:25px;

    box-shadow:0 15px 40px rgba(0,0,0,.06);

    animation:appear .35s ease;
}

.module.active{
    display:block;
}

@keyframes appear{
    from{
        opacity:0;
        transform:translateY(12px);
    }

    to{
        opacity:1;
        transform:translateY(0);
    }
}

.module h3{
    font-size:45px;
    margin:5px 0 20px;
}

.quote{
    border-left:4px solid var(--dorado);
    padding:10px 20px;
    margin:25px 0;
    font-size:22px;
    font-style:italic;
}

.reflection{
    margin-top:30px;
    padding:25px;
    border-radius:16px;
    background:#eee7d8;
}

textarea{
    width:100%;
    min-height:120px;

    margin-top:15px;
    padding:15px;

    border:1px solid var(--linea);
    border-radius:12px;

    background:#fffdf8;

    font-family:Georgia,serif;
    font-size:16px;

    resize:vertical;
}

/* ---------- QUIZ ---------- */

.quiz-question{
    background:var(--blanco);
    border:1px solid var(--linea);

    border-radius:18px;

    padding:25px;
    margin:20px 0;
}

.quiz-question h3{
    margin-top:0;
}

.option{
    display:block;

    padding:10px;
    margin:7px 0;

    border-radius:10px;

    cursor:pointer;
}

.option:hover{
    background:#eee7d8;
}

.result{
    display:none;

    margin-top:35px;

    padding:40px;

    text-align:center;

    border:2px solid var(--dorado);
    border-radius:20px;

    background:var(--blanco);
}

.result-score{
    font-size:70px;
    color:var(--verde);
    font-weight:bold;
}

/* ---------- CERTIFICATE ---------- */

.certificate{
    margin-top:30px;

    padding:45px 25px;

    border:7px double var(--dorado);

    background:#fffdf8;
}

.certificate h2{
    font-size:35px;
}

/* ---------- FOOTER ---------- */

footer{
    background:#203a31;
    color:#f5f0e5;
    text-align:center;
    padding:60px 20px;
}

footer .logo{
    color:#d7bd83;
}

.footer-small{
    font-family:Arial,sans-serif;
    font-size:12px;
    opacity:.7;
}

/* ---------- RESPONSIVE ---------- */

@media(max-width:750px){

    section{
        padding:65px 0;
    }

    .hero h1{
        font-size:52px;
    }

    .timeline::before{
        left:15px;
    }

    .timeline-item,
    .timeline-item:nth-child(even){
        width:100%;
        margin-left:0;
        padding-left:50px;
        padding-right:0;
    }

    .timeline-dot,
    .timeline-item:nth-child(even) .timeline-dot{
        left:4px;
        right:auto;
    }

    .module{
        padding:25px;
    }

    .module h3{
        font-size:36px;
    }
}
</style>
</head>

<body>


<!-- ================= HERO ================= -->

<header class="hero" id="inicio">

<div>

<div class="logo">
LEER · S.A. DE C.V.
</div>

<div class="kicker">
Curso introductorio de filosofía
</div>

<h1>
Un viaje por<br>
las grandes preguntas
</h1>

<p class="hero-subtitle">
"No una colección de respuestas, sino el valor de aprender a preguntar."
</p>

<button
class="btn"
onclick="document.getElementById('curso').scrollIntoView()">

Comenzar curso →

</button>

<button
class="btn btn-outline"
onclick="document.getElementById('sobre').scrollIntoView()">

Conocer el curso

</button>

</div>

</header>


<!-- ================= INTRODUCCIÓN ================= -->

<section id="sobre">

<div class="container">

<div class="kicker">
LEER FILOSOFÍA
</div>

<h2 class="section-title">
No memorices filosofía.<br>
Haz filosofía.
</h2>

<p class="intro">

La filosofía comienza cuando dejamos de aceptar las cosas
simplemente porque siempre han sido así.

Este curso propone un recorrido breve por algunas de las
preguntas que han acompañado al ser humano durante siglos:

¿Quién soy?

¿Qué puedo conocer?

¿Cómo debo vivir?

¿Somos libres?

¿Tiene sentido nuestra existencia?

</p>

</div>

</section>


<!-- ================= CURSO ================= -->

<section id="curso">

<div class="container">

<div class="kicker">
LÍNEA DEL TIEMPO
</div>

<h2 class="section-title">
El recorrido filosófico
</h2>

<p class="intro">
Selecciona una estación de la línea del tiempo para comenzar.
</p>


<div class="timeline">


<!-- SÓCRATES -->

<div class="timeline-item">

<span class="timeline-dot"></span>

<div
class="timeline-card"
onclick="openModule(0)">

<div class="timeline-year">
SIGLO V A. C.
</div>

<div class="timeline-name">
Sócrates
</div>

<div class="timeline-question">
¿Cómo debemos vivir?
</div>

</div>

</div>


<!-- PLATÓN -->

<div class="timeline-item">

<span class="timeline-dot"></span>

<div
class="timeline-card"
onclick="openModule(1)">

<div class="timeline-year">
SIGLO IV A. C.
</div>

<div class="timeline-name">
Platón
</div>

<div class="timeline-question">
¿Qué es la realidad?
</div>

</div>

</div>


<!-- ARISTÓTELES -->

<div class="timeline-item">

<span class="timeline-dot"></span>

<div
class="timeline-card"
onclick="openModule(2)">

<div class="timeline-year">
SIGLO IV A. C.
</div>

<div class="timeline-name">
Aristóteles
</div>

<div class="timeline-question">
¿Qué es una vida buena?
</div>

</div>

</div>


<!-- DESCARTES -->

<div class="timeline-item">

<span class="timeline-dot"></span>

<div
class="timeline-card"
onclick="openModule(3)">

<div class="timeline-year">
SIGLO XVII
</div>

<div class="timeline-name">
René Descartes
</div>

<div class="timeline-question">
¿Qué puedo conocer con certeza?
</div>

</div>

</div>


<!-- NIETZSCHE -->

<div class="timeline-item">

<span class="timeline-dot"></span>

<div
class="timeline-card"
onclick="openModule(4)">

<div class="timeline-year">
SIGLO XIX
</div>

<div class="timeline-name">
Friedrich Nietzsche
</div>

<div class="timeline-question">
¿Quién decide nuestros valores?
</div>

</div>

</div>


<!-- SARTRE -->

<div class="timeline-item">

<span class="timeline-dot"></span>

<div
class="timeline-card"
onclick="openModule(5)">

<div class="timeline-year">
SIGLO XX
</div>

<div class="timeline-name">
Jean-Paul Sartre
</div>

<div class="timeline-question">
¿Somos realmente libres?
</div>

</div>

</div>


<!-- CAMUS -->

<div class="timeline-item">

<span class="timeline-dot"></span>

<div
class="timeline-card"
onclick="openModule(6)">

<div class="timeline-year">
SIGLO XX
</div>

<div class="timeline-name">
Albert Camus
</div>

<div class="timeline-question">
¿Cómo vivir frente al absurdo?
</div>

</div>

</div>


</div>


<!-- ================= MÓDULOS ================= -->

<div id="modules">


<!-- MÓDULO 1 -->

<article class="module" id="module0">

<div class="kicker">
MÓDULO 01
</div>

<h3>
Sócrates
</h3>

<div class="quote">
"Conócete a ti mismo."
</div>

<p>

Sócrates convirtió la conversación y el cuestionamiento
en herramientas filosóficas.

En lugar de presentar grandes teorías sobre el universo,
prefería preguntar a las personas qué significaban realmente
sus propias palabras: justicia, virtud, conocimiento o felicidad.

Su filosofía parte de una idea sencilla pero incómoda:

<b>reconocer que no sabemos algo puede ser el comienzo de la sabiduría.</b>

</p>

<div class="reflection">

<strong>
Pregunta para reflexionar
</strong>

<p>
¿Cuánto de lo que crees realmente has cuestionado?
</p>

<textarea
placeholder="Escribe aquí tu reflexión...">
</textarea>

</div>

<br>

<button
class="btn"
onclick="openModule(1)">

Siguiente: Platón →

</button>

</article>


<!-- MÓDULO 2 -->

<article class="module" id="module1">

<div class="kicker">
MÓDULO 02
</div>

<h3>
Platón
</h3>

<div class="quote">
La alegoría de la caverna.
</div>

<p>

Platón imaginó a seres humanos encadenados dentro de una
caverna que solamente podían observar sombras proyectadas
sobre una pared.

Para ellos, esas sombras constituían la realidad.

La historia plantea una pregunta poderosa:

<b>
¿y si aquello que consideramos real fuera solamente una apariencia?
</b>

</p>

<div class="reflection">

<strong>
Pregunta para reflexionar
</strong>

<p>
¿Qué "sombras" de nuestra época podrían confundirse con la realidad?
</p>

<textarea
placeholder="Escribe aquí tu reflexión...">
</textarea>

</div>

<br>

<button
class="btn"
onclick="openModule(2)">

Siguiente: Aristóteles →

</button>

</article>


<!-- MÓDULO 3 -->

<article class="module" id="module2">

<div class="kicker">
MÓDULO 03
</div>

<h3>
Aristóteles
</h3>

<div class="quote">
La felicidad como una vida vivida de acuerdo con la virtud.
</div>

<p>

Para Aristóteles, vivir bien no consiste simplemente
en experimentar placer.

La buena vida requiere desarrollar hábitos,
carácter y virtudes.

La virtud se encuentra muchas veces en un equilibrio
entre extremos.

No se trata simplemente de saber qué es bueno:

<b>
hay que aprender a vivirlo.
</b>

</p>

<div class="reflection">

<strong>
Pregunta para reflexionar
</strong>

<p>
¿Qué hábito tuyo contribuye realmente a la persona que quieres ser?
</p>

<textarea
placeholder="Escribe aquí tu reflexión...">
</textarea>

</div>

<br>

<button
class="btn"
onclick="openModule(3)">

Siguiente: Descartes →

</button>

</article>


<!-- MÓDULO 4 -->

<article class="module" id="module3">

<div class="kicker">
MÓDULO 04
</div>

<h3>
René Descartes
</h3>

<div class="quote">
"Pienso, luego existo."
</div>

<p>

Descartes llevó la duda hasta sus límites.

Si podemos dudar de nuestros sentidos,
de nuestras creencias e incluso de aquello
que creemos conocer...

¿qué queda?

Descartes encuentra una certeza fundamental:

<b>
si estoy pensando, entonces necesariamente existo como ser que piensa.
</b>

</p>

<div class="reflection">

<strong>
Pregunta para reflexionar
</strong>

<p>
¿De qué estás seguro y cómo sabes que lo sabes?
</p>

<textarea
placeholder="Escribe aquí tu reflexión...">
</textarea>

</div>

<br>

<button
class="btn"
onclick="openModule(4)">

Siguiente: Nietzsche →

</button>

</article>


<!-- MÓDULO 5 -->

<article class="module" id="module4">

<div class="kicker">
MÓDULO 05
</div>

<h3>
Friedrich Nietzsche
</h3>

<div class="quote">
"Dios ha muerto."
</div>

<p>

Nietzsche cuestionó profundamente los valores tradicionales
de la sociedad occidental.

La famosa expresión "Dios ha muerto" no debe entenderse
simplemente como una afirmación religiosa.

También señala una crisis:

¿Qué ocurre cuando los fundamentos tradicionales
que daban sentido a nuestros valores dejan de convencer?

Nietzsche obliga al individuo a enfrentarse con la
responsabilidad de crear y afirmar sus propios valores.

</p>

<div class="reflection">

<strong>
Pregunta para reflexionar
</strong>

<p>
Si nadie te dijera qué debes valorar, ¿qué elegirías valorar?
</p>

<textarea
placeholder="Escribe aquí tu reflexión...">
</textarea>

</div>

<br>

<button
class="btn"
onclick="openModule(5)">

Siguiente: Sartre →

</button>

</article>


<!-- MÓDULO 6 -->

<article class="module" id="module5">

<div class="kicker">
MÓDULO 06
</div>

<h3>
Jean-Paul Sartre
</h3>

<div class="quote">
"Estamos condenados a ser libres."
</div>

<p>

Para Sartre, el ser humano no posee una esencia completamente
determinada que dicte de antemano quién debe ser.

Somos responsables de nuestras elecciones.

Incluso cuando decidimos no actuar,
estamos tomando una decisión.

Por eso la libertad puede resultar incómoda:

<b>
ser libre significa también hacerse responsable de lo que hacemos con nuestra libertad.
</b>

</p>

<div class="reflection">

<strong>
Pregunta para reflexionar
</strong>

<p>
¿Qué decisión estás dejando actualmente en manos de otros?
</p>

<textarea
placeholder="Escribe aquí tu reflexión...">
</textarea>

</div>

<br>

<button
class="btn"
onclick="openModule(6)">

Siguiente: Camus →

</button>

</article>


<!-- MÓDULO 7 -->

<article class="module" id="module6">

<div class="kicker">
MÓDULO 07
</div>

<h3>
Albert Camus
</h3>

<div class="quote">
El absurdo nace del choque entre nuestra búsqueda de sentido y el silencio del mundo.
</div>

<p>

Camus parte de una experiencia profundamente humana:

queremos encontrar un significado definitivo para nuestra existencia,
pero el mundo no necesariamente nos ofrece una respuesta.

A esta tensión la llama <b>absurdo</b>.

Pero Camus no propone simplemente rendirse.

Propone vivir.

Crear.

Experimentar.

Amar.

Y continuar incluso frente a la ausencia de una respuesta definitiva.

</p>

<div class="reflection">

<strong>
Pregunta para reflexionar
</strong>

<p>
Si la vida no viniera con un significado predeterminado,
¿qué significado construirías?
</p>

<textarea
placeholder="Escribe aquí tu reflexión...">
</textarea>

</div>

<br>

<button
class="btn"
onclick="goToQuiz()">

Ir a la evaluación →

</button>

</article>


</div>

</div>

</section>


<!-- ================= EVALUACIÓN ================= -->

<section id="evaluacion">

<div class="container">

<div class="kicker">
EVALUACIÓN FINAL
</div>

<h2 class="section-title">
Ahora te toca filosofar.
</h2>

<p class="intro">

Responde las cinco preguntas.

No buscamos solamente memoria:
buscamos comprensión.

</p>


<form id="quizForm">


<!-- PREGUNTA 1 -->

<div class="quiz-question">

<h3>
1. ¿Qué caracteriza especialmente al método socrático?
</h3>

<label class="option">
<input type="radio" name="q1" value="a">
Aceptar las tradiciones sin cuestionarlas.
</label>

<label class="option">
<input type="radio" name="q1" value="b">
Examinar las ideas mediante preguntas y diálogo.
</label>

<label class="option">
<input type="radio" name="q1" value="c">
Rechazar todo conocimiento.
</label>

</div>


<!-- PREGUNTA 2 -->

<div class="quiz-question">

<h3>
2. En la alegoría de la caverna, las sombras representan principalmente...
</h3>

<label class="option">
<input type="radio" name="q2" value="a">
Una forma de conocimiento perfecto.
</label>

<label class="option">
<input type="radio" name="q2" value="b">
Apariencias tomadas como realidad.
</label>

<label class="option">
<input type="radio" name="q2" value="c">
La felicidad.
</label>

</div>


<!-- PREGUNTA 3 -->

<div class="quiz-question">

<h3>
3. Para Descartes, ¿qué funciona como una certeza fundamental?
</h3>

<label class="option">
<input type="radio" name="q3" value="a">
La riqueza.
</label>

<label class="option">
<input type="radio" name="q3" value="b">
La tradición.
</label>

<label class="option">
<input type="radio" name="q3" value="c">
El hecho de pensar.
</label>

</div>


<!-- PREGUNTA 4 -->

<div class="quiz-question">

<h3>
4. ¿Qué problema plantea Nietzsche con la expresión "Dios ha muerto"?
</h3>

<label class="option">
<input type="radio" name="q4" value="a">
El fin de la necesidad de pensar.
</label>

<label class="option">
<input type="radio" name="q4" value="b">
La crisis de los fundamentos tradicionales de los valores.
</label>

<label class="option">
<input type="radio" name="q4" value="c">
Que la ciencia dejó de existir.
</label>

</div>


<!-- PREGUNTA 5 -->

<div class="quiz-question">

<h3>
5. ¿Qué relación establece Sartre entre libertad y responsabilidad?
</h3>

<label class="option">
<input type="radio" name="q5" value="a">
La libertad elimina toda responsabilidad.
</label>

<label class="option">
<input type="radio" name="q5" value="b">
Nuestra libertad implica hacernos responsables de nuestras elecciones.
</label>

<label class="option">
<input type="radio" name="q5" value="c">
Nadie puede elegir nada.
</label>

</div>


<button
type="button"
class="btn"
onclick="gradeQuiz()">

Terminar curso

</button>

</form>


<!-- RESULTADO -->

<div
class="result"
id="result">

<div class="kicker">
CURSO COMPLETADO
</div>

<div
class="result-score"
id="score">
</div>

<h2 id="resultTitle">
</h2>

<p id="resultMessage">
</p>


<div class="certificate">

<div class="logo">
LEER
</div>

<h2>
Certificado de exploración filosófica
</h2>

<p>
Por haber completado satisfactoriamente
</p>

<p>
<b>
"Un viaje por las grandes preguntas"
</b>
</p>

<p>
LEER S.A. de C.V.
</p>

<p class="footer-small">
Leer · Pensar · Transformar
</p>

</div>

</div>

</div>

</section>


<!-- ================= FOOTER ================= -->

<footer>

<div class="logo">
LEER
</div>

<p>
Leer · Pensar · Transformar
</p>

<p class="footer-small">
Curso demostrativo de filosofía · LEER S.A. de C.V.
</p>

</footer>


<!-- ================= JAVASCRIPT ================= -->

<script>

/* ---------- ABRIR MÓDULOS ---------- */

function openModule(number){

    const modules =
        document.querySelectorAll(".module");

    modules.forEach(function(module){
        module.classList.remove("active");
    });

    const selected =
        document.getElementById("module" + number);

    selected.classList.add("active");

    selected.scrollIntoView({
        behavior:"smooth",
        block:"center"
    });
}


/* ---------- IR AL EXAMEN ---------- */

function goToQuiz(){

    document
        .getElementById("evaluacion")
        .scrollIntoView({
            behavior:"smooth"
        });
}


/* ---------- EVALUAR ---------- */

function gradeQuiz(){

    const correctAnswers = {

        q1:"b",
        q2:"b",
        q3:"c",
        q4:"b",
        q5:"b"

    };


    let score = 0;


    for(
        const question in correctAnswers
    ){

        const selected =
            document.querySelector(
                'input[name="' +
                question +
                '"]:checked'
            );


        if(
            selected &&
            selected.value ===
            correctAnswers[question]
        ){

            score++;

        }

    }


    const result =
        document.getElementById("result");


    const scoreElement =
        document.getElementById("score");


    const title =
        document.getElementById("resultTitle");


    const message =
        document.getElementById("resultMessage");


    scoreElement.textContent =
        score + "/5";


    if(score === 5){

        title.textContent =
            "Impecable.";

        message.textContent =
            "No solamente estudiaste filosofía: empezaste a pensar filosóficamente.";

    }

    else if(score >= 3){

        title.textContent =
            "Buen recorrido.";

        message.textContent =
            "La filosofía no termina en las respuestas; empieza con las preguntas.";

    }

    else{

        title.textContent =
            "El viaje apenas comienza.";

        message.textContent =
            "La filosofía no es una carrera. Regresa a los módulos, vuelve a preguntar y continúa.";

    }


    result.style.display =
        "block";


    result.scrollIntoView({
        behavior:"smooth",
        block:"center"
    });

}

</script>

</body>
</html>
