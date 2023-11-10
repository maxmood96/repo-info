## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:20d3b546a9b573f27169861bd07968e5d0939d7738f65378373b258a12c9b077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:fc957c65d2150d7fd183fec1749bbe5adb538bf0dcfc6cafd92667d1a799489b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037960811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20fea01147b21c066c4a63a73c76ae02a61387390cc5515a352c4491f0472ed0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Thu, 09 Nov 2023 23:15:13 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:15:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.5/nats-server-v2.10.5-windows-amd64.zip
# Thu, 09 Nov 2023 23:15:15 GMT
ENV NATS_SERVER_SHASUM=0e07ed8f8ce2b0db0830eae0ba996f5023d8297ca043801411775555c183a964
# Thu, 09 Nov 2023 23:16:21 GMT
RUN Set-PSDebug -Trace 2
# Thu, 09 Nov 2023 23:18:01 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 09 Nov 2023 23:18:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 09 Nov 2023 23:18:03 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:18:04 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 09 Nov 2023 23:18:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b597f532bd5de48a9112abb9a71b13f9d8de9d52bbdbce1e11f9fe5a2472c641`  
		Last Modified: Thu, 09 Nov 2023 23:19:02 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ff2adbe6ec2a2587e8d4e25c48fb8c2623d5cec00758597b115e1f1f837aa1`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab0d9ece8307102c110647a0723cdc86fc1d4831a8c6e7272952d117ec8008c`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15081d252ec8cd448d61be1c1f55277085ed9d2a2795bf5bb57cb4bdedd03773`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 459.0 KB (458951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ab9f279797e45b6e0a34cc00b41b1295ae26e5baa12b643180050cfa74b180`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 5.9 MB (5898621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8754922d0f4912e6bb515690f0f752b9ae90ce8c927c56c77f0edb075a45de72`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b26c7151bd7bc6c861d6ed1a9dc1dbb53b7264b39a604f829c6e8b6105d7f0`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9dcefa248b044f2fb0c41aebcf9cb9ae7d75591edfc294272559a1cb79665f`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425508b62365bb42b7246651837150d092986710c7f6686e79f2e8d2be16c64c`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
