## `nats:windowsservercore`

```console
$ docker pull nats@sha256:a6c1153fd919a539581471edd798478057cef10a6347e770d03336a20d5e472b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `nats:windowsservercore` - windows version 10.0.17763.1879; amd64

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

### `nats:windowsservercore` - windows version 10.0.14393.4350; amd64

```console
$ docker pull nats@sha256:ad5ac25aa423d2df82324037dd73fec641098cd5f198cf98ccf19f4ae640d1f5
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5814950471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc9b58b0a6e7d867ee74a6023bf1768d2dad684760ace428c0bf425357fcc5c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 13:22:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Apr 2021 16:05:33 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 16:05:33 GMT
ENV NATS_SERVER=2.2.1
# Wed, 14 Apr 2021 16:05:35 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.2.1/nats-server-v2.2.1-windows-amd64.zip
# Wed, 14 Apr 2021 16:05:35 GMT
ENV GIT_DOWNLOAD_SHA256=1f0d48a7ba9200e2572016a9f3e1ec7e630f0518cc0b40950c14ff3a5d900924
# Wed, 14 Apr 2021 16:06:59 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Apr 2021 16:09:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Apr 2021 16:09:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Apr 2021 16:09:20 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Apr 2021 16:09:21 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Apr 2021 16:09:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f616bb7876e6f944d82fa1802ffab5ca4931a63e1b999f0851b52120cda83539`  
		Last Modified: Wed, 14 Apr 2021 15:37:43 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfa54f43457753c391f21da5e9a5bf47c61c574c0da04b8614d0e84bf823f54`  
		Last Modified: Wed, 14 Apr 2021 16:11:03 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d71ba1c574073f9d5dd016585c2fe26ac560c192f7aa36ce54d4c12832997f`  
		Last Modified: Wed, 14 Apr 2021 16:11:01 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9f66539738348100cf9f1e6a5bc40e8c2123bafb9329f5df3cf20a2015db33`  
		Last Modified: Wed, 14 Apr 2021 16:11:00 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f2eae922462b2537c1d0d32d548cb10190f6bda0d02da57440cc229da692b3`  
		Last Modified: Wed, 14 Apr 2021 16:11:00 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea168f84532f340be87f19704511ee160cbdc5b9c6ad8962fcd80e9fb8efea7`  
		Last Modified: Wed, 14 Apr 2021 16:11:01 GMT  
		Size: 5.7 MB (5651953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eda2d9556eb5afaf10e6300ac36ddc1383144ae65671ca3a01b24bac150c540`  
		Last Modified: Wed, 14 Apr 2021 16:11:01 GMT  
		Size: 14.4 MB (14401439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a04b0d9d602bb1f9c6fb7925bb92959ebcff2c30e6ca6a658cdd9976d662d70`  
		Last Modified: Wed, 14 Apr 2021 16:10:57 GMT  
		Size: 2.0 KB (1984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5e865356a464c9006414a165a6d0ffb8f062fa737be2ad42e1aa58fcfca23c`  
		Last Modified: Wed, 14 Apr 2021 16:10:56 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3533148ddde03cc5f28669b26c30dee8685db418d250a4b4829e465c0be8a7e`  
		Last Modified: Wed, 14 Apr 2021 16:10:56 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4573099491ec9887bd66033f55b39f6b897d1f59f21f679fdff4f822ebd7ea15`  
		Last Modified: Wed, 14 Apr 2021 16:10:56 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
