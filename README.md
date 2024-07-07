[Hello.txt](https://github.com/user-attachments/files/15522935/Hello.txt)
pip install boto3
import boto3

def list_kms_aliases():
    # Create a KMS client
    kms_client = boto3.client('kms')

    # List aliases
    response = kms_client.list_aliases()

    # Print aliases
    for alias in response['Aliases']:
        alias_name = alias.get('AliasName', 'No Alias')
        key_id = alias.get('TargetKey
