## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:caacdd68ac15825419bdd0d1ed333408d4c22b3a26035275e48d153c22268c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:6a50e306cf3f0c7dbd1e2df340d2696b1622ad3232c7d83cb0d1f72195089ca5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2022614730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82b912330f09e1d0a6d64e3034e0da94f54645b45b8713a83652480b2bea1b5`
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
# Thu, 21 Sep 2023 00:15:15 GMT
ENV NATS_SERVER=2.10.1
# Thu, 21 Sep 2023 00:15:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.1/nats-server-v2.10.1-windows-amd64.zip
# Thu, 21 Sep 2023 00:15:16 GMT
ENV NATS_SERVER_SHASUM=88f2990dd6fea0bb2d8ba5cfde41ab5c96dd01bbaf4f9e9a3569815a0803cb1c
# Thu, 21 Sep 2023 00:16:19 GMT
RUN Set-PSDebug -Trace 2
# Thu, 21 Sep 2023 00:18:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 21 Sep 2023 00:18:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 21 Sep 2023 00:18:06 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:18:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 21 Sep 2023 00:18:08 GMT
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
	-	`sha256:905f26828615c039d9da3e9f52c8b61ad3b2183a7ec3940bb1985bfc9a64be81`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a235c3fc87ed07702e70bb83fcbcb5ccaf81440d9ffd8d450d16bb7f273ce0`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759a393cccf186a4709cd9d0c4da137cade59a534bc53125be57217f7b21ef61`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cc61521de3ff29def7a6479a78dc7165d144b87f68e455eedb1ed30775aeaa`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 242.8 KB (242789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d014e00481cb1e60003ba14c0a143d5126a763b4d413032ddad39559313825d`  
		Last Modified: Thu, 21 Sep 2023 00:19:19 GMT  
		Size: 6.0 MB (6028853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ba83a190b4d5c219eab28b93cc94ab37e1a941e7270d4e60b5114f037589da`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 2.0 KB (1987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9ab4d57441cb1024559b87812361354ac635647bdb46a4ea450769c671d6f2`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd0e1cd2f7b50ded5cab327e6c888492fb4c4e022a0062cc719b9b6f9bcd8f4`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca70f3129ad44afad7b489a20cfd3a7bd2187694d47690907dab50fc4638c34`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
