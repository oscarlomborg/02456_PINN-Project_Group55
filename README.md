# Getting Started

This guide explains how to download this GitHub project, open it in Visual Studio Code (VS Code), and create its Conda environment using `dlenv.yml`.

## Prerequisites

Install the following before you begin:

- [Git](https://git-scm.com/downloads)
- [Visual Studio Code](https://code.visualstudio.com/)
- [Miniconda](https://www.anaconda.com/docs/getting-started/miniconda/main) or [Anaconda](https://www.anaconda.com/download)

Verify that Git and Conda are installed by running:

```bash
git --version
conda --version
```

If `conda` is not recognized, open an Anaconda Prompt (Windows) or initialize Conda in your terminal.

## 1. Clone the GitHub repository

1. Open this repository on GitHub.
2. Click the green **Code** button and copy the **HTTPS** URL.
3. Open VS Code.
4. Open the Command Palette with **Ctrl+Shift+P** (Windows/Linux) or **Cmd+Shift+P** (macOS).
5. Search for and select **Git: Clone**.
6. Paste the repository URL and choose where to save the folder on your computer.
7. When prompted, select **Open** to open the cloned project in VS Code.

**Alternative — use the terminal:**

```bash
git clone https://github.com/USERNAME/REPOSITORY.git
cd REPOSITORY
code .
```

Replace `USERNAME` and `REPOSITORY` with the values from the GitHub URL. If `code .` does not work, open the cloned folder through **File → Open Folder** in VS Code.

## 2. Create the Conda environment

In VS Code, open **Terminal → New Terminal**. Make sure the terminal is in the project folder containing `dlenv.yml`, then run:

```bash
conda env create -f dlenv.yml
```

Conda will create an environment and install the dependencies listed in `dlenv.yml`. This may take a few minutes.

Find the environment name by opening `dlenv.yml` and checking the `name:` field, for example:

```yaml
name: dlenv
```

Activate the environment using that name:

```bash
conda activate dlenv
```

> If the `name:` field is different, replace `dlenv` with the actual name.

You can confirm that the environment exists by running:

```bash
conda env list
```

## 3. Select the environment in VS Code

1. Install the **Python** extension by Microsoft in VS Code if you have not already.
2. Open the Command Palette (**Ctrl+Shift+P** or **Cmd+Shift+P**).
3. Select **Python: Select Interpreter**.
4. Choose the Python interpreter belonging to the Conda environment you just created.

VS Code will then use that environment for Python files and notebooks when the corresponding interpreter/kernel is selected.

## 4. Work on the project later

When reopening the project:

```bash
conda activate dlenv
```

If the dependencies in `dlenv.yml` change, update your environment with:

```bash
conda env update -f dlenv.yml --prune
```

To leave the environment:

```bash
conda deactivate
```

## Troubleshooting

- **`conda: command not found`:** Try Anaconda Prompt (Windows) or configure Conda for your shell using `conda init` and restart the terminal.
- **`EnvironmentFileNotFound`:** Make sure you are in the repository folder and that the file is named exactly `dlenv.yml`.
- **Environment not visible in VS Code:** Restart VS Code or use **Python: Select Interpreter** to locate it manually.
