## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:7be687bd0fcf28c0ff569af5d07b5586400ddc2e656ed5059fa069a1861d5310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2-windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:513908e15de358856596ba7150e84b831f6f711b57c69bff1dab9e0f2334ccc1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077910518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5993871186ecfe774a9cf8a2b3de0621e6afaf3fd93f99cbbaff6fffc782a8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 28 Apr 2026 00:22:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 28 Apr 2026 00:22:20 GMT
ENV NATS_DOCKERIZED=1
# Tue, 28 Apr 2026 00:22:21 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:22:22 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:22:23 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.8/nats-server-v2.12.8-windows-amd64.zip
# Tue, 28 Apr 2026 00:22:24 GMT
ENV NATS_SERVER_SHASUM=61836ff8d0cecbb773faf7daa22f5212b7ed3ab5a0c58c12b013d67d64edd6cc
# Tue, 28 Apr 2026 00:23:39 GMT
RUN Set-PSDebug -Trace 2
# Tue, 28 Apr 2026 00:24:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 28 Apr 2026 00:24:04 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 28 Apr 2026 00:24:05 GMT
EXPOSE 4222 6222 8222
# Tue, 28 Apr 2026 00:24:05 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 28 Apr 2026 00:24:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06ffdad23a2259ee9605b07af3b8756afac669d72d7f4df289af5e1bfa765df`  
		Last Modified: Tue, 28 Apr 2026 00:24:14 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349750824325190c58f7211d2a32fac8867324987e4912f6187dc9d6f9fb4ae8`  
		Last Modified: Tue, 28 Apr 2026 00:24:14 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e65ce208cc089d5d84714aa1b4c702e6514a37bc1a25a9e317e5484c4b6770`  
		Last Modified: Tue, 28 Apr 2026 00:24:13 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fefac29241015b39520060d922c7fb6054787dd9dd417b2cabd03743d7bda5f`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe557d93a73db69714369a258c20de37e40d04268b2f4804c92e12e16976bdd`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3130aba43c6a9d55589835a86638de2d3125fa2366b684015a8ac9fc1c818d`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d19f58f4c90bd0a1c10a151c0165e6d1660f82cb62c97e4a3e1ec5be69c14d0`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 507.2 KB (507220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b029516bfa850bb0dc8d626d1e3a9cda785c0b6ff3e1ac8797afb2adf5f0ed3`  
		Last Modified: Tue, 28 Apr 2026 00:24:15 GMT  
		Size: 7.2 MB (7178445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e8a07055de8fc46e4e8f02f1a81c1872033e0a3dda665ba7f3a7cdba7cd203`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2e16a4341e7b5618098955dbd5110c7fc4e24810d6e25bb7cd53e768b4539`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5a737b9ff5aae65f741d22ddd5e6e1c210d6f45528f4778fcb53b923c0e903`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdbeaf674140e140a6e0cb9b0b83df4612f9ab45bc55e9507b8d32bb2be05e1`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
