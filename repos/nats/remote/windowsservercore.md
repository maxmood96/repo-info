## `nats:windowsservercore`

```console
$ docker pull nats@sha256:7fa737be6b9ee90528f5210654f2cce77958411cf0019b91c6dbeb7f9d98a02c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:windowsservercore` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:60200e6d6acfe2ee1ea866f9466589b278ea9727b1ce47e0b02d81273325639c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2022627359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b338afb88070afc3c9e0061cef696ff84929c1aca9dcfc32d8f97d6fca6ba8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 29 Aug 2023 17:09:18 GMT
RUN Install update 10.0.17763.4851
# Wed, 13 Sep 2023 03:56:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Sep 2023 05:05:36 GMT
ENV NATS_DOCKERIZED=1
# Wed, 20 Sep 2023 00:16:07 GMT
ENV NATS_SERVER=2.10.0
# Wed, 20 Sep 2023 00:16:08 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.0/nats-server-v2.10.0-windows-amd64.zip
# Wed, 20 Sep 2023 00:16:08 GMT
ENV NATS_SERVER_SHASUM=bb932643a55347b8a12f7681d98b45d5ef858ce89be375dcc9e5701ef31900e2
# Wed, 20 Sep 2023 00:17:05 GMT
RUN Set-PSDebug -Trace 2
# Wed, 20 Sep 2023 00:18:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 20 Sep 2023 00:18:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 20 Sep 2023 00:18:40 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Sep 2023 00:18:41 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 Sep 2023 00:18:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179757339e051b99f9a62375fed8f87ffcc4df0eeedb984d20b485bdd089ad08`  
		Last Modified: Tue, 12 Sep 2023 19:41:25 GMT  
		Size: 365.7 MB (365709508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b21bbf840142288ae2bce3465085b591133cf10f78f7dda43277db4838332d8`  
		Last Modified: Wed, 13 Sep 2023 04:36:45 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54f616fe064e9d4e73bf2aec9a4fe9c58837ec84c2fc998a54ab7a77b52e109`  
		Last Modified: Wed, 13 Sep 2023 05:08:32 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9968d99cd124e281e9eb32b9c79dec9151b84a282de0b9ff48a6421893210018`  
		Last Modified: Wed, 20 Sep 2023 00:19:47 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8d65f137623b9fa041e6c95d037bb1c84ac45375dfb3f5e165fbc0de55d3b4`  
		Last Modified: Wed, 20 Sep 2023 00:19:47 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cce88f9f56d559bbcf61b53c8ee212347e9c2adfde6514bf7ca6b158038c0aec`  
		Last Modified: Wed, 20 Sep 2023 00:19:47 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5550f9c177606353dbe3304af76edd546e2e3d5b26b75dedbf0a37013fbb5b62`  
		Last Modified: Wed, 20 Sep 2023 00:19:48 GMT  
		Size: 242.9 KB (242950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499a91d096b1315cb5aac04373a5e9d946a685e495aee8b53edc2653447c09cd`  
		Last Modified: Wed, 20 Sep 2023 00:19:47 GMT  
		Size: 6.0 MB (6041303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1e39de17beb91f14ac1ef37deaf04b266f775d84e82bb59e5b097bf2de7a20`  
		Last Modified: Wed, 20 Sep 2023 00:19:45 GMT  
		Size: 1.9 KB (1950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437854ba90dbb5c87ffa19ad5c87d23fe1d37798a9335b9cb81dc43b30416a4a`  
		Last Modified: Wed, 20 Sep 2023 00:19:45 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57bacc93360e373bd14cd33b4a64310d1ff9128b513e6e91d8029d1107aa552`  
		Last Modified: Wed, 20 Sep 2023 00:19:45 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358e2291cb98e173820210f90cc332a39caf46d7efe66441543a683d80acecb6`  
		Last Modified: Wed, 20 Sep 2023 00:19:45 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
