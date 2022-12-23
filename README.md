# Data analytics template

Initialize new repository using this template. Use this README as base for your projects documentation.



# Prequisites

python, pip, pip-tools

Optional: 

 - Docker desktop 4.15.0 (93002)
 - Visual studio code
   - VSC 1.74.0
   - VSC Dev Containers Extension v0.245.2 (latest version has issues with MacOS & M1)

# Getting started:

## Setup git repository using template

0. (Create [GitHub account](https://github.com/) if you do not have one
    already.
1. Sign into your GitHub homepage
2. Go to
    [github.com/City-of-Helsinki/analytics_template](https://github.com/City-of-Helsinki/analytics_template)
    and click the green button that says ‘Use this template’.
3. Give your project a name. Do not use the dash symbol ‘-’, but rather
    the underscore ’\_’, because the name of the repo will become the
    name of your Python module.
4. If you are creating a project for your organization, change the
    owner of the repo. From the drop down bar, select your organization
    GitHub account (e.g. City-of-Helsinki). You need to be included as a
    team member to the GitHub of the organization.
5. Define your project publicity (you can change this later, but most
    likely you want to begin with a private repo).
6. Click ‘Create repository from template’

## Development environment setup

### Codespaces

If your organization has
[Codespaces](https://github.com/features/codespaces) enabled (requires
GitHub Enterprise & Azure subscription), you can do development using Visual Studio Code 
and you are now ready to begin development. Just launch the repository in a codespace, and a dev
container is automatically set up!

### Local vscode with python

Open cloned repository folder in Visual Studio Code.
Try to execute any python script. Virtual environment installation will be prompted. 

### Manual installation in local environment:

1. Create virtual environment:
   `python3 -m venv venv`
2. Activate virtualenv:
   `source venv/bin/activate`
3. Install pip-tools:
   `pip install pip-tools`
4. Compile requirements:
   `pip-compile --upgrade --generate-hashes --allow-unsafe --resolver=backtracking -o requirements.txt requirements.in dev-requirements.in`
5. Install requirements:
   `pip-sync requirements.txt`
6. Create an ipython kernel for running the notebooks:
    `python -m ipykernel install --user --name analytics_env`

# Development



## Dependencies

Add library dependencies to requirements/requirements and use pip-compile to construct requirement.txt. 
File dev-requirements.in is intended for project development environment requirements.
Use update_requirements.sh to compile requirements.txt.
