# Anomaly detection

## Description

## **Table of Contents**
- [Installation](#installation)
- [License](#license)


## **Installation**

### Initial Installation

1. Clone the repository and install dependencies:

```bash
git clone git@github.com:miahro/anomaly.git
cd anomaly
```


2. Create and activate the Conda environment:
```bash
conda env create -f environment.yml
conda activate anomaly
```

### Installing Updated Dependencies

To update the environment based on `environment.yml`:

```bash
conda env update --file environment.yml --prune
```

---

### **Installing New Packages to Conda Environment**

1. Make sure the `anomaly` environment is active:
```bash
conda activate anomaly
```

2. Install the new package:
```bash
conda install <library-name>
```

3. After installation, update `environment.yml`:
```bash
conda env export --no-builds | grep -v "^prefix:" > environment.yml
```

4. Commit and push the updated `environment.yml`:
```bash
git add environment.yml
git commit -m "Update Conda environment"
git push origin main
```

### Notes on conda vs pip

The environment is managed primarily with `conda` (using the `conda-forge` channel).
Some packages that are not available on conda (e.g. `fmiopendata`) are installed via `pip` **inside** the `anomaly` environment.

To ensure `pip` installs into the active conda environment, this project uses:

```bash
conda activate anomaly
python -m pip install <package>


## **License**
This project is released under the MIT License. See `LICENSE` for details.

[LICENSE](LICENSE)