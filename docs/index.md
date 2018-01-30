# High-level DevOps

## Question: what problems do enterprises face that DevOps can solve?

- Communication problems between developers ("works on my machine")
- Inability to quickly go from commit to release
- Problems with reliability in production (scalability, uptime, response times)
- Late responses to production release problems

## Task: draw a diagram for the whole DevOps process

![The process of turning an idea into reality](img/devops-process.jpg)

## Task: describe the process of a software release, step-by-step

1. Idea

2. Plan

3. Code, commit, push to feature-branch

4. Pipeline:
    - build
    - deploy
    - test end-to-end

6. When happy, merge pull request into master, then run pipeline:
    - build
    - deploy
    - test end-to-end

7. Monitor and respond to alerts when necessary.

## Question: who's responsibility is each step?

Steps 4 and 5 are done via a CI pipeline.

Other steps are done by humans, such as marketing people or engineering people.

## Question: what's the point of DevOps?

With DevOps, we get:

- Increased deployment frequency (feature / hotfix releases)
- Reliable releases that never fail in production

Business value:

- Happy application developers
- Less time (on payroll) spent on fixing and maintaining things
- Happy end customers (requested features and fixes get delivered quicker and reliably)
- No PR blunders due to security issues
