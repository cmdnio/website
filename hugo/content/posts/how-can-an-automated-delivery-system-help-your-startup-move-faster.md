---
title: "How can an automated delivery system help your startup move faster"
date: 2022-07-25
image: /blog/images/how-can-an-automated-delivery-system-help-your-startup-move-faster-hero.jpg
tags: ['product', 'devops', 'development', 'quality', 'delivery']
author: Dmitry Zaets, Engineering Manager & Co-Founder 
---

After you have defined the minimal scope of your application and started the development process, it is crucial to be able to test the features as soon as possible. Not only to catch bugs but also to verify that the features work the way they were meant to work.

The problem is that the features often look and feel different when implemented from what you've imagined they would like in a functional design or even may not solve the initial problem. It may occur due to various reasons, for example:

- There might be some technical limitations (for example, the new feature can't be easily integrated into the existing codebase without significant code changes)
- Functional requirements or feature flows conflict with each other and requires changes during the implementation
- The visual design implementation may be different from the functional design

I've seen many companies where the product owners tested the features only after engineers made the production deployment, and developers made the deployments monthly. That may happen because of many reasons, but the most typical ones are these:

- The team doesn't have a well-defined testing and delivery process.
- The release cycle is too bulky - multiple complex features are getting released at the same time.

Each reason makes teams afraid to break something and scared to do the deployments. Let's discuss the solution to each problem separately.

## Defining the testing and integration process

The earlier you can test the feature - the better. So as soon as the engineering team has a part of the feature ready for demonstration - you need to try it. There are several ways to get access to a testable version of the feature:

- A developer can demonstrate the feature on their computer - this approach requires an extra effort from a developer and would block their work.
- You can check the latest version of the feature locally on your computer - it requires having the project environment locally and updating it for each feature.
- Engineers could merge the feature into the project and deploy the latest version to a remote server - often called **staging** or **test environment.**
- Each feature can be separately deployed into a remote server with a dedicated URL before it gets integrated into the project's latest version.

We ordered the list by the complexity of the implementation, so you can start with the most straightforward option and evolve the testing strategy over time, getting to a more complex and effective one.

The bigger your engineering team would get, the more you would feel the need to create a Staging environment. We recommend having one from day one if it's possible. It would allow you to prepare, test, and polish your project each time before its production release.

The bigger the project, the more often it would have a risk of problems occurring after the new feature is merged into the codebase. It would also be harder to identify those problems manually. Sometimes, one feature affects the parts of the product used by other features, which may break elements of the functionality that used to work. To help ensure that the new code would not break the existing one, engineers have developed a couple of approaches and tools to automate the testing. Here is a couple of them:

- **Code linting** - an automated tool that checks the code for common mistakes, allows to follow the same code style across the whole project, and much more.
- **Unit testing** - a type of testing when small logical blocks, called units, are tested separately.
- **Integration testing** - a type of testing when the integration between different blocks is being tested.
- **End-to-end testing** - a type of testing when the feature is tested as a whole.

In Cmd + N, we analyze each customer's project needs and suggest which type of automated testing would help most. The key is to seek the right balance between the different levels of testing and invest a reasonable amount of time and effort to gain confidence in the quality of the product. Linting and unit testing usually require the least effort but bring the most value. The other types of testing require more effort and might be overkill for the fast-changing product.

To get better results, your team can set up the checks to be executed not only on the engineer computers manually but automatically on each commit, forbidding the commits that have problems. Additionally, the same tests could be performed before the deployment to staging and production environments to ensure that the deployed code works correctly.

## Simplifying the release cycle

You can test the features much faster and safer when you have a staging environment and the checks are in place. Also, the developers tend to become more confident about the quality of the code and eager to deploy more often. Ideally, engineers should deploy the features as soon as they are tested and ready to be released instead of waiting for a particular deployment day. In CMD + N, we encourage an approach called CI/CD (continuous integration and deployment). That means a couple of things:

- We constantly test the new features both manually and automatically.
- As soon as the feature is ready for testing - it gets deployed to a testing environment with a dedicated URL.
- QA engineers ensure that the feature works as expected and does not break other project parts.
- Product owners perform the acceptance testing, ensuring that the feature works as they planned it to work.
- The feature is merged into the codebase and immediately deployed to a staging environment.
- Once the new feature is deployed to staging, smoke testing could be performed.
- After that, the feature is ready for production deployment at any time.

## Conclusion

Based on our experience, having well-defined testing and release strategies improve both the product quality and velocity of the engineering team. Often in the early stage of the product, people underestimate the importance of such simple processes, which slows down the team and doesn't allow iterating faster.