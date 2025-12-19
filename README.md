## Setup (with uv)

1. Setup:
   ```sh
   uv venv .venv
   uv sync
   .venv\Scripts\Activate.ps1  # On Windows PowerShell
   # Or, for cmd: .venv\Scripts\activate.bat
   # Or, for bash: source .venv/bin/activate
   ```

## Running

- To train and log models:
  ```sh
  uv pip install .  # (if running as a package, otherwise skip)
  python train_model.py
  ```
- To launch the MLflow UI:
  ```sh
  mlflow ui --backend-store-uri ./mlruns --port 5000
  # Then open http://localhost:5000 in your browser
  ```

## Notes
- All dependencies are managed via `pyproject.toml`.
- No requirements.txt or environment.yml is needed.
- Use `uv` for all dependency management and environment setup.
