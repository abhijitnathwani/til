# Replace `\n` character with actual newline

`sed -i 's/\\n/\n/g' input_filename`

This comes when handy when we are processing/writing files based on some strings. This was particularly useful when I had to store a certificate string I got in an API to a file.

Response string:

```
-----BEGIN CERTIFICATE-----\nMIIDWTCCAkGgAwIBAgIUWudjVKBQgUiASXzNR2RSWrtEGogwDQYJKoZIhvcNAQEL\nBQAwTTFLMEkGA1UECwxCQW1hem9uIFdlYiBTZXJ2aWNlcyBPPUFtYXpvbi5jb20g\nSW5jLiBMPVNlYXR0bGUgU1Q9V2FzaGluZ3RvbiBDPVVTMB4XDTIwMDYwMjEyMzk0<somerandomcertificatecontents>\nDJ12Vdq4Y5nFMi4ZbmtvJBsEiQoRawhKSIjHjOGYG5ZHu/iM3lxmZqTR5BPt\n-----END CERTIFICATE-----\n
```

Actual to be stored:

```
-----BEGIN CERTIFICATE-----
MIIDWTCCAkGgAwIBAgIUWudjVKBQgUiASXzNR2RSWrtEGogwDQYJKoZIhvcNAQEL
BQAwTTFLMEkGA1UECwxCQW1hem9uIFdlYiBTZXJ2aWNlcyBPPUFtYXpvbi5jb20g
SW5jLiBMPVNlYXR0bGUgU1Q9V2FzaGluZ3RvbiBDPVVTMB4XDTIwMDYwMjEyMzk0
<somerandomcertificatecontents>
DJ12Vdq4Y5nFMi4ZbmtvJBsEiQoRawhKSIjHjOGYG5ZHu/iM3lxmZqTR5BPt
----END CERTIFICATE-----
```
