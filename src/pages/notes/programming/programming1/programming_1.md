---
title: "Database Installation Guide"
---

<!-- | header | header | header |
| ------ | :----: | -----: |
| a      |   b    |      c |
| 1      |   2    |      3 |
| foo    |  bar   |    baz | -->

<!-- | header | header | header |
| ------ | :----: | -----: |
| #1     |   b    |      c |
| 1      |   2    |      3 |
| foo    |  bar   |    baz | -->

<br>

# Introduction

<div class="separator"></div>

##### (Published on March 22, 2025)

<br>

In this article, we will walk through the my extension that help me a lot in written code more efficiency.

<!-- <div class="credentials-box">
    <div class="hierarchy-list">

- Two Server linux

  - Database Master
  - Database Slave

- Internet Connection for download

    </div>

</div> -->

<!-- ![db_replication3](/image/db_replication3.png) -->

<br>
<br>

<!-- [**laravel**](https://formulahendry.gallerycdn.vsassets.io/extensions/formulahendry/auto-close-tag/0.5.15/1702959502562/Microsoft.VisualStudio.Services.Icons.Default) -->

<!-- ![GitHub Logo](https://formulahendry.gallerycdn.vsassets.io/extensions/formulahendry/auto-close-tag/0.5.15/1702959502562/Microsoft.VisualStudio.Services.Icons.Default) -->

# VS CODE Extension

<div class="separator"></div>

<br>

<div class="table-container">
    <table>
        <thead>
            <tr>
                <th>No</th>
                <th>Tips</th>
                <th>Description</th>
                <!-- <th class="text-center">Status</th> -->
            </tr>
        </thead>
        <tbody>
            <tr>
                <td class="highlight">#1</td>
                <td>
                <img class="icon"  alt="Auto Close Tag" src="https://formulahendry.gallerycdn.vsassets.io/extensions/formulahendry/auto-close-tag/0.5.15/1702959502562/Microsoft.VisualStudio.Services.Icons.Default" >
                </td>
                <td>
                  Auto Close Tag
                        <br>
                        (Jun Han)
                </td>
                <!-- <td class="text-center status-active">Active</td> -->
            </tr>
            <tr>
                <td class="highlight">#2</td>
                <td>
                <img class="icon"  alt="Auto Close Tag" src="https://formulahendry.gallerycdn.vsassets.io/extensions/formulahendry/auto-rename-tag/0.1.10/1644319230173/Microsoft.VisualStudio.Services.Icons.Default" >
                    </td>
                </td>
                <td>
                Auto Rename Tag
                        <br>
                        (Jun Han)
                </td>
                <!-- <td class="text-center status-inactive">On Leave</td> -->
            </tr>
            <tr>
                <td class="highlight">#3</td>
                <td>
                <img class="icon"  alt="Auto Close Tag" src="https://eamodio.gallerycdn.vsassets.io/extensions/eamodio/gitlens/2024.12.2404/1735031340469/Microsoft.VisualStudio.Services.Icons.Default" >
                    </td>
                </td>
                <td>
                 GitLens
                        <br>
                        (GitKraken)
                </td>
                <!-- <td class="text-center status-inactive">On Leave</td> -->
            </tr>
            <tr>
                <td class="highlight">#4</td>
                <td>
                <img class="icon"  alt="Auto Close Tag" src="https://ecmel.gallerycdn.vsassets.io/extensions/ecmel/vscode-html-css/2.0.11/1730921970372/Microsoft.VisualStudio.Services.Icons.Default" >
                    </td>
                </td>
                <td>
                 HTML CSS Support
                        <br>
                        (Ecmel)
                </td>
                <!-- <td class="text-center status-inactive">On Leave</td> -->
            </tr>
            <tr>
                <td class="highlight">#5</td>
                <td>
             <img class="icon"  alt="Auto Close Tag" src="https://shufo.gallerycdn.vsassets.io/extensions/shufo/vscode-blade-formatter/0.24.4/1734887442034/Microsoft.VisualStudio.Services.Icons.Default" >
                    </td>
                </td>
                <td>
                  Laravel blade formatter
                        <br>
                        (Shuhei Hayashibara)
                </td>
                <!-- <td class="text-center status-inactive">On Leave</td> -->
            </tr>
            <tr>
                <td class="highlight">#6</td>
                <td>
             <img class="icon"  alt="Auto Close Tag" src="https://onecentlin.gallerycdn.vsassets.io/extensions/onecentlin/laravel5-snippets/1.18.0/1710409025279/Microsoft.VisualStudio.Services.Icons.Default" >
                    </td>
                </td>
                <td>
                  Laravel Snippet
                        <br>
                        (Winnie Lin)
                </td>
                <!-- <td class="text-center status-inactive">On Leave</td> -->
            </tr>
            <tr>
                <td class="highlight">#7</td>
                <td>
            <img class="icon"  alt="Auto Close Tag" src="https://naoray.gallerycdn.vsassets.io/extensions/naoray/laravel-goto-components/1.2.0/1635421420328/Microsoft.VisualStudio.Services.Icons.Default" >
                </td>
                <td>
                  laravel-goto-components
                        <br>
                        (naoray)
                </td>
                <!-- <td class="text-center status-inactive">On Leave</td> -->
            </tr>
            <tr>
                <td class="highlight">#8</td>
                <td>
<img class="icon"  alt="Auto Close Tag" src="https://pgl.gallerycdn.vsassets.io/extensions/pgl/laravel-jump-controller/0.0.33/1681960122487/Microsoft.VisualStudio.Services.Icons.Default" >
                </td>
                <td>
                   laravel-jump-controller
                        <br>
                        (pgl)
                </td>
                <!-- <td class="text-center status-inactive">On Leave</td> -->
            </tr>
            <tr>
                <td class="highlight">#9</td>
                <td>
                    <img class="icon"  alt="Auto Close Tag" src="https://open-southeners.gallerycdn.vsassets.io/extensions/open-southeners/laravel-pint/1.2.1/1720174668351/Microsoft.VisualStudio.Services.Icons.Default" >
                </td>
                <td>
                   Laravel Pint
                        <br>
                        (open-southeners)
                </td>
                <!-- <td class="text-center status-inactive">On Leave</td> -->
            </tr>
            <tr>
                <td class="highlight">#10</td>
                <td>
                  <img class="icon"  alt="Auto Close Tag" src="https://esbenp.gallerycdn.vsassets.io/extensions/esbenp/prettier-vscode/11.0.0/1723648421534/Microsoft.VisualStudio.Services.Icons.Default" >
                </td>
                <td>
                 Prettier - Code formatter
                        <br>
                        (Prettier)
                </td>
                <!-- <td class="text-center status-inactive">On Leave</td> -->
            </tr>
            <tr>
                <td class="highlight">#11</td>
                <td>
                   <img class="icon"  alt="Auto Close Tag" src="https://zobo.gallerycdn.vsassets.io/extensions/zobo/php-intellisense/1.3.3/1694733996289/Microsoft.VisualStudio.Services.Icons.Default" >
                </td>
                <td>
                 PHP IntelliSense
                        <br>
                        (Damjan Cvetko)
                </td>
                <!-- <td class="text-center status-inactive">On Leave</td> -->
            </tr>
            <tr>
                <td class="highlight">#12</td>
                <td>
                   <img class="icon"  alt="Auto Close Tag" src="https://mehedidracula.gallerycdn.vsassets.io/extensions/mehedidracula/php-namespace-resolver/1.1.9/1656799011659/Microsoft.VisualStudio.Services.Icons.Default" >
                </td>
                <td>
                 PHP Namespace Resolver
                        <br>
                        (Mehedi Hassan)
                </td>
                <!-- <td class="text-center status-inactive">On Leave</td> -->
            </tr>
            <tr>
                <td class="highlight">#13</td>
                <td>
                <img class="icon"  alt="Auto Close Tag" src="https://equinusocio.gallerycdn.vsassets.io/extensions/equinusocio/vsc-material-theme-icons/3.8.10/1731100343339/Microsoft.VisualStudio.Services.Icons.Default" >
                </td>
                <td>
                 Material Theme Icons
                        <br>
                        (Equinusocio)
                </td>
                <!-- <td class="text-center status-inactive">On Leave</td> -->
            </tr>
            <tr>
                <td class="highlight">#14</td>
                <td>
                <img class="icon"  alt="Auto Close Tag" src="https://albymor.gallerycdn.vsassets.io/extensions/albymor/increment-selection/0.2.0/1576523763134/Microsoft.VisualStudio.Services.Icons.Default" >
                </td>
                <td>
                 Increment Selection
                        <br>
                        (Alberto Morato)
                </td>
                <!-- <td class="text-center status-inactive">On Leave</td> -->
            </tr>
            <tr>
                <td class="highlight">#15</td>
                <td>
                <img class="icon"  alt="Auto Close Tag" src="https://donjayamanne.gallerycdn.vsassets.io/extensions/donjayamanne/jquerysnippets/0.0.1/1474455550460/Microsoft.VisualStudio.Services.Icons.Default" >
                </td>
                <td>
                 jQuery Code Snippets
                        <br>
                        (Don Jayamanne)
                </td>
                <!-- <td class="text-center status-inactive">On Leave</td> -->
            </tr>
            <tr>
                <td class="highlight">#16</td>
                <td>
                <img class="icon"  alt="Auto Close Tag" src="https://adpyke.gallerycdn.vsassets.io/extensions/adpyke/codesnap/1.3.4/1625238962906/Microsoft.VisualStudio.Services.Icons.Default" >
                </td>
                <td>
                 CodeSnap
                        <br>
                        (adpyke)
                </td>
                <!-- <td class="text-center status-inactive">On Leave</td> -->
            </tr>
            <tr>
                <td class="highlight">#17</td>
                <td>
                <img class="icon"  alt="Auto Close Tag" src="https://sleistner.gallerycdn.vsassets.io/extensions/sleistner/vscode-fileutils/3.10.3/1690034496024/Microsoft.VisualStudio.Services.Icons.Default" >
                    </td>
                </td>
                <td>
                  File Utils
                        <br>
                        (Steffen Leistner)
                </td>
                <!-- <td class="text-center status-inactive">On Leave</td> -->
            </tr>
            <tr>
                <td class="highlight">#18</td>
                <td>
                <img class="icon"  alt="Auto Close Tag" src="https://fallenmax.gallerycdn.vsassets.io/extensions/fallenmax/mithril-emmet/0.7.7/1648523464540/Microsoft.VisualStudio.Services.Icons.Default" >
                    </td>
                </td>
                <td>
                    Mithril Emmet
                        <br>
                        (FallenMax)
                </td>
                <!-- <td class="text-center status-inactive">On Leave</td> -->
            </tr>
            <tr>
                <td class="highlight">#19</td>
                <td>
               <img class="icon"  alt="Auto Close Tag" src="https://liamhammett.gallerycdn.vsassets.io/extensions/liamhammett/inline-parameters/0.2.1/1591646480793/Microsoft.VisualStudio.Services.Icons.Default" >
                    </td>
                </td>
                <td>
               Inline Parameters for VSCode
                        <br>
                        (Liam Hammett)
                </td>
                <!-- <td class="text-center status-inactive">On Leave</td> -->
            </tr>
            <tr>
                <td class="highlight">#20</td>
                <td>
              <img class="icon"  alt="Auto Close Tag" src="https://xyz.gallerycdn.vsassets.io/extensions/xyz/local-history/1.8.1/1583352056596/Microsoft.VisualStudio.Services.Icons.Default" >
                    </td>
                </td>
                <td>
               Local History
                        <br>
                        (xyz)
                </td>
                <!-- <td class="text-center status-inactive">On Leave</td> -->
            </tr>
            <tr>
                <td class="highlight">#21</td>
                <td>
              <img class="icon"  alt="Auto Close Tag" src="https://dotenv.gallerycdn.vsassets.io/extensions/dotenv/dotenv-vscode/0.28.1/1699146869103/Microsoft.VisualStudio.Services.Icons.Default" >
                    </td>
                </td>
                <td>
               Dotenv Official +Vault
                        <br>
                        (Dotenv)
                </td>
                <!-- <td class="text-center status-inactive">On Leave</td> -->
            </tr>
        </tbody>
    </table>
</div>

<br><br>

```sh
// Shift + Ctrl + p   :find(settings.json)
{
    "workbench.iconTheme": "material-icon-theme",
    "laravel-pint.enable": true,
    "[php]": {
    "editor.defaultFormatter": "open-southeners.laravel-pint"
    },
    "[json]": {
    "editor.defaultFormatter": "vscode.json-language-features"
    },
    "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[css]": {
    "editor.defaultFormatter": "vscode.css-language-features"
    },
    "workbench.startupEditor": "none",
    "editor.stickyScroll.enabled": false,
    "diffEditor.ignoreTrimWhitespace": false,
    "git.confirmSync": false,
    "editor.formatOnSave": true,
    "workbench.colorTheme": "Default Light+",
    "files.associations": {
    ".env*": "dotenv"
    },
    "editor.tokenColorCustomizations": {
    "textMateRules": []
    },
    "dotenv.enableAutocloaking": false,
}
```
