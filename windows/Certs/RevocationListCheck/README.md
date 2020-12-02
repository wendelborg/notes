## Certificate file verification
certutil -f -urlfetch -verify <filename>.cer


## Revocation list check
Powershell:

cd CERT:\
$cert = get-childitem -Path '<thumbprint>' -Recurse
Test-Certificate -Cert $cert


