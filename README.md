Sample Flask with Angular web app
====

Sample Flask with Angular web app.

### App Structure
```
/
├── LICENSE.md
├── README.md
├── requirements.txt
└── sample-flask-angular # Flask project folder
    ├── angular # Angular project folder
    │   ├── dist
    │   ├── e2e
    │   ├── karma.conf.js
    │   ├── node_modules
    │   ├── package.json
    │   ├── protractor.conf.js
    │   ├── README.md
    │   ├── src
    │   ├── tsconfig.json
    │   └── tslint.json
    └── main.py
```

Requirements
----

Install the following requisites:

- Python3
- Virtualenv
- NodeJs
- Angular-cli

On a Mac, this would typically be done using the `brew` command.

Installation
----

Create virtual enviroment folder and load:
```sh
$ virtualenv -p python3 .venv
$ source .venv/bin/activate
```

Install python dependencies:
```sh
(.venv) $ pip install -r requirements.txt
```

Install angular dependencies:
```sh
$ cd sample-flask-angular/angular
$ npm install
```


Deployment
----

First build application of Angular with Angular-cli:

```sh
$ cd sample-flask-angular/angular
$ ng build
```
This will compile the Angular code and output artifacts into the `dist` directory within `sample-flask-angular/angular`. 


Start server:
```sh
$ source .venv/bin/activate
(.venv) $ python sample-flask-angular/main.py
```

Routes
----
- `/`: Index route will serve angular application.
- `/hello`: return Flask `hello` function.

Authors
----

- Ismael Taboada: [profile](https://github.com/ismtabo)
- Pavel Berkovich: [profile](https://github.com/pb593)
