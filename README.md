# LaTeX

- LaTeX es un sistema de preparación de documentos. Escribe su documento en texto sin formato y, a lo largo del camino, incluye información sobre su estructura. El resultado es un archivo `.pdf` con un formato agradable. Esto tiene un par de ventajas principales en comparación con los procesadores de texto:
    - Es mucho más fácil escribir documentos estructurados, ya que te permite separar claramente el contenido y el formato (te preocupas principalmente por lo primero).
    - la consistencia y calidad tipográfica de sus documentos será excelente
    - Puedes componer cosas que son muy difíciles o imposibles de hacer con procesadores de texto normales.
- Seguramente ya ha notado que `\`, `{` y `}` tienen un significado especial para LaTeX. El signo `\` comienza una instrucción de LaTeX: un «comando». Las llaves `{` y `}` se usan para mostrar *argumentos obligatorios*: información necesaria para los comandos.

## Archivos

Cuando trabajas en un documento LaTeX, trabajas en un archivo `.tex` (por ejemplo, `main.tex`). Esto también se denomina **fuente** o **archivo fuente**. Para obtener un `.pdf`, **compila** ese archivo. En el dorso, compila su archivo haciendo clic en "actualizar vista previa".

# Comandos

Los comandos comienzan con `\`, seguido del nombre del comando. Algunos comandos hacen cosas por sí solos y otros actúan sobre algo más que usted especifica (llamado **argumento**), que coloca entre llaves (`{}`

**Comandos sin argumentos** hacen algo:

`\command`

**Comandos con argumentos** se aplican o se utilizan para seleccionar algo:

`\command{argument}`

Algunos comandos también tienen **argumentos opcionales** (también llamados **opciones**), que pones entre corchetes (`[]`). Estas opciones cambian de alguna manera lo que hace exactamente el comando:

`\command[option]{argument}`

Cuando no sean mutuamente excluyentes, puedes utilizar varias opciones al mismo tiempo separándolas con comas:

`\command[option1,option2]{article}`

También hay **ambientes**, que siempre comienzan y terminan, y se aplicarán a todo lo que esté dentro de ellos.

`\begin{environment}
stuff inside the environment\end{environment}`

Todos los comandos que utilizará se parecerán a los ejemplos anteriores. Será más claro; no te preocupes.

```latex
\section{Introduccion}
```

# **Preámbulo**

es donde va la información relativa a nuestro documento.

### clase de documento

Lo primero que debe determinar es el tipo de documento que escribirá, eligiendo una **clase de documento**. Los más comunes son `article`, `book` o `report`

Lo declaras de la siguiente manera, en la parte superior de tu archivo fuente:

`\documentclass{article}`

Esto seleccionará un diseño que sea apropiado para un artículo.

### Título y Autor

Luego le das un título a tu documento, con el `\title` comando:

`\documentclass{article}
\title{My article}`

Y un autor, con el `\author` comando:

`\documentclass{article}
\title{My article}
\author{John Smith}`

## Documento

Ahora comenzará a escribir su contenido real, utilizando el entorno `document`.

`\documentclass{article}
\title{My article}
\author{John Smith}`

`\begin{document}
The content of our article will be here.`

`\end{document}`

actualizar vista previa

Todo lo anterior `\begin{document}` se considerará preámbulo, y todo lo que vaya desde ese punto hasta `\end{document}` será el contenido del documento. Todo lo que esté debajo de `\end{document}` será ignorado.

- Mostremos el título y el autor con el comando `\maketitle` en tu documento:

### Fecha

También verás que ha aparecido la fecha de hoy. ‘\date{2020}’

```latex
\documentclass{article}
\title{My article}
\author{John Smith}
\date{2017}

\begin{document}
\maketitle

\end{document}
```

## Secciones

Un artículo suele tener **secciones**. Démosle a nuestro documento una sección de “Introducción”, usando el comando `\section`:

`\documentclass{article}
\title{My article}
\author{John Smith}`

`\begin{document}
\maketitle`

`\section{Introduction}`

`\end{document}`

- Al usar el tipo de documento estándar `article`, LaTeX numerará las secciones y subsecciones y pondrá los títulos en negrita.
- LaTeX puede estructurar el documento en bastantes niveles:
    - `\chapter` (pero para poder utilizarlo debemos utilizar `\documentclass{book}` o `\documentclass{report}`)
    - `\section`
    - `\subsection`
    - `\subsubsection`
    - Podemos ir más lejos: el siguiente es `\paragraph`, pero casi siempre esto será ir demasiado «lejos» en una sección (sí, `\paragraph` es un comando de sección, ¡*no* una forma de comenzar un nuevo párrafo!).
    
    ```latex
    \documentclass{article}
    \usepackage[T1]{fontenc}
    \begin{document}
    ¡Hey mundo!
    
    Éste es un primer documento.
    
    \section{Título de la primera sección}
    
    Texto del contenido de la primera sección
    
    Segundo párrafo.
    
    \subsection{Subsección de la primera sección}
    
    Texto del contenido de la subsección.
    
    \section{Segunda sección}
    
    Texto de la segunda sección.
    
    \end{document}
    ```
    

# comentarios

- Podemos añadir comentarios en el archivo LaTeX comenzándolos con `%`

# énfasis y cursiva

```latex
Texto con \emph{énfasis y contenido \emph{anidado}}.

Texto en \textit{cursiva y contenido \textit{anidado}}
```

# Listas

```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\begin{document}

Numerada
\begin{enumerate}
  \item Una entrada
  \item Otra
  \item ¡Guau! Tres entradas
\end{enumerate}

No enumerada
\begin{itemize}
  \item Una entrada
  \item Otra
  \item ¡Guau! Tres entradas
\end{itemize}

\end{document}
```

1
