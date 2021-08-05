## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:7bc91025d330e69dbd5130de2ef309126249f780ecb8d3951b7c6dc27118b8b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.2061; amd64

```console
$ docker pull nats@sha256:9e2d731cdb925c898d4579320d72701d2ac4fe6364d4eb2bca58ed40532cc2a5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2690732563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce9dae20e0206a3c75271c45ca7b3b6ae85b1fddbbac124fe498e4597d1fa65`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 06 Jul 2021 20:34:18 GMT
RUN Install update 1809-amd64
# Wed, 14 Jul 2021 01:07:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jul 2021 02:31:26 GMT
ENV NATS_DOCKERIZED=1
# Thu, 05 Aug 2021 01:14:25 GMT
ENV NATS_SERVER=2.3.4
# Thu, 05 Aug 2021 01:14:27 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.4/nats-server-v2.3.4-windows-amd64.zip
# Thu, 05 Aug 2021 01:14:29 GMT
ENV NATS_SERVER_SHASUM=729dc0609e0461aa5fb893c85c04c6b6afa40945183d8d8324d03186d1678a99
# Thu, 05 Aug 2021 01:15:28 GMT
RUN Set-PSDebug -Trace 2
# Thu, 05 Aug 2021 01:16:45 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 05 Aug 2021 01:16:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 05 Aug 2021 01:16:50 GMT
EXPOSE 4222 6222 8222
# Thu, 05 Aug 2021 01:16:52 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 05 Aug 2021 01:16:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f143c6fed32d477c35b660b2e108ea62e3593c03e44bd9ced208ce52b26b0841`  
		Size: 967.1 MB (967113907 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:adcec6ff907307155c0652222cc9b95a0cc964d4c371e02767e72a5c90472192`  
		Last Modified: Wed, 14 Jul 2021 02:02:19 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92bdc410321db22d4cf09322869bd9fb2495788c3725624c86d76a6ab3d95d3`  
		Last Modified: Wed, 14 Jul 2021 02:40:16 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5979713f8e1f662fa1588049500ad9a02d8f21edadb4270f498e66188c7f098b`  
		Last Modified: Thu, 05 Aug 2021 01:20:46 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbce67e3f27ea6f2ced1a18b80f76be1d1d9f4a3360eacf9b682f76e22ce70bd`  
		Last Modified: Thu, 05 Aug 2021 01:20:46 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a38cc6410be930a503a8d84a6c5179fc77d4f264b575a6b8ed9dba8652130448`  
		Last Modified: Thu, 05 Aug 2021 01:20:46 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bf5b9d1c9be32f37073b8570c4f5425741bf087b26830f109cf1da7548b2d4`  
		Last Modified: Thu, 05 Aug 2021 01:20:46 GMT  
		Size: 364.0 KB (363963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3630752cfb4d0af660aec8e61449bdee0768f832622c426e164c52310feb34ea`  
		Last Modified: Thu, 05 Aug 2021 01:20:49 GMT  
		Size: 4.9 MB (4908534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974b95416575ac8447156b16b48dbc2c1075da313fb92b34649907cfa9e64f6d`  
		Last Modified: Thu, 05 Aug 2021 01:20:43 GMT  
		Size: 1.9 KB (1946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732a55fe045a7122347b15fe0ffeb6f778d44005ba9fd8895a5742b53a3b45e3`  
		Last Modified: Thu, 05 Aug 2021 01:20:43 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750ae0f00a0b9b06b5540e999091d41c325666fe51da95ef04aac1a4677dccf1`  
		Last Modified: Thu, 05 Aug 2021 01:20:43 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3420ec40c0c7e96c3c2c8c8e4eb016f945ebe02a4471a1acad0d1b870447ba3e`  
		Last Modified: Thu, 05 Aug 2021 01:20:43 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
