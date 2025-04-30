# How to Run `python portal.py` from Scratch

Follow these steps to set up your environment and run `portal.py`:

1. **Create a new conda environment with Python 3.10.16:**
   ```bash
   conda create --name hgot python=3.10.16
   ```

2. **Activate the environment:**
   ```bash
   conda activate hgot
   ```

3. **Install required Python packages:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Create necessary directories for logs:**
   ```bash
   mkdir -p log/temp
   ```

5. **Prepare the environment variables:**
   Make a copy of `.env_template` and rename it to `.env`:
   ```bash
   cp .env_template .env
   ```
   Edit `.env` as needed for your configuration.

6. **Run the portal:**
   ```bash
   python portal.py
   ```

---

## About `config/config.json`

The file `config/config.json` contains important configuration settings for the portal. Here is an example:

```json
{
    "rm": "google",
    "lm": "gpt-3.5-turbo-1106",
    "lm_max_tokens": 300
}
```

- `rm`: The retrieval model to use (e.g., `google`).
- `lm`: The language model for generating responses (e.g., `gpt-3.5-turbo-1106`).
- `lm_max_tokens`: The maximum number of tokens the language model can generate in a single response (e.g., `300`).

You can edit these values in `config/config.json` to customize the portal’s behavior. After making changes, restart the portal to apply the new settings.

