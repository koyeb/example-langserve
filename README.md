<div align="center">
  <a href="https://koyeb.com">
    <img src="https://www.koyeb.com/static/images/icons/koyeb.svg" alt="Logo" width="80" height="80">
  </a>
  <h3 align="center">Koyeb Serverless Platform</h3>
  <p align="center">
    Deploy LangServe on Koyeb
    <br />
    <a href="https://koyeb.com">Learn more about Koyeb</a>
    ·
    <a href="https://koyeb.com/docs">Explore the documentation</a>
    ·
    <a href="https://koyeb.com/tutorials">Discover our tutorials</a>
  </p>
</div>


## About Koyeb and the LangServe example application

Koyeb is a developer-friendly serverless platform to deploy apps globally. No-ops, servers, or infrastructure management.

This repository contains is designed to show how LangServe applications can be deployed to Koyeb.  The image that this repository builds serves a LangServe application that uses LangChain to query the OpenAI API.

You can follow the [associated tutorial](https://www.koyeb.com/tutorials/using-langserve-to-build-rest-apis-for-langchain-applications) to learn more about how the example was constructed.

## Getting Started

Follow the steps below to deploy the LangServe application to your Koyeb account.

### Requirements

To use this repository, you need:

* A Koyeb account to build the Docker image and run the Dockerized application.  If you don't already have an account, you can [sign-up for free](https://app.koyeb.com/auth/signup).
* An [OpenAI](https://openai.com/) API key so that our application can send queries to OpenAI.

### Deploy using the Koyeb button

The fastest way to deploy the LangServe application is to click the **Deploy to Koyeb** button below.

[![Deploy to Koyeb](https://www.koyeb.com/static/images/deploy/button.svg)](https://app.koyeb.com/deploy?name=example-langserve&type=git&repository=koyeb%2Fexample-langserve&branch=main&builder=dockerfile&env%5BOPENAI_API_KEY%5D=CHANGE_ME&ports=8000%3Bhttp%3B%2F)

Clicking on this button brings you to the Koyeb App creation page with most of the settings pre-configured to launch this application.  You will need to replace the value for the following variable:

* `OPENAI_API_KEY`: Set to your OpenAI API key.

_To modify this application example, you will need to fork this repository. Checkout the [fork and deploy](#fork-and-deploy-to-koyeb) instructions._

### Fork and deploy to Koyeb

If you want to customize and enhance this application, you need to fork this repository.

If you used the **Deploy to Koyeb** button, you can simply link your service to your forked repository to be able to push changes.  Alternatively, you can manually create the application as described below.

On the [Koyeb Control Panel](https://app.koyeb.com/), click the **Create App** button to go to the App creation page.

1. Click **Create App** in the Koyeb control panel.
2. Select **GitHub** as the deployment option.
3. Choose the GitHub **repository** and **branch** containing your application code.
4. Name your service, for example `example-langserve`.
5. Select **Dockerfile** as the builder for the project.
6. Expand the **Advanced** section and click **Add Variable** to configure a new environment variable.  Create a variable called `OPENAI_API_KEY`.  Select the **Secret** type and choose **Create secret** in the value.  In the form that appears, create a new secret containing your OpenAI API key.
6. Name the App, for example `example-langserve`.
7. Click the **Deploy** button.

A container image for the LangServe application will be built and a container will be deployed to Koyeb.  You can follow the build process as the repository is cloned, built, and deployed.  Once the deployment is complete, it will be accessible using the Koyeb subdomain for your service.  Visit the URL with `/openai/playground` appended to view the prompt interface.

## Contributing

If you have any questions, ideas or suggestions regarding this application sample, feel free to open an [issue](//github.com/koyeb/example-langserve/issues) or fork this repository and open a [pull request](//github.com/koyeb/example-langserve/pulls).

## Contact

[Koyeb](https://www.koyeb.com) - [@gokoyeb](https://twitter.com/gokoyeb) - [Slack](http://slack.koyeb.com/)
