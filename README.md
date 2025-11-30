# Anomaly detection

## Description

## **Table of Contents**
- [Installation](#installation)
- [License](#license)


## **Installation**

### Initial Installation

Clone the repository and install dependencies:

```bash
git clone git@github.com:miahro/anomaly.git
cd anomaly
```

1. Pull the latest version of the repo:
```bash
git pull origin main
```

2. Create and activate the Conda environment:
```bash
conda create -n anomaly python=3.10
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

## **License**
This project is released under the MIT License. See `LICENSE` for details.

[LICENSE](LICENSE)