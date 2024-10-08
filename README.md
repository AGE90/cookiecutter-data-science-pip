# Cookiecutter Data Science Template

A **Cookiecutter** template to jumpstart data science projects with a well-organized structure. This template is designed to help data scientists and machine learning practitioners create consistent and scalable project structures.

---

## Features

- **Organized Project Structure**: Predefined directories for data, notebooks, models, reports, and more.
- **Configurable**: Choose from multiple options for setting up your project (e.g., setting up virtual environmentsa and initializing a Git repo).
- **Best Practices**: Follows best practices for reproducibility, data versioning, and testing.
- **Extensible**: Customizable structure that can easily adapt to different workflows.

---

## Requirements

Before using the Cookiecutter template, ensure you have the following installed:

- **Python 3.9+**
- **[Cookiecutter Python package](https://cookiecutter.readthedocs.io/en/latest/installation.html)**

You can install the Cookiecutter package via `pip`:

```bash
pip install cookiecutter
```

---

## How to Start a New Project

1. **Navigate to the folder** where you want to create your new project.

2. **Run Cookiecutter** with the following command to generate a new project from this template:

    ```bash
    cookiecutter https://github.com/AGE90/-cookiecutter-data-science-pip
    ```

3. **Follow the prompts**: Cookiecutter will ask you a series of questions (e.g., project name, author, etc.) and create a customized project structure based on your responses.

---

## Project Structure

This template provides a well-structured project layout with the following directory structure:

```text
.
├── LICENSE
├── README.md              <- The top-level README for developers using this project.
├── CHANGELOG.md           <- A changelog to track project updates and versions.
├── pyproject.toml         <- Project configuration file (replaces setup.py and requirements.txt).
├── .gitignore             <- Specifies intentionally untracked files to ignore.
├── Makefile               <- Automate common tasks like testing, running, or setting up.
├── .env                   <- Environment variables (ignored by git).
├── .pre-commit-config.yaml <- Pre-commit hooks for linting/formatting.
├── app                    <- Main application code (if applicable).
│   └── main.py            <- Entry point for the application.
├── config                 <- Configuration files for the project.
│   ├── dev.yml            <- Development environment configuration.
│   └── prod.yml           <- Production environment configuration.
├── data
│   ├── external           <- Data from third party sources.
│   ├── interim            <- Intermediate data that has been transformed.
│   ├── processed          <- The final, canonical data sets for modeling.
│   ├── raw                <- The original, immutable data dump.
│   └── .dvc/              <- DVC meta-files for data tracking.
├── docs                   <- Project documentation.
│   ├── index.md           <- Main index or README for the documentation.
│   ├── project_structure.md    <- Project structure tree.
│   ├── install.md         <- Detailed instructions to set up this project.
│   ├── api.md             <- API documentation.
│   ├── user_guide.md      <- User guide for the project.
│   └── developer_guide.md <- Guide for developers contributing to the project.
├── logs                   <- Log files.
├── models                 <- Trained and serialized models, model predictions, or model summaries.
├── notebooks              <- Jupyter notebooks. Naming convention is a number (for ordering),
│                             the creator's initials, and a short `-` delimited description, e.g.
│                             `01-AGE90-initial_data_exploration`.
├── references             <- Data dictionaries, manuals, and all other explanatory materials.
├── reports                <- Generated analysis as HTML, PDF, LaTeX, etc.
│   └── figures            <- Generated graphics and figures to be used in reporting.
├── scripts                <- Utility scripts for project management, data processing, etc.
│   ├── data_download.sh   <- Script to download raw data.
│   └── setup_env.sh       <- Script to set up the development environment.
├── src
│   └── {{ cookiecutter.module_name }}  <- Source code for use in this project.
│       ├── __init__.py    <- Makes {{ cookiecutter.module_name }} a Python module.
│       ├── data           <- Scripts to download or generate data.
│       │   └── make_dataset.py
│       ├── features       <- Scripts to turn raw data into features for modeling.
│       │   └── build_features.py
│       ├── models         <- Scripts to train models and then use trained models to make predictions.
│       │   ├── predict_model.py
│       │   └── train_model.py
│       ├── utils          <- Scripts to help with common tasks.
│       │   └── paths.py   <- Helper functions for relative file referencing across project.
│       └── visualization  <- Scripts to create exploratory and results oriented visualizations.
│           └── visualize.py
└── tests                  <- Test files should mirror the structure of `src`.
    ├── __init__.py
    ├── conftest.py        <- Shared pytest fixtures.
    ├── e2e/               <- End-to-end or integration tests.
    └── unit/              <- Unit tests, mirroring src structure.
```

---

## Project Setup Options

### Package Configuration

- **Minimal Setup**:
  - Includes only the `ipykernel` package in `requirements.txt`.
  - Suitable for lightweight projects or when you want to manually manage dependencies.

- **Full Setup**:
  - Includes a set of data science packages in `requirements.txt`:
    - pandas: For data manipulation and analysis
    - missingno: For visualizing missing data
    - openpyxl: For reading/writing Excel files
    - matplotlib: For creating static, animated, and interactive visualizations
    - seaborn: For statistical data visualization
  - Ideal for data science projects requiring a basis set of tools.

### Virtual Environment

- **Option**: Configure a Python virtual environment for isolated dependency management.
- **If selected**:
  - Creates a virtual environment named `.venv` in the project directory.
  - Installs the project in editable mode (`pip install -e .`).
  - Installs development dependencies specified in `pyproject.toml`.
  - Installs packages listed in `requirements.txt`.
- **Benefits**:
  - Isolates project dependencies from system-wide Python packages.
  - Ensures reproducibility across different development environments.
  - Simplifies dependency management and project setup for collaborators.

### Git Repository Initialization

- **Option**: Automatically initialize a Git repository for version control.
- **If selected**:
  - Initializes a new Git repository in the project directory.
  - Creates an initial commit with all project files.
- **Benefits**:
  - Enables immediate version control for your project.
  - Facilitates collaboration and code tracking from the start.
  - Sets up a foundation for good development practices.

### Post-Setup Steps

After the project is created:

1. Activate the virtual environment (if created):

   ```bash
   source .venv/bin/activate  # On Unix or MacOS
   .venv\Scripts\activate     # On Windows
   ```

2. Verify the installation:

   ```bash
   python -m pip list
   ```

3. Start developing your project!

Remember to commit your changes regularly if you've initialized a Git repository.

---

## Contributing

Contributions are welcome! If you'd like to improve this template or add new features, feel free to submit a pull request.

1. Fork the repository.
2. Create a new branch for your feature (`git checkout -b feature/your-feature`).
3. Make your changes.
4. Submit a pull request.

---

## License

This project is licensed under the [MIT License](LICENSE).

---

## Support

If you encounter any issues or have questions, feel free to open an issue on the [GitHub repository](https://github.com/AGE90/-cookiecutter-data-science-pip/issues).

---
