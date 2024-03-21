<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a name="readme-top"></a>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]



<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/othneildrew/Best-README-Template">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">Best-README-Template</h3>

  <p align="center">
    An awesome README template to jumpstart your projects!
    <br />
    <a href="https://github.com/othneildrew/Best-README-Template"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/othneildrew/Best-README-Template">View Demo</a>
    ·
    <a href="https://github.com/othneildrew/Best-README-Template/issues">Report Bug</a>
    ·
    <a href="https://github.com/othneildrew/Best-README-Template/issues">Request Feature</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Índice</summary>
  <ol>
    <li>
      <a href="#Planteamiento del problema">Planteamiento del problema</a>
    </li>
    <li>
      <a href="#Desarrollo">Desarrollo</a>
      <ul>
        <li><a href="#Diseño del logo">Diseño del logo</a></li>
        <li><a href="#c%C3%B3digo-en-rapid">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- Planteamiento del problema -->
## Planteamiento del problema

Las redes sociales figuran en la actualidad como una de las principales formas de dar respuesta a las necesidades de los consumidores. Gigantes tecnológicos que dan cabida a todo tipo de marcas dentro de sus espacios publicitarios como Facebook, Instagram, o incluso Twitter. En el contexto de la asignatura de robótica, y en vista de lo anterior, se escogió a esta última empresa para el diseño de su logotipo en el entorno del laboratorio.

En los siguientes apartados se identifican los aspectos que fueron necesarios para lograr el diseño en simulación y en el robot real, de manera satisfactoria.

<!-- GETTING STARTED -->
## Desarrollo

### Diseño del logo

En primera instancia, según los parámetros definidos en la guía de laboratorio, se realizó en Inventor el característico diseño del logo de Twitter, conformado por la silueta de un monarca nuquinegro. A continuación se observa el diseño realizado.

![Diseño CAD del logo junto a iniciales en el tablero](/Recursos/Workspacev3.png)

### 



![Vista de planta de los elementos dispuestos en la estación ](/Recursos/vistaPlanta.png)

### Código en RAPID

`MoveL`: mueve el robot siguiendo una trayectoria lineal  
`MoveJ`: mueve el robot mediante un movimiento de ejes  
`MoveC`: mueve el robot en una trayectoria circular 

```rapid
MODULE Module1
    PERS tooldata THerramienta:=[TRUE,[[84.853,0,134.853],[0.923879533,0,0.382683432,0]],[0.1,[23.11,0,61.258],[1,0,0,0],0,0,0]];
    TASK PERS wobjdata Workobject_1:=[FALSE,TRUE,"",[[0,0,10],[1,0,0,0]],[[409.583,-9.692,240],[0,1,0,0]]];
    CONST robtarget Target_MM:=[[290.713816879,-34.485338984,-399.373982496],[0.041038912,0.230927375,0.344436207,0.909039083],[0,-1,0,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_HH:=[[169.853003696,-95,-377.146975726],[0,0.382683414,0,0.92387954],[0,0,0,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_5:=[[172.146,169.721,-50],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_10:=[[172.146,169.721,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_15:=[[94.179,126.363,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_20:=[[95.464,37.16,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_25:=[[97.319,60.55,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_30:=[[108.141,81.369,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_35:=[[114.101,64.13,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_40:=[[128.91,53.479,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_45:=[[128.569,60.297,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_50:=[[129.686,67.033,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_55:=[[140.077,49.513,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_60:=[[159.408,43.089,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_65:=[[156.802,49.64,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_70:=[[156.139,56.659,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_75:=[[174.493,43.802,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_80:=[[196.643,47.198,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_85:=[[173.907,75.001,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_90:=[[164.745,109.728,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_95:=[[198.416,125.037,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_100:=[[192.364,161.526,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_105:=[[195.069,171.202,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_110:=[[199.539,180.201,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_115:=[[190.171,175.306,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_120:=[[183.068,167.479,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_125:=[[184.555,176.204,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_130:=[[187.549,184.533,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_135:=[[179.202,177.798,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_138:=[[200,225,-50],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_140:=[[200,225,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_150:=[[200,240,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_155:=[[150,290,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_160:=[[100,240,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_170:=[[100,225,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_175:=[[105,392.992,-50],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_180:=[[105,392.992,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_185:=[[150,321.197,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_190:=[[195,392.992,0],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    CONST robtarget Target_195:=[[195,392.992,-50],[0,0,0,1],[-1,0,-1,0],[9E+09,9E+09,9E+09,9E+09,9E+09,9E+09]];
    PROC main()
        Reset DO_01;
        Reset DO_02;
        WHILE TRUE DO
            IF DI_01=1 THEN
                Set DO_01;
                Twitter;
                Reset DO_01;
            ENDIF
            IF DI_02=1 THEN
                Set DO_02;
                Path_40;
                Reset DO_02;
            ENDIF
        ENDWHILE
    ENDPROC
    PROC Path_40()
        MoveJ Target_MM,v600,z0,THerramienta\WObj:=Workobject_1;
    ENDPROC
    PROC Twitter()
        MoveJ Target_HH,v600,z0,THerramienta\WObj:=Workobject_1;
        MoveJ Target_5,v600,z5,THerramienta\WObj:=Workobject_1;
        MoveL Target_10,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_15,Target_20,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_25,Target_30,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_35,Target_40,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_45,Target_50,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_55,Target_60,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_65,Target_70,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_75,Target_80,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_85,Target_90,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_95,Target_100,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_105,Target_110,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_115,Target_120,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_125,Target_130,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_135,Target_10,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveL Target_5,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveL Target_138,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveL Target_140,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveL Target_150,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_155,Target_160,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveL Target_170,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveL Target_140,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveL Target_138,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveL Target_175,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveL Target_180,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveC Target_185,Target_190,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveL Target_195,v200,z0,THerramienta\WObj:=Workobject_1;
        MoveJ Target_HH,v600,z0,THerramienta\WObj:=Workobject_1;
    ENDPROC
ENDMODULE
```
## Resultados

### Robot en funcionamiento - Robot Studio

<iframe width="500" height="281" src="https://www.youtube.com/embed/8ak_B7RKMWM" title="PruebaTwitter" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

<iframe width="320" height="180" src="https://www.youtube-nocookie.com/embed/FEa2diI2qgA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen="1"></iframe>



<iframe width="840" height="473" src="https://www.youtube.com/embed/IRyxWnemi_k" title="RSLab1" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### Robot en funcionamiento - Entorno de laboratorio


<!-- USAGE EXAMPLES -->
## Usage

Use this space to show useful examples of how a project can be used. Additional screenshots, code examples and demos work well in this space. You may also link to more resources.

_For more examples, please refer to the [Documentation](https://example.com)_

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ROADMAP -->
## Roadmap

- [x] Add Changelog
- [x] Add back to top links
- [ ] Add Additional Templates w/ Examples
- [ ] Add "components" document to easily copy & paste sections of the readme
- [ ] Multi-language Support
    - [ ] Chinese
    - [ ] Spanish

See the [open issues](https://github.com/othneildrew/Best-README-Template/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

Your Name - [@your_twitter](https://twitter.com/your_username) - email@example.com

Project Link: [https://github.com/your_username/repo_name](https://github.com/your_username/repo_name)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

Use this space to list resources you find helpful and would like to give credit to. I've included a few of my favorites to kick things off!

* [Choose an Open Source License](https://choosealicense.com)
* [GitHub Emoji Cheat Sheet](https://www.webpagefx.com/tools/emoji-cheat-sheet)
* [Malven's Flexbox Cheatsheet](https://flexbox.malven.co/)
* [Malven's Grid Cheatsheet](https://grid.malven.co/)
* [Img Shields](https://shields.io)
* [GitHub Pages](https://pages.github.com)
* [Font Awesome](https://fontawesome.com)
* [React Icons](https://react-icons.github.io/react-icons/search)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=for-the-badge
[contributors-url]: https://github.com/othneildrew/Best-README-Template/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/othneildrew/Best-README-Template.svg?style=for-the-badge
[forks-url]: https://github.com/othneildrew/Best-README-Template/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=for-the-badge
[stars-url]: https://github.com/othneildrew/Best-README-Template/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=for-the-badge
[issues-url]: https://github.com/othneildrew/Best-README-Template/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://github.com/othneildrew/Best-README-Template/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/othneildrew
[product-screenshot]: images/screenshot.png
[Next.js]: https://img.shields.io/badge/next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white
[Next-url]: https://nextjs.org/
[React.js]: https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB
[React-url]: https://reactjs.org/
[Vue.js]: https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D
[Vue-url]: https://vuejs.org/
[Angular.io]: https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white
[Angular-url]: https://angular.io/
[Svelte.dev]: https://img.shields.io/badge/Svelte-4A4A55?style=for-the-badge&logo=svelte&logoColor=FF3E00
[Svelte-url]: https://svelte.dev/
[Laravel.com]: https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white
[Laravel-url]: https://laravel.com
[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com
[JQuery.com]: https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white
[JQuery-url]: https://jquery.com 
