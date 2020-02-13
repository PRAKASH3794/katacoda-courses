Clone the source for the sample Node.js project and inspect the code.

`git clone https://github.com/javajon/node-js-tekton`

Navigate into the directory.

`cd node-js-tekton`{{execute}}

Inspect some of the files.

`tree`

`cat src/app.js`{{execute}}

`cat src/Dockerfile`{{execute}}

`cat src/deploy.yaml`{{execute}}

At this point we could build the application into a container and deploy on Kubernetes using a series of command line tools. However, most things deployed to Kubernetes should be infrastructure-as-code including the recipes that continuously deliver application updates as we fix and evolve our applications. This CI/CD process is often captured in source code for CI/CD pipelines. Tekton allows you to declare your pipelines in code.