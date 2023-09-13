## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:0d1237c42b0bf510367a68f73790bafd41d3e4dba95502ecf7d630eb6dcf0694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:4bc9d7dc99d75f7813148b82653c884ac51975085d49de22b68ac981bf1b3c40
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2022365856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f7856c543b220cf294996bece7566b5515805212fc38127b1450f60b3e3ba5`
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
# Wed, 13 Sep 2023 05:05:36 GMT
ENV NATS_SERVER=2.9.22
# Wed, 13 Sep 2023 05:05:37 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.22/nats-server-v2.9.22-windows-amd64.zip
# Wed, 13 Sep 2023 05:05:38 GMT
ENV NATS_SERVER_SHASUM=e91db73b02bd4dca3eb7a4bf32e29763450b08d593f73e87d0a6b70102dea0d4
# Wed, 13 Sep 2023 05:06:28 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Sep 2023 05:07:52 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Sep 2023 05:07:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Sep 2023 05:07:53 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Sep 2023 05:07:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Sep 2023 05:07:55 GMT
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
	-	`sha256:7e138a75d8a68c57acda5ac3d2a5ea38cfcd91aeeac6e996187886cdc4fe512b`  
		Last Modified: Wed, 13 Sep 2023 05:08:31 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba6b3e055f188fc0c938c464d3df287b87b4ebd990c6d3023e4043e9475882b`  
		Last Modified: Wed, 13 Sep 2023 05:08:30 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d1091bb5b201027155aa6154441b33e21f06c80c98e5502f0ea97d3e6ac36`  
		Last Modified: Wed, 13 Sep 2023 05:08:30 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98cf75715be616bda4fd455e8842d5c47e6361520831c79994aac63897f074a6`  
		Last Modified: Wed, 13 Sep 2023 05:08:30 GMT  
		Size: 242.8 KB (242766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3267078f67f5f3fb7955bda584f1a858622791ed81e9c2e45ac79383c6c3795`  
		Last Modified: Wed, 13 Sep 2023 05:08:30 GMT  
		Size: 5.8 MB (5779913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd81aab1223d4ac5fade6bcbff4e433f5a038988f73089bb43aff8b974c715a2`  
		Last Modified: Wed, 13 Sep 2023 05:08:28 GMT  
		Size: 2.0 KB (1985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a790db19f2a0d625636fa4d186b3b076500c592809d8b95c7a725e0c46a094`  
		Last Modified: Wed, 13 Sep 2023 05:08:28 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4edbf9880281abc4bccc4d818ad299ce3cd5ad235e1cb033fbc49b3096f3a7`  
		Last Modified: Wed, 13 Sep 2023 05:08:28 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c05fad63f054ab864e4484c552a76f82c3bf9e322da181d03f63a597755912`  
		Last Modified: Wed, 13 Sep 2023 05:08:28 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
