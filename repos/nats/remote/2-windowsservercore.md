## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:721cd8da25a86823d56344291d85d05ce9b5c40ae006912e9463677f56076b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `nats:2-windowsservercore` - windows version 10.0.20348.3807; amd64

```console
$ docker pull nats@sha256:5b1ac53cf8d84ac4f1990a8f1dfa6d2d56088985b67fab505db885d99b751d27
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2287448985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8955133c3423b09ccde2ff623bc49ace5dea7f49ba767552e01d5e66156f6cb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Tue, 10 Jun 2025 21:28:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Jun 2025 21:28:35 GMT
ENV NATS_DOCKERIZED=1
# Tue, 10 Jun 2025 21:28:36 GMT
ENV NATS_SERVER=2.11.4
# Tue, 10 Jun 2025 21:28:37 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.4/nats-server-v2.11.4-windows-amd64.zip
# Tue, 10 Jun 2025 21:28:38 GMT
ENV NATS_SERVER_SHASUM=c78771905c52a8590f6c20cb101bb38ab65bd3046bd6ab8edf4e38efd41dce6f
# Tue, 10 Jun 2025 21:28:47 GMT
RUN Set-PSDebug -Trace 2
# Tue, 10 Jun 2025 21:29:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 10 Jun 2025 21:29:05 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 10 Jun 2025 21:29:05 GMT
EXPOSE 4222 6222 8222
# Tue, 10 Jun 2025 21:29:06 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Jun 2025 21:29:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e1ced6fb764fa5a38c516afb40a7008714fde114ef105e7088e410ccce69db`  
		Last Modified: Tue, 10 Jun 2025 22:08:23 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b46ecde7c274cae88562245589dff9d175718cffbe135c9105e6480764cb9a1`  
		Last Modified: Tue, 10 Jun 2025 22:08:23 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7202529d281af14d8248f83052f2a91ceda3b2f7d0e2c5b917c0acfd81ee7e6e`  
		Last Modified: Tue, 10 Jun 2025 22:08:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeaaf4ea7efbf0e0900e2ff8f49bf8fe3dd8e6ce602fca404acf2d7f36fb10e0`  
		Last Modified: Tue, 10 Jun 2025 22:08:24 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201ea7bea6448cfa5b2fc222d1bf6490669c98275f65db37a106d24331533175`  
		Last Modified: Tue, 10 Jun 2025 22:08:24 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef85e0bd1c5e3ccb5aefddc045b1c575eed7c918a5d6715a3ea9410cb8d176fc`  
		Last Modified: Tue, 10 Jun 2025 22:08:24 GMT  
		Size: 343.1 KB (343095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ec3e2367286b9e494ea4c95006b982c94d0520e11990ab45b77a1e113b87ca`  
		Last Modified: Tue, 10 Jun 2025 22:08:25 GMT  
		Size: 6.8 MB (6842086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5594090af04d7ee120840ee0d40feac93f57d746e81422d643dd67408023db0e`  
		Last Modified: Tue, 10 Jun 2025 22:08:25 GMT  
		Size: 1.9 KB (1865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b4de5f57e5a8ca64ec8f1d3650aba948db2a90000a730c869e5c2b332c01ca`  
		Last Modified: Tue, 10 Jun 2025 22:08:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d31ae85223afc98fdbe9de819943ac6559345ae284b366067a1b3e1cbceb6a`  
		Last Modified: Tue, 10 Jun 2025 22:08:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:919864ab6b2d56813b397245948b2c37b529feacc653a877e65198ef3e9c3dd4`  
		Last Modified: Tue, 10 Jun 2025 22:08:26 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
