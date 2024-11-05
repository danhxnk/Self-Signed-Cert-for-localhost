# Self-Signed-Cert-for-localhost
## Use PowerShell to create a self signed certificate for localhost

Executing the command (on Windows) 'New-SelfSignedCertificate -DnsName "localhost" -CertStoreLocation "cert:\LocalMachine\My" -NotAfter (Get-Date).AddYears(1)' will generate a certificate for localhost that is valid for 1 year. You can amend AddYears to have an expiry of your choosing. The certificate created will be stored your computers personal store. 

Once added, you should export it and add a password. Remove the original certificate from the store and imported the exported certificate file. 

To avoid untrusted certificate errors, import the certificate file into Trusted Root.


