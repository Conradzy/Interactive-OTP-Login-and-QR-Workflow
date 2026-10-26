# Interactive OTP Login and QR-Code Workflow

Implements an input-driven registration and login sequence inside a notebook. Credentials are stored in SQLite, a TOTP secret is enrolled through a QR code, and a protected API action becomes available after login.

## Workflow

1. Initialize the SQLite users table.
2. Prompt for registration information.
3. Generate a TOTP enrollment QR code.
4. Prompt for username, password, and current OTP.
5. After authentication, retrieve a joke and generate its QR code.

## Data Requirements

- No external dataset is required; `users.db` is created at runtime.
- The notebook calls the Official Joke API.

Datasets and generated artifacts are not included unless they are embedded directly in the notebook.

## Requirements

- pyotp
- qrcode
- Pillow
- requests
- SQLite (Python standard library)
- IPython

Install missing packages in your Jupyter or Google Colab environment before running the notebook.

## Running the Notebook

1. Open [`LoginOTPSQLite_QRCode_API_InputFlow.ipynb`](LoginOTPSQLite_QRCode_API_InputFlow.ipynb) in Jupyter Notebook or Google Colab.
2. Place any required data files in the path expected by the notebook.
3. Update local or Google Drive paths where needed.
4. Run the cells from top to bottom.

## Outputs

- Runtime SQLite database
- Authenticator QR image
- Protected joke QR image

## Security and Responsible Use

This educational example stores passwords in plaintext and displays database rows. Use password hashing, secret protection, and a proper session system in real applications. Embedded outputs were removed from the public copy.

## Repository Contents

```text
.
|-- README.md
`-- LoginOTPSQLite_QRCode_API_InputFlow.ipynb
```

## Notes

- This repository preserves the analysis as a notebook-first educational project.
- Results may vary with dataset versions, random splits, package versions, and available hardware.
- Review file paths and runtime-specific commands before executing outside Google Colab.
