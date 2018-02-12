# developer

## Local copies of repos

The environment assumes a relative path to git clones of the probcomp repos such as:

```
../bayeslite
../cgpm
../crosscat
../workshop-materials
.
.
```

Clone these yourself or run the bootstrap script to download them automatically.

## Common Commands

### Bootstrap the local dev environment (or reinstall probcomp libraries in docker environment)

```
make bootstrap
```

### Start Jupyter (required for other commands to work)

```
make up
```

Output will show you a local URL to access jupyter:

```
notebook_1  |     Copy/paste this URL into your browser when you connect for the first time,
notebook_1  |     to login with a token:
notebook_1  |         http://localhost:8888/?token=b032fbc6928fdaecc3bd7800f1b90f36a5a4ed99d5c7d59a
```

### Start ipython

```
make ipython
```

### Start a bayeslite shell

```
make shell
```

### Enable development mode

When you first setup your development environment or if you restart the docker container, you'll need to enable development mode by first uninstalling the conda package. Run `make <REPO_NAME>-dev` to uninstall the conda package and use your local repo instead:

```
make bayeslite-dev
```

### Installing and/or making local changes take effect

Build and install from local sources and re-run to make changes take effect with `make <REPO_NAME>`:

```
make bayeslite
```

### Running tests

Run a repo's tests with `make <REPO_NAME>-test`:

```
make bayeslite-test
```

### Run a bash shell inside the docker container

```
make bash
```

### Install docker

```
make install-docker
```

### Install docker-compose

```
make install-docker-compose
```
