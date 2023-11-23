# lucentLIMS
a translucnet OpenSource LIMS - Project and progress overview

## Motivation
The supply of "Laboratory Information and Management Systems" (LIMS) is vast but gets considerably thinner if you're looking for an OpenSource offering. But even then you have great options. lucentLIMS aims to be one of them, especially if you need a system, that is easy to understand (almost as if it's translucent) and hence easily adaptable.

Building on top of R and Shiny, lucentLIMS aims at smaller laboratories with a tech savvy staff. Many universities teach R in their courses and it is generally widespread in the scienfitic community. The spread of its' basic components - R, Shiny and MariaDB / MySQL - allows administrators to quickly rewrite lucentLIMS' code to fit their specific needs. The code is kept deliberatly simple so that examples from the web can be easily integrated. Therefore coding elegance is no priority.

## Security
Instead of implementing its own authentification, lucentLIMS is using well established Linux methods such as ssh tunneling. Rights and privileges on database level are handled directly by MariaDB. A lucentLIMS user is always also a unix as well as a MariaDB user.

## Windows Compatibility
As a web app lucentLIMS can be used on any platform given a modern browser. The server backend is specifically tailored to be installed on a unix like operating system. While running a shiny app on a Windows machine isn't difficult, the authentification system would need to be reworked to use Windows as a backend.

## Requirements
A Linux server and the ability to install the following packages. Container images should be fine. TODO: lucentLIMS should be a container too.

### MariaDB
Version 10 or higher.

### Nginx
Version 1.14 or higher.

### R
* [shiny](https://shiny.posit.co/)
* [shinydashboard](https://rstudio.github.io/shinydashboard/)
* [shinywidgets](https://github.com/dreamRs/shinyWidgets)
* [shinyjs](https://cran.r-project.org/web/packages/shinyjs/index.html)
* [leaflet](https://rstudio.github.io/leaflet/)
* [leaflet.extras](https://cran.r-project.org/web/packages/leaflet.extras/index.html)

### Python (command console only)
* ...