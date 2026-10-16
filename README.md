# CI/CD Tools and Practices Final Project Template

## Project name

**ci-cd-final-project**

This repository contains the IBM / Coursera **Continuous Integration and Continuous Delivery (CI/CD) Final Project**. The sample Flask counter microservice is validated with GitHub Actions and delivered using Tekton and OpenShift Pipelines.

## Continuous Integration

The CI workflow at [`.github/workflows/workflow.yml`](.github/workflows/workflow.yml) runs on pushes and pull requests to `main`. It checks out the source, installs dependencies, lints with flake8, and runs nose unit tests with coverage.

## Continuous Delivery

Tekton task definitions in [`.tekton/tasks.yml`](.tekton/tasks.yml) include a workspace cleanup task and nose test task. The lab's OpenShift pipeline links these with git-clone, flake8, buildah, and an OpenShift deployment step.

## Development setup

```bash
bash ./bin/setup.sh
```

Close the terminal with `exit` and open a new terminal to activate the Python virtual environment.

## License

Licensed under the Apache-2.0 License. See [LICENSE](LICENSE).

## Author

Skills Network (template); project implementation for the IBM CI/CD final assignment.
