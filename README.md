[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/aknjoroge/Three.js-setup.git">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">Three.Js startup setup </h3>

  <p align="center">
  `Three.js`
  </p>
</p>

<!-- ABOUT THE PROJECT -->

## About The Project

[![Product Name Screen Shot][product-screenshot]](https://github.com/aknjoroge/Three.js-setup.git)

This is a project startup for three.js, the projects implements orbit controls and basic materials

<br/>

---

## Getting Started

The library is imported in the html from the node_modules folder <br/>
`<script defer src="node_modules/three/build/three.min.js"></script>`
<br/>
The library can also be imported from three js CDN as ` import * as THREE from 'https://cdn.skypack.dev/three@<version>';`.
<br/>
Get better installation guides from [three.js installation docs](https://threejs.org/docs/#manual/en/introduction/Installation).
<br/>

The scripts have the attribute `defer` since they are places in the html header not the footer

I also import Orbit controlls that allows the camera to orbit around a target.<br/>

```html
<script
  defer
  src="node_modules/three/examples/js/controls/OrbitControls.js"
></script>
```

I assign a class to a html element which i use to render the three.js scene ` <div class="webgl"></div>`

### Library

Three.js setup requires :

1. Scene = `javascript let scene = new THREE.Scene();`

2. Camera = `javascript let camera = new THREE.PerspectiveCamera()`

3. Renderer = `javascript let renderer = new THREE.WebGLRenderer();`

An object is then initialized using a :

1. Geometry = `javascript let geometry = new THREE.BoxGeometry();`

2. Material = `javascript let material = new THREE.MeshBasicMaterial(); `

> Mesh basic material is not affected by lighting

Orbit controlls are initialzed using the camera object and renderer Dom element

` let controls = new THREE.OrbitControls(camera, renderer.domElement);`

<br/>

` controls.enableZoom = true;` used to activate or deactivate the zooming functionality of the controls

<br/>

`requestAnimationFrame()` is used to update the scene rendering on camera change

## Usage

clone the repo and start your 3D world project

<!-- ROADMAP -->

## Roadmap

View [Three js documentation](https://threejs.org/docs) for more understanding

## License

Distributed under the MIT License. See `LICENSE` for more information.

<!-- CONTACT -->

## Contact

Alexander Karanja - [@Twitter](https://twitter.com/aknjoroge) - info@techkey.co.ke

[license-url]: https://opensource.org/licenses/MIT

<br/>

[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/aknjoroge/
[product-screenshot]: images/screenshot.png
