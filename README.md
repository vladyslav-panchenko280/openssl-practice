# openssl-practice

Interactive Jupyter notebook with hands-on OpenSSL exercises for learning cryptographic fundamentals. Master RSA key generation, message encryption/decryption, and asymmetric cryptography basics. Export to PDF, DOCX, or HTML.

## Running the Jupyter Notebook

### Prerequisites

- Python 3.x
- Jupyter Notebook

### Installation

1. Create a virtual environment:
   ```bash
   python3 -m venv .venv
   ```
   This creates an isolated Python environment for this project, preventing dependency conflicts with other projects.

2. Activate the virtual environment:
   ```bash
   source .venv/bin/activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
   This installs Jupyter and ipykernel within the virtual environment.

   Or install them individually:
   ```bash
   pip install jupyter ipykernel
   ```

## Notebook Contents

The notebook covers the following topics:

1. OpenSSL Installation - Install OpenSSL on macOS
2. RSA Key Generation - Generate 2048-bit private keys
3. Key Inspection - Examine private key components (modulus, exponents, primes)
4. Public Key Extraction - Derive public keys from private keys
5. Message Encryption - Encrypt messages using public key cryptography
6. Message Decryption - Decrypt messages using private keys
7. Verification - Validate encryption/decryption workflow

### Running the Notebook

1. Navigate to the project directory:
   ```bash
   cd /Users/vladyslav/Practice/openssl-practice
   ```

2. Activate the virtual environment (if not already active):
   ```bash
   source .venv/bin/activate
   ```

3. Start Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
   Or if the `jupyter` command is not found:
   ```bash
   python3 -m jupyter notebook
   ```
   This will start the Jupyter server and automatically open it in your default web browser at `http://localhost:8888`.

4. Open the notebook:
   Click on [openssl-practice.ipynb](openssl-practice.ipynb) to open it.

   Alternatively, you can open it directly:
   ```bash
   jupyter notebook openssl-practice.ipynb
   ```

### Stopping the Notebook

Press `Ctrl+C` in the terminal where Jupyter is running, then confirm the shutdown with `y`.

To deactivate the virtual environment when you're done:
```bash
deactivate
```

## Generating Documentation

You can export the Jupyter notebook to various formats (PDF, DOCX, HTML).

### Prerequisites

Install additional dependencies for document conversion:
```bash
pip install -r requirements.txt
brew install pandoc
playwright install chromium
```

### Generate PDF

```bash
jupyter nbconvert --to webpdf openssl-practice.ipynb
```

This creates `openssl-practice.pdf`.

### Generate DOCX

```bash
jupyter nbconvert --to html openssl-practice.ipynb
pandoc openssl-practice.html -o openssl-practice.docx
```

This creates `openssl-practice.docx`.

### Generate HTML

```bash
jupyter nbconvert --to html openssl-practice.ipynb
```

This creates `openssl-practice.html`.
