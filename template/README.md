# Template

We can use [Cookiecutter](http://cookiecutter.readthedocs.io/en/latest/readme.html), to initialise a project using a template with the same structure seen in the tutorial.

We start by [creating a repository on GitHub](https://help.github.com/articles/creating-a-new-repository/) *without* choosing any additional option, like initialising a readme file. In the following, we refer to the GitHub repository name with *\<project_name\>*.

Install Coockiecutter if you do not have it already installed.

```shell
pip install cookiecutter
```

Go to the folder where you would like to store the project and create the project template.

```shell
cookiecutter https://github.com/Satalia/production_data_science/template
```

You will be prompted with values to fill, like the project name (use *\<project_name\>*), the package name and the author name.

Create a virtual environment and install the package.

```shell
cd <project_name>
mkvirtualenv <package_name>
pip install -e <package_name>
pip freeze | grep -v <package_name> > <package_name>/requirements.txt
git init
git add .
git commit -m "First commit"
git remote add origin <remote_repository_url>
git push -u origin master
```

Here, *\<package_name\>* is the name of the Python package to be used to productionise the exploratory work. They should match the respective values you imputed in Cookiecutter.

Now, create a branch, switch to it,

```shell
git checkout -b <branch_name>
```

and you are ready to start! 🎉