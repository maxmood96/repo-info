## `nats:windowsservercore`

```console
$ docker pull nats@sha256:ffd2fb1c88681df4d7256b3f8cf9a4c93b10f3c71d1d640028d78caac84949fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `nats:windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull nats@sha256:6b3d0cdc48520b0f07fd0e49717f80220817bd9d5493fc3fd48da1b9dcd1eaa1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1843284696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2afac6b75ab215d5e5d8bdd43e3e79eb1483fe051ede8f22cca4fd30bd1bdd6c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 13 Jan 2026 23:01:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 13 Jan 2026 23:01:42 GMT
ENV NATS_DOCKERIZED=1
# Tue, 13 Jan 2026 23:01:42 GMT
ENV NATS_SERVER=2.12.3
# Tue, 13 Jan 2026 23:01:43 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.3
# Tue, 13 Jan 2026 23:01:44 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.3/nats-server-v2.12.3-windows-amd64.zip
# Tue, 13 Jan 2026 23:01:45 GMT
ENV NATS_SERVER_SHASUM=33cab92d3113cc5c209773748efdd910b85db49493716b31e74df80c659b83f0
# Tue, 13 Jan 2026 23:01:52 GMT
RUN Set-PSDebug -Trace 2
# Tue, 13 Jan 2026 23:02:08 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 13 Jan 2026 23:02:08 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 13 Jan 2026 23:02:09 GMT
EXPOSE 4222 6222 8222
# Tue, 13 Jan 2026 23:02:09 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 13 Jan 2026 23:02:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:28:58 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb8d8274e62e3c5b1abaeb487f99123d4a6a52456f9f2c607ae94c0fdaf0a3f`  
		Last Modified: Tue, 13 Jan 2026 23:02:23 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88d82f88908c880064058041b57a08bcad52efa83cb81c861d4cef35fa63946`  
		Last Modified: Tue, 13 Jan 2026 23:02:23 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16563e3966482d34317a1e583bd9ef858fbf50fd83bd98a4847994f6c06a3977`  
		Last Modified: Tue, 13 Jan 2026 23:02:17 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35d78593147892e4dc1b0862f357d60da658c514d4ed6ad30a14d265e9d9aee`  
		Last Modified: Tue, 13 Jan 2026 23:02:23 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45993d2af835c94d8c57163bd6d9b5a6bc22cf03b6035373df29608c6d0b7233`  
		Last Modified: Tue, 13 Jan 2026 23:02:23 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9865315b0af55202a1c4f81edb574c7a93c4b7111d031c53265bfe5e459a757a`  
		Last Modified: Tue, 13 Jan 2026 23:02:15 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f764af314369919a82ba864a6d42705858f32863d7ba85035d85836d56635281`  
		Last Modified: Tue, 13 Jan 2026 23:02:15 GMT  
		Size: 487.4 KB (487412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3aa75ccda6866d3deaf9c0725ca2f0c49669c116be52b0bfd5413ac6dcbfe27`  
		Last Modified: Tue, 13 Jan 2026 23:02:24 GMT  
		Size: 7.1 MB (7124370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63fb7462d6d9a12c4731cbc33686dc888dcdf8f7a8e77bc9bd82b0a3421ed445`  
		Last Modified: Tue, 13 Jan 2026 23:02:23 GMT  
		Size: 1.9 KB (1888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf3851dbefeb54757d1a7ab2cb055814b7e7975a667ed77bca48e6ee3d36846`  
		Last Modified: Tue, 13 Jan 2026 23:02:14 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b2cf2bfc670b555a8d1f35418f547f057c9eb49545246fee09583d2809792c`  
		Last Modified: Tue, 13 Jan 2026 23:02:13 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6b3cef151dd4daeb69c3f714d23e7249f1434b44232997938860e2ca473cff`  
		Last Modified: Tue, 13 Jan 2026 23:02:23 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
