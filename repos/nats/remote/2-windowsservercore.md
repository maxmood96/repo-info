## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:5b3e38cc7df1ccd71cb1357b316228b34861c6c37727ca7ffd148b73e64b321b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:fc57a2fbc1740965db1c40c59291ef89a6d9f5f235b4d963f4d0602ae0666443
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2186249989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b64d1c4d9a958ede215514048d16b164a246beedd0c21e6c59ff3d07f069867`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:05:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_DOCKERIZED=1
# Tue, 21 May 2024 23:14:46 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:14:47 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.16/nats-server-v2.10.16-windows-amd64.zip
# Tue, 21 May 2024 23:14:48 GMT
ENV NATS_SERVER_SHASUM=22a5ef3a54200ebdebaa325822f477c89dc6533ec6fc1f531d897aa876517ccf
# Tue, 21 May 2024 23:15:38 GMT
RUN Set-PSDebug -Trace 2
# Tue, 21 May 2024 23:16:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 21 May 2024 23:16:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 21 May 2024 23:16:58 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:16:58 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 21 May 2024 23:16:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7274f776737e98439583e21fd0c4ff8dedfa0009226d44af30e91a144f1d44b`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ffc0e64d2024463ed60d3672fe6067839e3b23d912046685d28053bccb8997`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d075cbe94bdd5f06bdabff0ae1baa13ad48a75f808800d9c9cf7d554470d866`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a88d0da7a6579af9c2bdff927235dee0c94b1bfc1cec3787d05218c6a55ec3c`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f922389c5664c8e701d97ef08d1cc52e256e6002e475dacd84e45e12ccaf8cc0`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096dd602404c378351787720a7178c38038189543894dcbe1ce4b5260124b8af`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 445.9 KB (445881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1bad7b47779f08ea37f050914a7169eb3be6ad32530159df515b046af95396`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 6.1 MB (6079688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c3b9fbec461537454b31d72f007b18f9d7d0449481a6532b4bc0465145b360`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93647e59b4740ef7e3e440c385dfc114fbae9e7fa990db167023a7040f182a11`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445badc8d13b259ba8343872927775698cdbb81b6013fa153680a9052fea5330`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da65ffc80b4f6a0ef8841c9d2e497145d917917587c49470ad4ca54c6cf78de`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
