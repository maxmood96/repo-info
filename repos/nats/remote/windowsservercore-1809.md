## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:3002e35b4bb91080eac08408891e6bb9155d38086cbb6fcfb654b61e0d2383e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:9f3868f133ddd1a10ac71bbe835764e9d60e9b00081851a00ca05cd3362ea5d1
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2484142070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be425426bfa101eb4fdc6741eccbeaddde31c6c0761a665b4654dea39a17279`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 13:10:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Apr 2021 16:02:50 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 16:02:51 GMT
ENV NATS_SERVER=2.2.1
# Wed, 14 Apr 2021 16:02:52 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.2.1/nats-server-v2.2.1-windows-amd64.zip
# Wed, 14 Apr 2021 16:02:53 GMT
ENV GIT_DOWNLOAD_SHA256=1f0d48a7ba9200e2572016a9f3e1ec7e630f0518cc0b40950c14ff3a5d900924
# Wed, 14 Apr 2021 16:03:32 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Apr 2021 16:04:53 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Apr 2021 16:04:55 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Apr 2021 16:04:56 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Apr 2021 16:04:57 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Apr 2021 16:04:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2159a5d0f75ce11e6fe71e4260ede5c3c88a9eb76a0ff43ac6746b2b9b96775`  
		Last Modified: Wed, 14 Apr 2021 15:37:10 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e849354f21f856ec720d6daecc37978fd7246f376ba3c32fd63d4400cce357bc`  
		Last Modified: Wed, 14 Apr 2021 16:10:16 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daae5ee02f484d7c054ad550cbee6900a35477f4e23e322cc3af6eb7c4690416`  
		Last Modified: Wed, 14 Apr 2021 16:10:14 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4df8575d5fc511a7ac278cfc55a4053b36afce4c0bcae2af0af7907c7f91e6`  
		Last Modified: Wed, 14 Apr 2021 16:10:14 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570a7e5edba00d92281a4a147639b5fc0b6724693cbfed80007b5b5db612a3e8`  
		Last Modified: Wed, 14 Apr 2021 16:10:13 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60092b7b0679ad17236eb09b832adcc7bb67a5fd8c2d9a69ffbfc863716274c2`  
		Last Modified: Wed, 14 Apr 2021 16:10:15 GMT  
		Size: 5.1 MB (5072726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5d3b99689d155ccd6cdf6acbc7ef61472c65ce2cee49f441c4c3b844242410`  
		Last Modified: Wed, 14 Apr 2021 16:10:13 GMT  
		Size: 9.3 MB (9302175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dae780c7132cf39c97d1602e11b6a58481594df6d896054f3a9e6e9f54e63a`  
		Last Modified: Wed, 14 Apr 2021 16:10:10 GMT  
		Size: 2.0 KB (1957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f2291e14ae4d6e97942f3284122a80c7c969cb9bcfc9a417a833439505f85d`  
		Last Modified: Wed, 14 Apr 2021 16:10:11 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b07be56d63a82b0606023df13bf32a522a13a12a44c53116ec24d0c1bd2ca1`  
		Last Modified: Wed, 14 Apr 2021 16:10:11 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6cc0327d5edba60d3e99a97fa6c015e1953c9451bc816f20d6d73a67b9e426`  
		Last Modified: Wed, 14 Apr 2021 16:10:11 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
