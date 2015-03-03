# Blueprint

Blueprint is a lightweight deployment tool which enables technical and
non-technical to deploy code or perform scheduled tasks for their environments.

### Installation

To make Blueprint as versatile as possible, the only dependencies are PHP (5.4+)
and a database such as MySQL - everything else is optional.

### Example Blueprint file

To configure a job, Blueprint looks for a file named '.blueprint.yml' within
your source directory. This file contains a series of options and instructions
to carry out once a trigger has been received from an endpoint (or user
operation).

Here is an example:

```yaml
name: Example codebase
vcs: git

notifications:
  email:
    - "jacob@example.com"
    - "team.email.test@example.com"

on_success:
  notify:
    - email

on_failure:
  notify:
    - email
```

### Providers

- GitHub

### Contributing

Found a bug? Thought of a feature you would like to see? Open a pull request!

### License

This project is licensed under the MIT license.
