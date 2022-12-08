<div id="top"></div>
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
[![Apache License 2.0][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]



<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/dlwhitehurst/bird-life">
    <img src="https://dlwhitehurst.com" alt="Logo" width="80" height="80">
  </a>

<h3 align="center">Bird Life</h3>

  <p align="center">
    This project is used to showcase a Mule4 API implementation related to my birding and photography hobby.
    <br />
    <a href="https://github.com/dlwhitehurst/bird-life/issues">Report Bug</a>
	.
    <a href="https://github.com/dlwhitehurst/bird-life/issues">Request Feature</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
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



<!-- ABOUT THE PROJECT -->
## About The Project
This project stems from a promise to show how to do paging of large collections returned by
the server using REST and implementing using Hypertext as the Engine of Application State or HATEOAS.

<p align="right">(<a href="#top">back to top</a>)</p>



### Built With

* [Mule4.4](https://docs.mulesoft.com/mule-runtime/4.4/intro-mule-message)
* [Anypoint Studio 7.14.0](https://www.mulesoft.com/platform/studio)
* [RAML 1.0](https://raml.org/)

<p align="right">(<a href="#top">back to top</a>)</p>


<!-- GETTING STARTED -->
## Getting Started

These instructions can be used to run this project in AnypointStudio and see the HATEOAS implementation
in operation. Be sure to checkout the code on the main branch as other branches are used as working code
and are not stable.

### Prerequisites
Before you clone and checkout the `main` branch, be sure that you have the following installed.

- [Git](https://git-scm.com/)
- [Anypoint Studio 7+](https://www.mulesoft.com/platform/studio)(preferably version 7.14+)

### Installation
Clone the project locally and then run the API deployment in Anypoint Studio

1. Clone the repo
   ```bash
   git clone https://github.com/dlwhitehurst/bird-life.git
   ```
2. Start AnypointStudio

3. Import the project

4. Run the project as a Mule Application in AnypointStudio

### Make a Request to the Mule Server
There are several ways to interact with the REST API. Mulesoft recommends
the use of ARC Client or [Advanced Rest Client][arc-url]. curl is more cryptic
but easier to show the request in a single statement or command. 

The following curl command will call the GET API resource for `/photos`.

```bash
curl -i http://localhost:8081/api/v1/photos
```

You should get a response something like this.
```
HTTP/1.1 200 OK
Content-Type: application/json; charset=UTF-8
Content-Length: 1561
Date: Thu, 08 Dec 2022 18:48:39 GMT

{
  "data": [
    {
      "id": "123",
      "name": "IMG_3456.CR2",
      "type": "RAW",
      "status": "REVIEWED",
      "created-by": "CAMERA",
      "drive-folder": "2022_09_12",
      "drive-camera": "EOS-6D",
      "drive-name": "PHOTO-1",
      "backup": "false",
      "notes": "Nothing to report"
    },
    {
      "id": "124",
      "name": "YMP_EOS6D_09122022_3456.JPG",
      "type": "JPG",
      "status": "Published/Watermarked",
      "created-by": "ADOBE",
      "drive-folder": "2022_09_12",
      "drive-camera": "EOS-6D",
      "drive-name": "C-WINDOWS",
      "backup": "false",
      "notes": "All processing complete"
    },
    {
      "id": "125",
      "name": "IMG_3457.CR2",
      "type": "RAW",
      "status": "REVIEWED",
      "created-by": "CAMERA",
      "drive-folder": "2022_09_12",
      "drive-camera": "EOS-6D",
      "drive-name": "PHOTO-1",
      "backup": "false",
      "notes": "Nothing to report"
    },
    {
      "id": "126",
      "name": "IMG_3456.CR2",
      "type": "RAW",
      "status": "REVIEWED",
      "created-by": "CAMERA",
      "drive-folder": "2022_09_12",
      "drive-camera": "EOS-6D",
      "drive-name": "PHOTO-1",
      "backup": "false",
      "notes": "Nothing to report"
    }
  ],
  "links": {
    "first": "/api/v1/photos?startItem=1&maxItemCount=4",
    "self": "/api/v1/photos?startItem=1&maxItemCount=4",
    "next": "/api/v1/photos?startItem=5&maxItemCount=4",
    "previous": "/api/v1/photos?startItem=1&maxItemCount=4",
    "last": "/api/v1/photos?startItem=25&maxItemCount=4"
  }
}
```
<p align="right">(<a href="#top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
## Usage

Later

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- ROADMAP -->
## Roadmap

- [] Feature 1
- [] Feature 2
- [] Feature 3
    - [] Nested Feature

See the [open issues](https://github.com/dlwhitehurst/bird-life/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#top">back to top</a>)</p>



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

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- LICENSE -->
## License

Distributed under the Apache 2.0 License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

David L Whitehurst - dlwhitehurst@gmail.com

Project Link: [https://github.com/dlwhitehurst/bird-life](https://github.com/dlwhitehurst/bird-life)

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

* []()
* []()
* []()

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/dlwhitehurst/bird-life.svg?style=for-the-badge
[contributors-url]: https://github.com/dlwhitehurst/bird-life/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/dlwhitehurst/bird-life.svg?style=for-the-badge
[forks-url]: https://github.com/dlwhitehurst/bird-life/network/members
[stars-shield]: https://img.shields.io/github/stars/dlwhitehurst/bird-life.svg?style=for-the-badge
[stars-url]: https://github.com/dlwhitehurst/bird-life/stargazers
[issues-shield]: https://img.shields.io/github/issues/dlwhitehurst/bird-life.svg?style=for-the-badge
[issues-url]: https://github.com/dlwhitehurst/bird-life/issues
[license-shield]: https://img.shields.io/github/license/dlwhitehurst/bird-life.svg?style=for-the-badge
[license-url]: https://github.com/dlwhitehurst/bird-life/blob/main/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/linkedin_username
[product-screenshot]: images/screenshot.png
[arc-url]: https://install.advancedrestclient.com/
