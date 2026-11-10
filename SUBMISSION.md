# Secure DevOps – Project 2

**Name:** Ahmed Alameri
**Student ID:** 24528667

## Repository links

| Repo | Link |
|---|---|
| Forked `aws-elastic-beanstalk-express-js-sample` (holds the `Jenkinsfile`) | https://github.com/AhmedSamiAlameri/aws-elastic-beanstalk-express-js-sample |
| `Project2-Compose` (Docker Compose stack: Jenkins + Docker-in-Docker) | https://github.com/AhmedSamiAlameri/Project2-Compose |

Jenkins pipeline: `24528667-Project-2-pipeline`, set to "Pipeline script from SCM" using the fork's `Jenkinsfile` on `main`. Build #2 result: **SUCCESS**.

The Word document for Blackboard is [`Project2-Submission.docx`](Project2-Submission.docx).

## Graded tasks and proof

| # | Task | Points | Proof |
|---|---|---|---|
| 1 | Fork `aws-samples/aws-elastic-beanstalk-express-js-sample` to my GitHub | 5 | [Fork link](https://github.com/AhmedSamiAlameri/aws-elastic-beanstalk-express-js-sample), [`05-github-fork-jenkinsfile.png`](screenshots/05-github-fork-jenkinsfile.png) ("forked from aws-samples/…") |
| 2 | Create the repo `Project2-Compose` | 5 | [Project2-Compose link](https://github.com/AhmedSamiAlameri/Project2-Compose), [`06-github-project2-compose.png`](screenshots/06-github-project2-compose.png) |
| 3 | Option 1: Docker Compose stack running a dind container and a Jenkins container that uses it to run pipelines | 30 | [`docker-compose.yml`](https://github.com/AhmedSamiAlameri/Project2-Compose/blob/main/docker-compose.yml), [`Dockerfile`](https://github.com/AhmedSamiAlameri/Project2-Compose/blob/main/Dockerfile), [`04-console-output-success.png`](screenshots/04-console-output-success.png) (the `node:16` agent container is started on the dind daemon) |
| 4 | Commit and push the compose setup to `main` of Project2-Compose | 10 | [`06-github-project2-compose.png`](screenshots/06-github-project2-compose.png) (`docker-compose.yml` on `main`), [commit history](https://github.com/AhmedSamiAlameri/Project2-Compose/commits/main) |
| 5 | `Jenkinsfile` in the fork's root: Node 16 Docker image as the agent, build step runs `npm install --save` | 20 | [`Jenkinsfile`](https://github.com/AhmedSamiAlameri/aws-elastic-beanstalk-express-js-sample/blob/main/Jenkinsfile), [`03-build-stages.png`](screenshots/03-build-stages.png) (`node --version` gives v16.20.2, then `npm install --save`) |
| 6 | Commit and push the `Jenkinsfile` to `main` of the fork | 10 | [`05-github-fork-jenkinsfile.png`](screenshots/05-github-fork-jenkinsfile.png) (`Jenkinsfile` in root on `main`), [commit history](https://github.com/AhmedSamiAlameri/aws-elastic-beanstalk-express-js-sample/commits/main) |
| 7 | Pipeline project `24528667-Project-2-pipeline` using "Pipeline script from SCM", running successfully | 20 | [`01-pipeline-job-page.png`](screenshots/01-pipeline-job-page.png), [`02-pipeline-config-scm.png`](screenshots/02-pipeline-config-scm.png), [`03-build-stages.png`](screenshots/03-build-stages.png), [`04-console-output-success.png`](screenshots/04-console-output-success.png) (ends in `Finished: SUCCESS`) |

## Screenshots

| File | Shows |
|---|---|
| [`01-pipeline-job-page.png`](screenshots/01-pipeline-job-page.png) | Jenkins job page; build #2 is the last successful build |
| [`02-pipeline-config-scm.png`](screenshots/02-pipeline-config-scm.png) | Job configuration: Pipeline script from SCM, Git, the fork's URL, `*/main`, `Jenkinsfile` |
| [`03-build-stages.png`](screenshots/03-build-stages.png) | Pipeline Overview for build #2: Checkout SCM and Build stages passed |
| [`04-console-output-success.png`](screenshots/04-console-output-success.png) | Full console output for build #2, ending in `Finished: SUCCESS` |
| [`05-github-fork-jenkinsfile.png`](screenshots/05-github-fork-jenkinsfile.png) | The fork on GitHub with `Jenkinsfile` in the root |
| [`06-github-project2-compose.png`](screenshots/06-github-project2-compose.png) | Project2-Compose on GitHub with `docker-compose.yml` |
