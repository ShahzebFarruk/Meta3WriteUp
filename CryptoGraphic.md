## CryptoGraphic.md
### Command to verify the MD5 of a file on Windows 10: Verify after downloading this file from [Nessus](https://www.tenable.com/downloads/tenable-appliance?loginAttempted=true#tenablecore-nessus).
MD5:
```
CertUtil -hashfile Tenable-Core-Nessus-20230417.ova Md5
```
SHA-256:
```
CertUtil -hashfile Tenable-Core-Nessus-20230417.ova SHA256
```

On Linux:
```
sha256 <expected-sha-256-sum> <name-of-the-file>
```
