# omnivoreimport
Used to import omnivore export archives into another instance using the GraphQL API

Currently doesn't support:
- importing PDFs. If your JSON file contains the url for the PDF it will try to add it that way, but it will not upload PDF files directly from your archive, because I don't think you can do that via the API.

## Usage
    usage: importer.py [-h] --api-key API_KEY [--api-url API_URL] --folder FOLDER
    
    Import articles and highlights into Omnivore
    
    options:
      -h, --help              show this help message and exit
      --api-key API_KEY       Omnivore API key from instance you will be importing to (found at /settings/api)
      --api-url API_URL       Omnivore API endpoint (default: https://api-prod.omnivore.app/api/graphql)
      --folder FOLDER         Path to folder containing contents of extracted archive
      --ignore-invalid-certs  Bypass validating TLS/SSL certificates during API calls
