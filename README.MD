# Secret Manager Env Injector

- ## [Getting Started](#getting-started)
    * [Prerequiste](#prerequiste)
    * [Installation](#installation)
    * [Examples](#example)
        * [Key Types](#key-type)
- ## [Available Methods](#available-methods)

- ### Prerequisites
    - Python >= 3.6.x
    - pip

- ### Installation
    ```
    $ pip install secret-manager-env-injector
    ```

- ### Examples
    - Using the Injector decorator
    ```
    # import the decorator
    from SecretManagerEnvInjector import injector
    
    # it will inject the secret in the environment with the name provided or the secret name in finds in the arn 
    @inject('arn:aws:secretsmanager:us-xxxx-1:xxxxxxxxxxxx:secret:xxxxxxxx-xxxxxxx', region='us-east-1', custom_secret_name='my-secret')
    def test():
        print("hello world")
    test()

    ```

### Available Methods

- JSONParser

| Method | Params | type | default | Description 
| --- | --- | --- | --- | --- |
| inject | arn | str | NA | ARN of the secret that needs to be extarcted
| inject | region | str | 'us-east-1' | select the AWS region
| inject | custom_secret_name | str | None | select the name with which you want the secret to be stored

### Note:
 - The package is under development and will be prone to more frequent updates