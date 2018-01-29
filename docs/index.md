# High-level DevOps

## Task: describe the whole process of developing and releasing a software feature

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

## Task: who's responsibility is each step?

Steps 4 and 5 are done via a CI pipeline.

Other steps are done by humans, such as marketing people, engineering people, and
