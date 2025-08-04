---
sidebar_position: 40
sidebar_label: Deploy your first application
---

# Deploy your first application

## What is a Stack?

> **TL;DR**: Leanly Stacks are a unified way to manage the lifecycle of your cloud infrastructure, platforms, and applications. With full support for diverse technologies and integrations, they empower you to efficiently build, deploy, monitor, and operate your workloads across various cloud environments.

Head over to the [Leanly Stacks](/stacks) section to learn more.

## Deploy your first React Application stack

### Getting Started Recap

At this point, you should have set up an integration that connects to your chosen source code management tool (e.g. GitHub). Now, we’ll leverage this integration to bootstrap a first React application and CI/CD processes to eventually deploy and operationalize your first application.

### Leanly React App Starter Kit

In this guide, we’ll deploy a simple Static React Website. This website will be provided by Leanly's Instant Web Deploy, backed by AWS's powerful content delivery network, [Amazon CloudFront](https://aws.amazon.com/cloudfront/). Despite its impressive performance and global reach, this serverless solution is a cost-effective way to host static websites. You’ll see how quickly it can be set up!

1. Go to your Leanly tenant and open the **Applications Catalog**.

1. Choose **Leanly React App Starter Kit**.

1. Enter a friendly **name** for your stack. This is used only within Leanly to help you easily identify your application.

1. Specify a **repository name** — this will be the actual Git repository that Leanly bootstraps for you.

1. Skip the remaining settings for now; we’ll come back to them shortly.

1. Click **Next** to move to the review step.

1. On the review page, double-check your configuration details. Once everything looks good, click **Submit** to start the deployment.

1. You’ll be taken to your new application’s dashboard in Leanly. Feel free to explore while your resources are being provisioned.

Now, let’s create a deployable artifact from your current React application source code:

1. Navigate to the **CI/CD** tab.

1. Locate the **Run GitHub Actions Workflow** operation and click Run. This triggers the pre-configured GitHub Actions CI workflow set up during bootstrapping.

1. In the form that appears, simply follow the steps until you click **Submit** — no input is needed.

1. After submission, the operation’s status will be updated, indicating whether the workflow trigger was successful.

1. To view progress and details, follow the GitHub Actions workflow URL provided in the CI/CD tab.

Once the CI process finishes, a deployable artifact is ready—your first live application is just a few steps away. Let’s return to your Leanly tenant to deploy it.

1. Go to the **Leanly Instant Web Deploy** tab in your application stack.

1. Click **+ Add**.

1. Select the generated artifact. It’s named after the **Git commit hash**, uniquely tying it to the exact state of your code at the time of creation.

1. Click **Next** to proceed to the review step.

1. Review your configuration details. If everything looks good, click **Submit** to begin the deployment.

1. You’ll be redirected back to the application dashboard. Leanly will now provision your resources.

This might take a minute — as a global content delivery network is being rolled out on your behalf. Sounds complex? It is — but Leanly handles all the infrastructure intricacies so you can focus on building your application.

After a short wait, your _Leanly Instant Web Deploy_ will be marked as fulfilled, and your app’s live endpoint will appear. Go ahead and check it out!

### Next

Congratulations! 🎉 You now have a fully functional GitHub repository, complete with everything you need to build your application - including built-in continuous integration, deployment workflows, and safety checks.

Now that your application is live, here are a few things you can do:

- Make changes to your codebase and trigger new CI runs to generate fresh deployable artifacts.

- Switch your existing _Leanly Instant Web Deploy_ instance to a different artifact — great for rolling forward or reverting to a previous version.

- Deploy a second _Leanly Instant Web Deploy_ instance using a different artifact to compare multiple live versions side by side.

- Clean up by destroying any _Leanly Instant Web Deploy_ instances you no longer need.
