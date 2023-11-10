# .

This template should help get you started developing with Vue 3 in Vite.

## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).

## Customize configuration

See [Vite Configuration Reference](https://vitejs.dev/config/).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```


# Assingment

- Descrizione:
    - Create un nuovo progetto utilizzando Vite e Vue 3 e definite i componenti necessari per strutturare il layout come da screenshot allegato.
    - Quando la struttura a macroblocchi è pronta, popolate le voci di menu dinamicamente usando i data del componente.
    - Per oggi diamo priorità alla struttura: quando è tutto bello solido, passiamo al Sass!
    - Font: Open Sans Condensed per titolo e Open Sans per il resto

- Bonus:
Creare un componente aggiuntivo per gestire la fascia azzurra con le icone.


# attenzione

dato che le immagini forniteci provenivano da un file di tipo json e non da un dato js, al posto di usare il tipico approccio

``` js
const data
data = ...
export {data}
```
``` vue
import {data} from 'path'
```
ho preferito  mantenere il formato json e importare il tutto tramite la libreria di axios, quindi

``` vue
import axios from 'axios'
....
export default {
    ....
    methods: {
        fetchData() {
            axios
                .get('../src/components/data/dc-comics.json')
                .then(response => {
                    this.importedFiles = response.data
                    console.log(this.importedFiles)
                })
        },
        
    },
    mounted() {
        this.fetchData()
    }
}
```