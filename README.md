# Github Action - dotenv-vault-action
## Description
This action allows you to download `.env` files from [dotenv-vault](https://www.dotenv.org/) and use them in your workflow.

## Usage
```yaml
- name: Download .env file
  uses: zdeneklapes/dotenv-vault-action@v1
  with:
    dotenvMe: ${{ secrets.DOTENV_ME }}
    stage: "ci"
    move: true
```

## Inputs
### `dotenvMe` (required)
- **Description**: The `dotenvMe` secret from [dotenv-vault](https://www.dotenv.org/).

### `stage` (optional, default: 'ci')
The stage of the `.env` file you want to download. 

**Examples**: `ci`/`staging`/`production`/`development` or any other stage you have set up in dotenv-vault.

### `move` (optional, default: true)
If set to `false`, the `.env` file will be moved to the root of your repository. 
