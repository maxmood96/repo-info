## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:f701716476a8d968bd766320239d98d7f973ebaaa7a6f960f65648bda132229e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2-windowsservercore` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:2c61006c6743420a33c3ade658d600d9b81f09a86df8c44fe02741a71d196d7f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2140052973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782541001e22820de00703de294e85e7c622fc9ea85c9030e8fda96177afa0cb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Mon, 29 Jun 2026 19:16:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 29 Jun 2026 19:16:31 GMT
ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 19:16:32 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:16:33 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:16:35 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.3/nats-server-v2.14.3-windows-amd64.zip
# Mon, 29 Jun 2026 19:16:37 GMT
ENV NATS_SERVER_SHASUM=94e338d742761272e31eab1efb1f767eac3a2e56e4c05a7933c65a73fe95a27b
# Mon, 29 Jun 2026 19:17:35 GMT
RUN Set-PSDebug -Trace 2
# Mon, 29 Jun 2026 19:18:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 29 Jun 2026 19:18:06 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 19:18:08 GMT
EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 19:18:09 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 19:18:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac87f215828b12e2044c46470b221ea4307d0fc11cf8280e12474587a59317d`  
		Last Modified: Mon, 29 Jun 2026 19:18:18 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff6f7da74f9e652f79bc8278319981b268148b1548a3ef4220d3ccbe4b5473d`  
		Last Modified: Mon, 29 Jun 2026 19:18:18 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e85164857353b52ed850cc83049bc199678edaed484f95d1e38aa0a4f1b525b`  
		Last Modified: Mon, 29 Jun 2026 19:18:18 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706cc542b32b6c088b1b95499c39a0c6f9dbe749f47087a0cd668545100147ba`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25bcf16bfd2387cc38d31f75eeac32290dada9d452e1f50b902530775f1c0ff`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64aecb5ee131c5c835ec5c73c2ad224bf1e9c3ede99efeca9eec6a270f5c22b1`  
		Last Modified: Mon, 29 Jun 2026 19:18:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2f1b98897859ea619b08dd0f0db49b009771052a13d263d4980a21c40901f2`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 496.7 KB (496723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784da3b63359a7bbb87eb47bb8a637b409b418e94af977bf3c24722cbc2ec89e`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 7.4 MB (7417113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae24643aacc8edba76b5661a3358a9461f9fda9a7d1f0fccaeca461dfb074a23`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe52ddb42630f70fd61331adf5e83118d27382c4d3922882adb2d981105bac94`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087e85133498df0eb7d45b8bc9353ec3fa1fc98964b2f88c33152ca73bf5abd6`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9462b672f1e05436ba0020f6b3b71b8db8b844d5c5183c1088c29d06d39df1be`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
