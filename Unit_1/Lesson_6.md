# Lesson 6: Ephemeral Environments

## Ephermeral Environments definition

Temporary deployments that have self-contained versions of your application, generally every feature branch

e.g. 

say a dev is changing something on a website, and they'd like to get feedback

a code reviewer would look at the code, not seeing the visual ramifications, but with an ephemeral environment, they would be able to see a version of the website with the proposed change

it's like halfwau between a dev and stage environment

- Accelerates software development lifecycle
- Allows devs to share changes with designers, managers and other stakeholders

## ephemeral environments have a hard time dealing with state, like dealing with databases or microservives

<hr>

## How do databases work in ephemeral environments?
- Prepopulated data - it contains representative, anonymized data - to pass security audits, all Personally-Identifiable Information (PII) must be scrubbed from databases to be used
- Undoable - If data is deleted or modified, it should be easy to reset the database to its original state. 
- Migrated - Database uses the scheme currently used in production, and has proposed migrations run against it: one of the most common classes of problems uncovered by ephermeral environments are broken or non-performant database migrations. 

<hr>

## Ephemeral environment lifecycle management: 

- Option A: tie the lifecycle to the life of a pull/merge request
    - biggest factor to consider is cost, what if we had 30 open PRs?
- Option B: create a ChatOps bot that allows creating a new environment for a specific branch with a small timeout
    - can be slow, hard to find when to delete
- Option C: create an ephemeral environment for every commit, and hibernate them the second they are provisioned, then wake them up as they are required
    - Best option but not many providers do this

<hr>

## Continuous Staging Definition
CI/CD is merged with ephemeral environments to form a unified CI/CD and review process for every commit 

<hr>

## DIY ephemeral environments

Budget 6-12 months of engineering time for setup, then dedicated person for managing these environments

Will need a cloud service provider

Create a Slackbot that responds to /env-create-for-mybranch with a link

## [timestamp to the setup of an ephemeral environment](https://youtu.be/j5Zsa_eOXeY?t=3962)