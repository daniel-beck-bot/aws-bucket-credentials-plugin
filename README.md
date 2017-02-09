#This is a jenkins plugin to retrieve encrypted credentials from an Amazon S3 bucket that is encrypted with KMS

##The variables are:
| variable | description | required |
|----------|-------------|----------|
|username | the username to use with these credentials | yes |
|region | the region to use for aws | no | 
|bucketName| the name of the bucket in s3 | yes |
|bucketPath| the object id within the bucket where the encrypted value where the cipher text should be read from | yes |
|isS3Proxy | use the proxy when doing s3 requests | no - default to off|
|EncryptionContextKey | if you set any context when encrypting the secret, set the key here | no |
|EncryptionValue | the value to use along with the encryption context key| no |
|isKmsProxy | use the proxy when doing kms requests | no - defaults to off|
|proxyHost | the proxy host name (no protocol) | no - used with proxy |
|proxyPort | the proxy port number | no - used with proxy |

KMS is used to decrypt the cipher text
You can optionally provide a context key and value within the script if you used this to encrypt with.
