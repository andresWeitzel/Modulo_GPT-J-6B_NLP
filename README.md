![Index app](https://github.com/andresWeitzel/Modulo_GPT-J_NLP_NodeJs/blob/master/doc/assets/img/brain.jpg)

<div align="right">
  <img width="27" height="27" src="./doc/assets/icons/devops/png/postman.png" />
  <img width="29" height="27" src="./doc/assets/icons/devops/png/git.png" />
  <img width="27" height="27" src="./doc/assets/icons/backend/javascript-typescript/png/nodejs.png" />
  <img width="27" height="27" src="./doc/assets/icons/artificial-intelligence/png/ia-bot.png" />
  <img width="27" height="27" src="./doc/assets/icons/artificial-intelligence/png/ia-robot.png" />
  <img width="27" height="27" src="./doc/assets/icons/artificial-intelligence/png/ia-human.png" />
</div>

<br>

<div align="right">
    <a href="./translation/README.es.md" target="_blank">
      <img src="./doc/assets/icons/translation/arg-flag.jpg" width="10%" height="10%" />
  </a> 
   <a href="./README.md" target="_blank">
      <img src="./doc/assets/icons/translation/eeuu-flag.jpg" width="10%" height="10%" />
  </a>
</div>

<br>

<div align="center">

# GPT-J-6B_NLP_Module ![(status-completed)](./doc/assets/icons/badges/status-completed.svg)

</div>  

Open source module for Natural Language Processing based on GPT-J-6B, a language model developed by EleutherAI as an alternative to GPT-3. It allows generating text, translating, answering questions and completing code through the Banana.dev API.

*   [GPT-J-6B Guide](https://huggingface-co.translate.goog/EleutherAI/gpt-j-6b?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=tc)
*   [NPM package gpt-j](https://www.npmjs.com/package/gpt-j)
*   [Playlist functionality test](https://www.youtube.com/watch?v=GddMV140leA&list=PLCl11UFjHurDYl5a2CQOkrMx4HWamPuZI) <a href="https://www.youtube.com/watch?v=GddMV140leA&list=PLCl11UFjHurDYl5a2CQOkrMx4HWamPuZI" target="_blank"> <img src="./doc/assets/icons/social-networks/yt.png" width="5%" height="5%" /> </a>



<br>

## Index 📜

<details>
 <summary> See </summary>

 <br>

### Section 1) Description, configuration and technologies.

*   [1.0) Project description.](#10-project-description-)
*   [1.1) Project status.](#11-project-status-)
*   [1.2) Technologies used.](#12-technologies-used-)
*   [1.3) Required dependencies.](#13-required-dependencies-)

### Section 2) Project execution and testing

*   [2.0) Project setup.](#20-project-setup-)
*   [2.1) NPM package execution.](#21-npm-package-execution-)
*   [2.2) Environment variables.](#22-environment-variables-)

### Section 3) Documentation and resources

*   [3.0) GPT-J documentation.](#30-gpt-j-documentation-)
*   [3.1) Video tutorials.](#31-video-tutorials-)
*   [3.2) References.](#32-references-)

<br>

</details>

<br>



## Section 1) Description, configuration and technologies.

### 1.0) Project description.

<details>
<summary>See</summary>

<br>

Open source Natural Language Processing module. GPT-J-6B is a 6 billion parameter language model trained using Mesh Transformer JAX. It was developed by EleutherAI as an open source alternative to GPT-3. The model can perform tasks such as text generation, translation, answering questions and code completion. This module provides a simple interface to interact with GPT-J-6B through the Banana.dev API.

<br>

</details>

### 1.1) Project status.

<details>
<summary>See</summary>

<br>

![(status-completed)](./doc/assets/icons/badges/status-completed.svg)

<br>

</details>

### 1.2) Technologies used.

<details>
<summary>See</summary>

<br>

- **Node.js** - JavaScript Runtime
- **Banana.dev API** - AI model inference service
- **GPT-J-6B** - 6 billion parameter language model
- **NPM** - Package manager

<br>

</details>

### 1.3) Required dependencies.

<details>
<summary>See</summary>

<br>

```json
{
  "@banana-dev/banana-dev": "3.0.0"
}
```

<br>

</details>

<br>

## Section 2) Project execution and testing.

### 2.0) Project setup.

<details>
<summary>See</summary>

<br>

#### Project cloning

```bash
git clone https://github.com/andresWeitzel/Api_GPT-J_NLP_NodeJs
cd Modulo_GPT-J-6B_NLP_NodeJs
```

#### Dependencies installation

```bash
npm install @banana-dev/banana-dev@3.0.0
```

<br>

</details>

### 2.1) NPM package execution.

<details>
<summary>See</summary>

<br>

#### NPM package installation

```bash
npm i gpt-j
```

#### Basic usage

```js
const modelRunner = require('gpt-j');
const apiKey = 'XXXX'
const modelKey = 'gptj'

modelRunner.run('hello', apiKey, modelKey);
```

<br>

</details>

### 2.2) Environment variables.

<details>
<summary>See</summary>

<br>

#### Environment variables configuration

Create `config.js` file:

```js
module.exports = {
    API_KEY: process.env.API_KEY || "xxxx",
    MODEL_KEY: process.env.MODEL_KEY || "gptj"
}
```

#### Implementation with environment variables

```js
const config = require('config.js');
const modelRunner = require('gpt-j');

//keys
const apiKey = config.API_KEY;
const modelKey = config.MODEL_KEY;

modelRunner.run('hello', apiKey, modelKey);
```

**IMPORTANT**: Create a `.gitignore` file to exclude the `config.js` file

<br>

</details>

<br>

## Section 3) Documentation and resources.

### 3.0) GPT-J documentation.

<details>
<summary>See</summary>

<br>

#### Model Parameters

##### Input (text param)
Corresponds to the input layer that the model will analyze (Ex: `generate two functions in javascript`)

##### Text Length (length param)
The output text length is measured in tokens, these are common character sequences that are found through the model core. The higher the number, the more text and information we will get in the output.

##### Temperature Adjustment (temperature param)
Temperature determines the exhaustiveness of the generative model.
- Setting low temperature values leads to a safer model.
- Setting high temperature values leads to a more unstable model.

##### Batch Size (batchSize param)
Implemented for GPU performance.

##### Parameters Example

```js
{
    "text": "i want to know the current temperature",
    "length": 250,
    "temperature": 0.9,
    "batchSize": 1
}
```

#### Model Layer Model Parameters implemented (Setup)

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

#### Model Layer Runner implemented (Execution)

**Input**: `I want to know the current temperature in Buenos Aires, Argentina`

```js
//Imports
const gptCore = require('@banana-dev/banana-dev');
const config = require('../configs/config.js');
const modelParameters = require('../models/modelParameters');

//keys
const apiKey = config.API_KEY;
const modelKey = config.MODEL_KEY;

//Params
let text = "I want to know the current temperature in Buenos Aires, Argentina"
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

#### GPT-J Core Output (Response)

```terminal
{
    message: 'success',
    created: 1668961622,
    apiVersion: '26 Nov 2021',
    modelOutputs: [
        {
            output: '\n' +
                '\n' +
                'Buenos Aires has a very high temperature in summer. If you are a person who lives in Argentina and would like to know what the heat rate is in Buenos Aires, I present my method to know the current temperature in Buenos Aires.\n' +
                '\n' +
                'You don\'t need a GPS to know the current temperature\n' +
                '\n' +
                'Yes, it\'s true, you can know the current temperature at any point in the city in a few seconds. All the information you need is in the following tables.\n' +
                '\n' +
                'To know the current temperature in Buenos Aires, you need to know the temperature of the city area where you are now. If you are in the city, the heat rate in Buenos Aires is quite similar. However, if you are at a point in the city outside the center, the temperature will be higher.\n' +
                '\n' +
                'To know the temperature of the area where you are now, you simply need to know your location point. For example, if you are in the city of Buenos Aires, then you need to know your location point to know the temperature of Buenos Aires.\n' +  
                '\n' +
                'To know your location point, you don\'t need a GPS. You just need to know your address and your speed. The address and speed are the two coordinates of your position.',
            input: 'I want to know the current temperature in Buenos Aires, Argentina'
        }
    ],
    callID: 'call_4a3b9440-fcb6-4122-b269-6ac55a46c3eb'
}
```

<br>

</details>

### 3.1) Video tutorials.

<details>
<summary>See</summary>

<br>

#### [Watch Functional test playlist](https://www.youtube.com/watch?v=GddMV140leA&list=PLCl11UFjHurDYl5a2CQOkrMx4HWamPuZI)

  <a href="https://www.youtube.com/watch?v=GddMV140leA&list=PLCl11UFjHurDYl5a2CQOkrMx4HWamPuZI">
    <img src="./doc/assets/img/yt_playlist.png" />
  </a> 

<br>

<br>

</details>

### 3.2) References.

<details>
<summary>See</summary>

<br>

#### GPT-J-6B Core API
* [Base Example](https://www.banana.dev/pretrained-models/nodejs/gptj)
* [Generate Api Key](https://app.banana.dev/)
* [Models](https://www.banana.dev/pretrained-models/nodejs)
* [Banana API Documentation](https://docs.banana.dev/)
* [Pricing and Plans](https://www.banana.dev/pricing)

#### Core Original GTP-J-6B (Mesh Transformer JAX)
* (The Core with the unoptimized model weighs 6gb. With the Optimized Model 61gb).
* [Repository](https://github.com/kingoflolz/mesh-transformer-jax/#mesh-transformer-jax)
* [Original Paper](https://arxiv.org/abs/2104.04473)
* [Blog EleutherAI](https://blog.eleuther.ai/gpt-j-6b/)
* [Model on HuggingFace](https://huggingface.co/EleutherAI/gpt-j-6B)

#### Additional documentation
* [GPT-J-6B Guide](https://huggingface-co.translate.goog/EleutherAI/gpt-j-6b?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=tc)
* [NPM package gpt-j](https://www.npmjs.com/package/gpt-j)
* [Implementation Tutorial](https://www.youtube.com/watch?v=jlogLBkPZ2A)
* [Comparison with other models](https://www.eleuther.ai/artifacts/gpt-j-6b)
* [JAX Documentation](https://jax.readthedocs.io/)
* [Mesh Transformer JAX Wiki](https://github.com/kingoflolz/mesh-transformer-jax/wiki)

<br>

</details>
