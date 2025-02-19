# Package your Python code in 5 questions

This template is maintained by the [research engineering team](https://www.uu.nl/en/research/research-data-management/support/research-engineers) of Utrecht University.
It uses [Copier](https://copier.readthedocs.io/en/stable/) for creating your package. The goal of this template is to be minimalist; 5 questions is all you need to answer
to create your package.

## Features

- Sphinx documentation for readthedocs
- Ruff for linting
- Pytest for unit tests
- Pytest-cov for coverage testing
- Nbval for integration/notebook tests
- Mypy for type checking
- GitHub action continuous integration
- Modularity: the above features can be selected individually
- Uses `setuptools-scm` for packaging and version control

## Usage

### 1. Install copier

You can install copier using `pip`, `pipx` or `uvx`.

```python
pip install copier
```

While using `pip` is the easiest, [`pipx`](https://github.com/pypa/pipx) or [`uvx`](https://docs.astral.sh/uv/) are recommended.

### 2. Create your package

To create your new package use:

```sh
copier copy gh:UtrechtUniversity/python-template directory_of_your_package
```

Answer the questions, and you will have a new directory that will get you started with your package. Feel free to disable some of
the features you don't understand for now. You can always add these features into your repository later.

### 3. Initialize a git repository

You will need to initialize a git repository in the newly created folder for the package to be installable ([instructions for installing git]([git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)). 

```sh
cd directory_of_your_package
git init
```

### 4. Try installing the package


> [!TIP]
> We recommend working with [virual environments](https://docs.astral.sh/uv/pip/environments/#creating-a-virtual-environment). If you are working with `uv` for Python project management, initialize a `venv` in your repository with the following commands:
> ```
> uv python pin 3.11
> uv sync
> ```
> Where `3.11` can be changed to the Python version of your choice.

You can install your package now:

```sh
pip install . 
```
and test whether the installation works correctly:

```sh
python -c "import your_package_name; your_package_name.hello_world('Universe')"
```
This should return `Hello Universe!!`.

### 5. Upload your package to GitHub

The first step is to create an empty repository on [GitHub](github.com) using the web interface. Your empty repository typically contains instructions on how to connect your local repository to it. Otherwise, you there should be a green code button; copy the link to your repository. Then on your local machine type:

```
git remote add origin link_to_your_github_repository
```

Add all the files and upload it to GitHub:

```
git add .
git commit -m "Initial commit from Python template"
git push
```

### 6. Start modifying the template

You are now ready to add your own Python files to your repository!





