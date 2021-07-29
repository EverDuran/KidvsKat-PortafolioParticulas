<div align="center">
<img src="https://i.ibb.co/jW8RBL5/particulasjs.png" alt="particulasjs" border="0">
</div>
<br>

## **Video del Proyecto** 
[2021🚀 Efecto Partículas en Movimiento! Responsivo [Angular 12 & Librería JS] ](https://youtu.be/xiHmxGZtyKU "Youtube")
<br/>

## HomeParticulas

Este proyecto se generó con [Angular CLI] (https://github.com/angular/angular-cli) versión 12.0.5.


## Servidor de desarrollo

Ejecute `ng serve` para un servidor de desarrollo. Vaya a `http: // localhost: 4200 /`. La aplicación se recargará automáticamente si cambia alguno de los archivos de origen.

### Demostracioó de la aplicación en web:

<div>
<img src="https://i.ibb.co/mhknVgW/2021-07-09-03-53-12-online-video-cutter-com.gif" alt="particulasjs" border="0" width:50%>
</div>
<br>

### Demostración en tablet:

<div>
<img src="https://i.ibb.co/HxLJqff/tablet.gif" alt="tablet" border="0">
</div>
<br>

### Demostración en móvil:

<div>
<img src="https://i.ibb.co/TTYCzWc/movil.gif" alt="movil" border="0">
</div>

## INSTALACION DE NG-PARTICLES EN ANGULAR-12

#### Instalar usando npm
[![anix](https://nodei.co/npm/proton-engine.png)](https://npmjs.org/package/proton-engine)

##### Nota: la versión usada es "ng-particles": "^2.14.1", "tsparticles": "^1.31.1",

```shell
npm install ng-particles tsparticles
```
```yarn
yarn add ng-particles tsparticles
```


#### importar en <b> app.module.ts </b>
```javascript
import { NgParticlesModule } from 'ng-particles';
import { NgModule } from "@angular/core";

@NgModule({
  declarations: [
    /* AppComponent */
  ],
  imports: [
    /* other imports */ NgParticlesModule // NgParticlesModule is required
  ],
  providers: [],
  bootstrap: [ /* AppComponent */ ]
})
export class AppModule { }
```

app.component.ts
 shell
importaciones necesarias  

```javascript

import { Component } from '@angular/core';
import { Container, Main } from 'tsparticles';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss'],
})
export class AppComponent {
  id = 'tsparticles';
  particlesUrl = 'http://foo.bar/particles.json';
  particlesOptions = {
    fpsLimit: 60,
    interactivity: {
      detectsOn: 'canvas',
      events: {
        onClick: {
          enable: true,
          mode: 'push',
        },
        onHover: {
          enable: true,
          mode: 'repulse',
        },
        resize: true,
      },
      modes: {
        bubble: {
          distance: 400,
          duration: 2,
          opacity: 0.8,
          size: 40,
        },
        push: {
          quantity: 4,
        },
        repulse: {
          distance: 200,
          duration: 0.4,
        },
      },
    },
    particles: {
      color: {
        value: '#FFFC00',//
      },
      links: {
        color: '#ffc000',
        distance: 170,
        enable: true,
        opacity: 0.8,
        width: 1,
      },
      collisions: {
        enable: true,
      },
      move: {
        direction: 'none',
        enable: true,
        outMode: 'bounce',
        random: false,
        speed: 4,
        straight: false,
      },
      number: {
        density: {
          enable: true,
          value_area: 800,
        },
        value: 80,
      },
      opacity: {
        value: 0.5,
      },
      shape: {
        type: 'circle',
      },
      size: {
        random: true,
        value: 5,
      },
    },
    detectRetina: true,
  };

  particlesLoaded(container: Container): void {
    console.log(container);
  }

  particlesInit(main: Main): void {
    console.log(main);
  }
}
```

##### template.html

```html
<ng-particles [id]="id" [options]="particlesOptions" (particlesLoaded)="particlesLoaded($event)"
  (particlesInit)="particlesInit($event)"></ng-particles>
```

## Ayuda adicional

Para obtener más ayuda sobre ng-particles visite https://www.npmjs.com/package/ng-particles.
<br>
Pagina de ng-particle https://particles.js.org/
<br>
Ejemplos utlizados con ng-particle https://codepen.io/collection/DPOage

## Redes Sociales
`<YouTube>` : <https://www.youtube.com/channel/UCFPYlFz5afh_o7tVW--htKw>
<br/>
`<Facebook>` : <https://www.facebook.com/kidvskat.code>
