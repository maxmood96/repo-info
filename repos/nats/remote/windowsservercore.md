## `nats:windowsservercore`

```console
$ docker pull nats@sha256:dc86f96f385113e83673d85b0c4b9d6341683d91832b157dde6e5bcc9440b6ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2183; amd64
	-	windows version 10.0.14393.4651; amd64

### `nats:windowsservercore` - windows version 10.0.17763.2183; amd64

```console
$ docker pull nats@sha256:16b38c7099b3bfacb7e6224b87c3d439d2f94435f2a428176abd264ed9e81787
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2691990580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:480b4069e0e61d73288a9f54f59ea41e72e7b23b6ae8b2e529dd679d13436a6a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Sep 2021 04:08:33 GMT
RUN Install update 1809-amd64
# Wed, 15 Sep 2021 13:14:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Sep 2021 15:40:54 GMT
ENV NATS_DOCKERIZED=1
# Wed, 15 Sep 2021 15:40:55 GMT
ENV NATS_SERVER=2.5.0
# Wed, 15 Sep 2021 15:40:56 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.5.0/nats-server-v2.5.0-windows-amd64.zip
# Wed, 15 Sep 2021 15:40:57 GMT
ENV NATS_SERVER_SHASUM=0eae96ad4555f5060b0b6325ba972566b404cd8930b3168b9c0ffe911d15c5d8
# Wed, 15 Sep 2021 15:41:39 GMT
RUN Set-PSDebug -Trace 2
# Wed, 15 Sep 2021 15:42:48 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 15 Sep 2021 15:42:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 15 Sep 2021 15:42:49 GMT
EXPOSE 4222 6222 8222
# Wed, 15 Sep 2021 15:42:50 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 Sep 2021 15:42:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0ddf88812f10c7d6edc858aa9784ff5ca9de4a7bb631909c090090343abd059`  
		Size: 968.4 MB (968365008 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6c4091e033b8590db7b89fded6d31ac2224162744daa4d7a7a66cbebd4b8c228`  
		Last Modified: Wed, 15 Sep 2021 15:04:44 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c75402e6fab70f623ca8becfa5bb563e5630bbb4dac8adb11e385d75e171aed`  
		Last Modified: Wed, 15 Sep 2021 15:45:53 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473a723b3e6315586b9135948bb51f096c06cc7e5eadaead7438b9c7ba1997e0`  
		Last Modified: Wed, 15 Sep 2021 15:45:52 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4776a6c5726f798ab97dc1ae39da7632a7896bf7f7f87182c648b914d3ad07ef`  
		Last Modified: Wed, 15 Sep 2021 15:45:52 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b53a75778782a846153156529c0d022ead4a05b49aca4aea1694d511010449b`  
		Last Modified: Wed, 15 Sep 2021 15:45:53 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:467093e4fe8c72c036724367d959d58396599fecdc3c868ab712c07eff30d647`  
		Last Modified: Wed, 15 Sep 2021 15:45:53 GMT  
		Size: 349.5 KB (349456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8ea09bb898384faccfc7d2e2c1d300789f1d0ce5cc3124f8bf1fcf443d5ef6`  
		Last Modified: Wed, 15 Sep 2021 15:45:51 GMT  
		Size: 4.9 MB (4930656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d11b47fc4c7d221ad48b3c92b896e8aaba990b9147b07b5eaca9d3b785504f3`  
		Last Modified: Wed, 15 Sep 2021 15:45:50 GMT  
		Size: 1.8 KB (1847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17d4aa84573f4aef18be60f58da9ac4de4f43bc4a4ae40b7b70a97e51e9ca55`  
		Last Modified: Wed, 15 Sep 2021 15:45:50 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfc39abe03d3751e52fd86fe0a40894d85af817080bece5771cdb296d9121aa`  
		Last Modified: Wed, 15 Sep 2021 15:45:50 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ea8a4e8f7462ead2253e51b034307a6b4cbee52d0dbf799bd9a6069789a6a6`  
		Last Modified: Wed, 15 Sep 2021 15:45:50 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:windowsservercore` - windows version 10.0.14393.4651; amd64

```console
$ docker pull nats@sha256:7cbc05eb45c582c2183f504b734fe818cb95a7855c2715d43fb0646f636ffaea
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6276636436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e3be11dc730f4c7edcc14830b2914e542934af2cd851036c1ec3410f3aec82`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 13 Sep 2021 01:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Sep 2021 13:26:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Sep 2021 15:43:15 GMT
ENV NATS_DOCKERIZED=1
# Wed, 15 Sep 2021 15:43:16 GMT
ENV NATS_SERVER=2.5.0
# Wed, 15 Sep 2021 15:43:17 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.5.0/nats-server-v2.5.0-windows-amd64.zip
# Wed, 15 Sep 2021 15:43:18 GMT
ENV NATS_SERVER_SHASUM=0eae96ad4555f5060b0b6325ba972566b404cd8930b3168b9c0ffe911d15c5d8
# Wed, 15 Sep 2021 15:44:02 GMT
RUN Set-PSDebug -Trace 2
# Wed, 15 Sep 2021 15:45:15 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 15 Sep 2021 15:45:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 15 Sep 2021 15:45:17 GMT
EXPOSE 4222 6222 8222
# Wed, 15 Sep 2021 15:45:18 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 Sep 2021 15:45:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9b8281bf21e46c781fb54e4f15f5728e2c44dea4219c9e6deeb732f1d909d3b`  
		Size: 2.2 GB (2201342322 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5796468f91731000e9a76e836156826a1cd4ed963bcd80e6558c538a12c2132d`  
		Last Modified: Wed, 15 Sep 2021 15:05:15 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611fe9c559abed986280087eef7d362a6ecb9ad281b1427395fdfc2d99d3d9c4`  
		Last Modified: Wed, 15 Sep 2021 15:46:29 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe97e08139d272284140d657e253065dab56b362c78dd414ec60a4500ffd471`  
		Last Modified: Wed, 15 Sep 2021 15:46:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e3609d16791e22d069e03abfb33c315561c5d7b3cc88d9e8521cfdd01e6b08`  
		Last Modified: Wed, 15 Sep 2021 15:46:28 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655ff9498510f350d59b64f3226c80e6f264ed769f356c27384bc92589c713b2`  
		Last Modified: Wed, 15 Sep 2021 15:46:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bcfde11293a10fb9b99d3f8581a37ad8ce71e468b0cb2a45bbab435155002a9`  
		Last Modified: Wed, 15 Sep 2021 15:46:28 GMT  
		Size: 338.7 KB (338699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496c14f31c02e41ea76ad4d38ca97bdb0fa90479f9858332400abc8c5faff1b4`  
		Last Modified: Wed, 15 Sep 2021 15:46:27 GMT  
		Size: 5.0 MB (4957181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde2e758dd983c28b139b8f2470eb7029f3893d19e44d9883a276813537ef699`  
		Last Modified: Wed, 15 Sep 2021 15:46:25 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fe030af86f1d29f778e51804c466499ae1b880d557b6a0d8b66186f0cf3990`  
		Last Modified: Wed, 15 Sep 2021 15:46:25 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07db3f2fcb0d7d398e8a0caca0f2bcfd2c2b51a890b29bf5484e4f91bd626106`  
		Last Modified: Wed, 15 Sep 2021 15:46:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58b88b21f41a8ec6b79834e5b3eda83446b5a93f70581fb198c939be2153ddd`  
		Last Modified: Wed, 15 Sep 2021 15:46:25 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
