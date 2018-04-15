# Hosted CI/CD scripts [![](https://user-images.githubusercontent.com/516342/38551453-17b7e8ca-3cb1-11e8-9754-b70c6e0f316c.png)](https://github.com/omrilotan/ci-cd.net#readme)

A collection of hosted CI-CD generic helper scripts, which aim to streamline continues integration and delivery processes across services. This project's goal is to include non business logic scripts which can be used out-of-the-box or adapted by arguments.

## Using hosted shell scripts
Using a script with defaults
```
curl ci-cd.net/v1/<SCRIPT> | sh
```

Passing arguments
```bash
curl ci-cd.net/v1/<SCRIPT> | sh -s <ARGUMENT_1> <ARGUMENT_2>
```

Visit [ci-cd.net](http://ci-cd.net) for full feature list

[auto published](https://circleci.com/gh/omrilotan/ci-cd.net) [<img height="32px" src="https://user-images.githubusercontent.com/516342/37675827-f3016264-2c7e-11e8-9806-46341bec1d6c.png">](https://omrilotan.com)
