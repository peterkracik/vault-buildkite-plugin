# Vault Secrets to Environment Variables Buildkite Plugin

Exports secrets from Vault as environment variables during a build.

## Example

Add the following to your `pipeline.yml`:

```yml
steps:
  - command: ls
    plugins:
      - parkside-it/vault-buildkite-plugin#v1.0.0:
          secret_name: 'my_secret'

Configuration 
`secret_name` (Required, string)
The name of the secret in Vault that you want to export as environment variables.
`VAULT_FORMAT` (Optional, string)
Set the format used by Vault. The default format is `"json"`.

Developing
To run the tests:
docker-compose run --rm tests
Contributing
	1.	Fork the repo
	2.	Make the changes
	3.	Run the tests
	4.	Commit and push your changes
	5.	Send a pull request
Please ensure to manage and protect your logs as this plugin will echo the names of your secrets for debugging purposes. Make sure these logs are appropriately secured and never display the actual secret values.
