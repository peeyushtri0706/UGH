# <span class="greenbox">Docker "Hello, World" POC1 🙂</span>

This folder contains a `Dockerfile` to build a very simple Docker image—one which contains simple Node.js app in the app.js file, using Express:

```
const express = require('express');
const app = express();
const PORT = process.env.PORT || 3000;
 
app.get('/', (req, res) => {
    res.send('Hello World');
});
 
app.listen(PORT, () => {
    console.log(`Hello world app running on port ${PORT}`);
});
```

 👉"Hello, World"!—to demonstrate how to create Docker images and deploy the image on `AWS ECR`. 


## <span class="heading">Building the Docker container</span>

✅ Install [Docker](https://www.docker.com/) and make sure it's on your `PATH`.</br>
✅ Run `docker build --file Dockerfile -t hello-world-example .`.</br>
✅ Run `docker run -it `.</br>
✅ You should see the text "Hello, World!"</br>



## <span class="heading">Github workflow for Build and Deploy to AWS ECR</span>

<div><ul style="list-style: none;">
<li><span class="greenbox">Step 1</span>: Set Up an Amazon ECR Repository. Log in to the AWS Management Console and navigate to the Amazon ECR service.</br></li>
<li><span class="greenbox">Step 2</span>: Configure AWS Credentials.</br></li>
<li><span class="greenbox">Step 3</span>: Create the Dockerfile and Push to github repository.</br></li>
<li><span class="greenbox">Step 4</span>: Configure GitHub Secrets. </br></li>
<li><span class="greenbox">Step 5</span>: Create GitHub Actions Workflow. </br></li>
<li><span class="greenbox">Step 6</span>: Trigger the GitHub Workflow</br></li></ul></div>

## <span class="heading">Additional link</span>

* GitHub Actions documentation homepage: https://docs.github.com/en/actions 
* Docker documentation homepage: https://docs.docker.com 
* AWS ECR documentation homepage: https://docs.aws.amazon.com/ecr/

 