---
sidebar_position: 40
sidebar_label: Deploy your first website
---

# Deploy your first website

At this point, you should have set up an integration that connects to your chosen source code management tool (e.g. GitHub). Now, we’ll leverage this integration to create a first application and CI/CD processes to eventually deploy and operationalize your first application.

> This guide assumes you have an existing project you want to deploy. This project must be a JavaScript-based application (e.g. React) and synced to the source code management tool you've set up earlier.

## What is a Stack?

> **TL;DR**: Leanly Stacks are a unified way to manage the lifecycle of your cloud infrastructure, platforms, and applications. With full support for diverse technologies and integrations, they empower you to efficiently build, deploy, monitor, and operate your workloads across various cloud environments.

Head over to the [Leanly Stacks](/stacks) section to learn more.

## Deploy your first static website

### Static Website

In this guide, we’ll deploy a simple [static website](/stacks/applications/static-js-app). This website will be provided by Leanly's Instant Web Deploy, backed by AWS's powerful content delivery network, [Amazon CloudFront](https://aws.amazon.com/cloudfront/). Despite its impressive performance and global reach, this serverless solution is a cost-effective way to host static websites. You’ll see how quickly it can be set up!

1. Go to your Leanly tenant and open the **Applications Catalog**.

1. Choose **Static JavaScript Application**.

1. Enter a friendly **name** for your stack. This is used only within Leanly to help you easily identify your application.

1. Select the **GitHub owner** you set up earlier.

   > Not seeing any owners? Make sure you've [set up your initial GitHub integration](/getting-started/integrations)

1. Select the **repository** the project you want to deploy is synced to.

1. Optionally, change the **branch** the project you want to deploy is synced to.

1. Click **Next** to move to the review step.

1. On the review page, double-check your configuration details. Once everything looks good, click **Submit** to start the deployment.

1. You’ll be taken to your new application’s dashboard in Leanly. Feel free to explore while your resources are being provisioned.

Now, let’s create a deployable artifact from your current React application source code:

1. Navigate to the **CI Builds** tab.

1. Locate the **Run GitHub Actions Workflow** operation and click Run. This triggers the pre-configured GitHub Actions CI workflow set up during bootstrapping.

1. In the form that appears, simply follow the steps until you click **Submit** — no input is needed.

1. After submission, the operation’s status will be updated, indicating whether the workflow trigger was successful.

1. To view progress and details, follow the GitHub Actions workflow URL provided in the _CI Builds_ tab.

Once the CI process finishes, a deployable artifact is ready — your first live application is just a few steps away. Let’s return to your Leanly tenant to deploy it.

1. Go to the **Environments** tab in your application stack.

1. Click **+ Add**.

1. Leave _Leanly Instant Web Deploy_ as your deployment type for now.

   > Good to know: _Leanly Instant Web Deploy_ will create a fully managed deployment of your application. Hassle free! Feel free to try different options later.

1. Select the generated build artifact. It’s named after the **Git commit hash**, uniquely tying it to the exact state of your code at the time of creation.

1. Click **Next** to proceed to the review step.

1. Review your configuration details. If everything looks good, click **Submit** to begin the deployment.

1. You’ll be redirected back to the application dashboard. Leanly will now provision your resources.

This might take a minute — as a global content delivery network is being rolled out on your behalf. Sounds complex? It is — but Leanly handles all the infrastructure intricacies so you can focus on building your application.

After a short wait, your _Leanly Instant Web Deploy_ will be marked as fulfilled, and your app’s live endpoint will appear. Go ahead and check it out!

### Next

Congratulations! 🎉 You now have a fully functional GitHub repository, complete with everything you need to build your application - including built-in continuous integration, deployment workflows, and safety checks.

Now that your application is live, here are a few things you can do:

- Make changes to your codebase and trigger new CI runs to generate fresh deployable artifacts.

- Switch your existing environment to a different artifact — great for rolling forward or reverting to a previous version.

- Deploy a second environment using a different artifact to compare multiple live versions side by side.

- Play with other deployment options and deploy an environment in your own cloud account.

- Clean up by destroying any environments you no longer need.
