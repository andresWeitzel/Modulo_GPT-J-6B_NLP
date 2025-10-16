![Index app](https://github.com/andresWeitzel/Modulo_GPT-J_NLP_NodeJs/blob/master/doc/assets/img/brain.jpg)

<div align="right">
  <img width="27" height="27" src="../doc/assets/icons/devops/png/postman.png" />
  <img width="29" height="27" src="../doc/assets/icons/devops/png/git.png" />
  <img width="27" height="27" src="../doc/assets/icons/backend/javascript-typescript/png/nodejs.png" />
  <img width="27" height="27" src="../doc/assets/icons/artificial-intelligence/png/ia-bot.png" />
  <img width="27" height="27" src="../doc/assets/icons/artificial-intelligence/png/ia-robot.png" />
  <img width="27" height="27" src="../doc/assets/icons/artificial-intelligence/png/ia-human.png" />
</div>

<br>

<div align="right">
    <a href="./README.es.md" target="_blank">
      <img src="../doc/assets/icons/translation/arg-flag.jpg" width="10%" height="10%" />
  </a> 
   <a href="../README.md" target="_blank">
      <img src="../doc/assets/icons/translation/eeuu-flag.jpg" width="10%" height="10%" />
  </a>
</div>

<br>

<div align="center">

# Módulo_GPT-J-6B_NLP ![(status-completed)](../doc/assets/icons/badges/status-completed.svg)

</div>  

Módulo de código abierto para el Procesamiento de Lenguaje Natural basado en GPT-J-6B, un modelo de lenguaje desarrollado por EleutherAI como alternativa a GPT-3. Permite generar texto, traducir, responder preguntas y completar código a través de la API de Banana.dev.

*   [Guía GPT-J-6B](https://huggingface-co.translate.goog/EleutherAI/gpt-j-6b?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=tc)
*   [Paquete npm gpt-j](https://www.npmjs.com/package/gpt-j)
*   [Lista de reproducción de pruebas funcionales](https://www.youtube.com/watch?v=GddMV140leA&list=PLCl11UFjHurDYl5a2CQOkrMx4HWamPuZI) <a href="https://www.youtube.com/watch?v=GddMV140leA&list=PLCl11UFjHurDYl5a2CQOkrMx4HWamPuZI" target="_blank"> <img src="../doc/assets/icons/social-networks/yt.png" width="5%" height="5%" /> </a>



<br>

## Índice 📜

<details>
 <summary> Ver </summary>

 <br>

### Sección 1) Descripción, configuración y tecnologías.

*   [1.0) Descripción del proyecto.](#10-descripción-del-proyecto-)
*   [1.1) Estado del proyecto.](#11-estado-del-proyecto-)
*   [1.2) Tecnologías utilizadas.](#12-tecnologías-utilizadas-)
*   [1.3) Dependencias requeridas.](#13-dependencias-requeridas-)

### Sección 2) Ejecución y pruebas del proyecto

*   [2.0) Configuración del proyecto.](#20-configuración-del-proyecto-)
*   [2.1) Ejecución del paquete NPM.](#21-ejecución-del-paquete-npm-)
*   [2.2) Variables de entorno.](#22-variables-de-entorno-)

### Sección 3) Documentación y recursos

*   [3.0) Documentación GPT-J.](#30-documentación-gpt-j-)
*   [3.1) Tutoriales en video.](#31-tutoriales-en-video-)
*   [3.2) Referencias.](#32-referencias-)

<br>

</details>

<br>



## Sección 1) Descripción, configuración y tecnologías.

### 1.0) Descripción del proyecto.

<details>
<summary>Ver</summary>

<br>

Módulo de código abierto para el Procesamiento de Lenguaje Natural. GPT-J-6B es un modelo de lenguaje de 6 mil millones de parámetros entrenado usando Mesh Transformer JAX. Fue desarrollado por EleutherAI como una alternativa de código abierto a GPT-3. El modelo puede realizar tareas como generación de texto, traducción, responder preguntas y completar código. Este módulo proporciona una interfaz sencilla para interactuar con GPT-J-6B a través de la API de Banana.dev.

<br>

</details>

### 1.1) Estado del proyecto.

<details>
<summary>Ver</summary>

<br>

![(status-completed)](../doc/assets/icons/badges/status-completed.svg)

<br>

</details>

### 1.2) Tecnologías utilizadas.

<details>
<summary>Ver</summary>

<br>

- **Node.js** - Runtime de JavaScript
- **Banana.dev API** - Servicio de inferencia de modelos de IA
- **GPT-J-6B** - Modelo de lenguaje de 6 mil millones de parámetros
- **NPM** - Gestor de paquetes

<br>

</details>

### 1.3) Dependencias requeridas.

<details>
<summary>Ver</summary>

<br>

```json
{
  "@banana-dev/banana-dev": "3.0.0"
}
```

<br>

</details>

<br>

## Sección 2) Ejecución y pruebas del proyecto.

### 2.0) Configuración del proyecto.

<details>
<summary>Ver</summary>

<br>

#### Clonación del proyecto

```bash
git clone https://github.com/andresWeitzel/Api_GPT-J_NLP_NodeJs
cd Modulo_GPT-J-6B_NLP_NodeJs
```

#### Instalación de dependencias

```bash
npm install @banana-dev/banana-dev@3.0.0
```

<br>

</details>

### 2.1) Ejecución del paquete NPM.

<details>
<summary>Ver</summary>

<br>

#### Instalación del paquete NPM

```bash
npm i gpt-j
```

#### Uso básico

```js
const modelRunner = require('gpt-j');
const apiKey = 'XXXX'
const modelKey = 'gptj'

modelRunner.run('hola', apiKey, modelKey);
```

<br>

</details>

### 2.2) Variables de entorno.

<details>
<summary>Ver</summary>

<br>

#### Configuración de variables de entorno

Crear archivo `config.js`:

```js
module.exports = {
    API_KEY: process.env.API_KEY || "xxxx",
    MODEL_KEY: process.env.MODEL_KEY || "gptj"
}
```

#### Implementación con variables de entorno

```js
const config = require('config.js');
const modelRunner = require('gpt-j');

//claves
const apiKey = config.API_KEY;
const modelKey = config.MODEL_KEY;

modelRunner.run('hola', apiKey, modelKey);
```

**IMPORTANTE**: Crear un archivo `.gitignore` para excluir el archivo `config.js`

<br>

</details>

<br>

## Sección 3) Documentación y recursos.

### 3.0) Documentación GPT-J.

<details>
<summary>Ver</summary>

<br>

#### Parámetros del Modelo

##### Entrada (parámetro text)
Corresponde a la capa de entrada que el modelo analizará (Ej: `generar dos funciones en javascript`)

##### Longitud del texto (parámetro length)
La longitud del texto de salida se mide en tokens, estos son secuencias de caracteres comunes, que se encuentran a través del núcleo del modelo. Cuanto mayor sea el número, mayor texto e información obtendremos en la salida.

##### Ajuste de Temperatura (parámetro temperature)
La temperatura determina la exhaustividad del modelo generativo.
- Establecer valores de temperatura bajos conlleva a un modelo más seguro.
- Establecer valores de temperatura altos conlleva a un modelo más inestable.

##### Tamaño del Lote (parámetro batchSize)
Se implementa para rendimiento de GPU.

##### Ejemplo de Parámetros

```js
{
    "text": "quiero saber la temperatura actual",
    "length": 250,
    "temperature": 0.9,
    "batchSize": 1
}
```

#### Modelo de Capa Parámetros del Modelo implementado (Configuración)

```js
module.exports.set = (text, length, temp, batch) => {
    const params = {
        "text": text,
        "length": length,
        "temperature": temp,
        "batchSize": batch
    }
    return params;
}
```

#### Modelo de Capa Ejecutor implementado (Ejecución)

**Entrada**: `Quiero saber la temperatura actual en Buenos Aires, Argentina`

```js
//Importaciones
const gptCore = require('@banana-dev/banana-dev');
const config = require('../configs/config.js');
const modelParameters = require('../models/modelParameters');

//claves
const apiKey = config.API_KEY;
const modelKey = config.MODEL_KEY;

//Parámetros
let text = "Quiero saber la temperatura actual en Buenos Aires, Argentina"
let length = 400
let temperature = 0.7
let batchSize = 1

let params = modelParameters.set(text, length, temperature, batchSize);

let run = async (params) => {
    try {
        var out = await gptCore.run(apiKey, modelKey, params)
        console.log(out)
        return out
    } catch (error) {
        console.log(error);
    }
}

run(params)
```

#### Salida del Núcleo GPT-J (Respuesta)

```terminal
{
    message: 'success',
    created: 1668961622,
    apiVersion: '26 Nov 2021',
    modelOutputs: [
        {
            output: '\n' +
                '\n' +
                'Buenos Aires tiene una temperatura muy alta en el verano. Si eres una persona que vive en la Argentina y te gustaría saber cuál es el ritmo de calor que tienes en Buenos Aires, te presento mi método para saber la temperatura actual en Buenos Aires.\n' +
                '\n' +
                'No necesitas un GPS para saber la temperatura actual\n' +
                '\n' +
                'Sí, es cierto, puedes conocer la temperatura actual en cualquier punto de la ciudad en pocos segundos. Toda la información que necesitas está en las siguientes tablas.\n' +
                '\n' +
                'Para saber la temperatura actual en Buenos Aires, necesitas saber la temperatura de la zona de la ciudad donde estás ahora. Si eres en la ciudad, el ritmo de calor en Buenos Aires es bastante similar. Sin embargo, si eres en un punto de la ciudad fuera del centro, la temperatura será más alta.\n' +
                '\n' +
                'Para saber la temperatura de la zona donde estás ahora, simplemente debes saber tu punto de ubicación. Por ejemplo, si eres en la ciudad de Buenos Aires, entonces debes saber tu punto de ubicación para saber la temperatura de Buenos Aires.\n' +  
                '\n' +
                'Para saber tu punto de ubicación, no necesitas un GPS. Sólo necesitas saber tu dirección y tu velocidad. La dirección y la velocidad son las dos coordenadas de tu posición.',
            input: 'Quiero saber la temperatura actual en Buenos Aires, Argentina'
        }
    ],
    callID: 'call_4a3b9440-fcb6-4122-b269-6ac55a46c3eb'
}
```

<br>

</details>

### 3.1) Tutoriales en video.

<details>
<summary>Ver</summary>

<br>

#### [Ver Lista de reproducción de pruebas funcionales](https://www.youtube.com/watch?v=GddMV140leA&list=PLCl11UFjHurDYl5a2CQOkrMx4HWamPuZI)

  <a href="https://www.youtube.com/watch?v=GddMV140leA&list=PLCl11UFjHurDYl5a2CQOkrMx4HWamPuZI">
    <img src="../doc/assets/img/yt_playlist.png" />
  </a> 

<br>

<br>

</details>

### 3.2) Referencias.

<details>
<summary>Ver</summary>

<br>

#### API del Núcleo GPT-J-6B
* [Ejemplo Base](https://www.banana.dev/pretrained-models/nodejs/gptj)
* [Generar Clave API](https://app.banana.dev/)
* [Modelos](https://www.banana.dev/pretrained-models/nodejs)
* [Documentación API Banana](https://docs.banana.dev/)
* [Precios y Planes](https://www.banana.dev/pricing)

#### Núcleo Original GTP-J-6B (Mesh Transformer JAX)
* (El Núcleo con el modelo no optimizado pesa 6gb. Con el Modelo Optimizado 61gb).
* [Repositorio](https://github.com/kingoflolz/mesh-transformer-jax/#mesh-transformer-jax)
* [Artículo Original](https://arxiv.org/abs/2104.04473)
* [Blog EleutherAI](https://blog.eleuther.ai/gpt-j-6b/)
* [Modelo en HuggingFace](https://huggingface.co/EleutherAI/gpt-j-6B)

#### Documentación adicional
* [Guía GPT-J-6B](https://huggingface-co.translate.goog/EleutherAI/gpt-j-6b?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=tc)
* [Paquete npm gpt-j](https://www.npmjs.com/package/gpt-j)
* [Tutorial de Implementación](https://www.youtube.com/watch?v=jlogLBkPZ2A)
* [Comparación con otros modelos](https://www.eleuther.ai/artifacts/gpt-j-6b)
* [Documentación JAX](https://jax.readthedocs.io/)
* [Wiki Mesh Transformer JAX](https://github.com/kingoflolz/mesh-transformer-jax/wiki)

<br>

</details>
