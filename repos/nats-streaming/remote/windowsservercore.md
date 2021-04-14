## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:a8102f4b4b7a4dd707584cb4127c67087e63f8b5bb46b66e8bcd6dc8565c6258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:d9b88aa3a330b3290906f99e7d6ecd15ca2a2e1d3971b9d9289b93d30c3cd169
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2485693134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edccba0ec32510e9cbd95e6fb54bc1cce5ffcda21318e14b15aef92d30b968a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
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
# Wed, 14 Apr 2021 20:27:47 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 20:27:48 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.1/nats-streaming-server-v0.21.1-windows-amd64.zip
# Wed, 14 Apr 2021 20:27:49 GMT
ENV GIT_DOWNLOAD_SHA256=798ec9b686a8dcb4de93074f416eab067a0896b52ccfc05b65a5e21d55e634e5
# Wed, 14 Apr 2021 20:28:31 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Apr 2021 20:30:13 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 14 Apr 2021 20:30:14 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 20:30:15 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Apr 2021 20:30:16 GMT
CMD ["-m" "8222"]
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
	-	`sha256:117282a30c6a3fbb982bd59e09a51b1fef503b2c8b179319ba79482e99fe384e`  
		Last Modified: Wed, 14 Apr 2021 20:35:30 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496226fe152ceeff1fa0f62ca2d7b6bc19faa001434219174ae46a5fd50a5062`  
		Last Modified: Wed, 14 Apr 2021 20:35:30 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d2433ca3469117417315b440945cb8cd6772eb21571dd4179873e007da1d89`  
		Last Modified: Wed, 14 Apr 2021 20:35:30 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939e907443a80f726b409bd6af9aac2d7d95ea075599cf36b47c67d96db68e5b`  
		Last Modified: Wed, 14 Apr 2021 20:35:33 GMT  
		Size: 5.1 MB (5072715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36493380d982f607672d92b042f6a6fba85e6c73a2514659ab314414e1e03ce5`  
		Last Modified: Wed, 14 Apr 2021 20:35:31 GMT  
		Size: 10.9 MB (10855200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c00d72188f4d2c91bcd99fcff6f8aaa8ecbddaf6e31490f52ea27ffa361240b`  
		Last Modified: Wed, 14 Apr 2021 20:35:27 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c24f1b01b5e8513e9c865e784023d71e169853d5b5d84d09f32a4ad347d6633`  
		Last Modified: Wed, 14 Apr 2021 20:35:27 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d461ef53125c21684fd7078f19d920864bc170e1419530a9799d4c4637f57e6c`  
		Last Modified: Wed, 14 Apr 2021 20:35:28 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:windowsservercore` - windows version 10.0.14393.4350; amd64

```console
$ docker pull nats-streaming@sha256:fb1d8548b281cb5116d343ca84eeeb7b3b384ea4fbad8e15050fa042425a55e3
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816454011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f2cd68f941eba9047e18e03d45bc6ad435c2f87e4374be7184090e2822cc37`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
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
# Wed, 14 Apr 2021 20:30:43 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 20:30:45 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.1/nats-streaming-server-v0.21.1-windows-amd64.zip
# Wed, 14 Apr 2021 20:30:46 GMT
ENV GIT_DOWNLOAD_SHA256=798ec9b686a8dcb4de93074f416eab067a0896b52ccfc05b65a5e21d55e634e5
# Wed, 14 Apr 2021 20:32:29 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Apr 2021 20:34:42 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 14 Apr 2021 20:34:43 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 20:34:44 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Apr 2021 20:34:46 GMT
CMD ["-m" "8222"]
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
	-	`sha256:a2d8948e6263c2bac7f73817369684ee9ce80dcea983d2da7c4d7be9fa1b92da`  
		Last Modified: Wed, 14 Apr 2021 20:36:05 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a701af2866e93c3ecf557b60b96c4c01276eb2e524382b5ad189843adbf3355`  
		Last Modified: Wed, 14 Apr 2021 20:36:05 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fc8f88f56d9ac579fa5db162a04bdd9d01802dd45c4f75577dae3515349334`  
		Last Modified: Wed, 14 Apr 2021 20:36:05 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff9002a73083bb7987c2c033559072c3803ffb30b5df7ec99d7236e718ac397`  
		Last Modified: Wed, 14 Apr 2021 20:36:04 GMT  
		Size: 5.6 MB (5646320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4a7bb20d404a5bac7e79831b31797bd1a2dbf58ab157ff26fafe63e748966e`  
		Last Modified: Wed, 14 Apr 2021 20:36:07 GMT  
		Size: 15.9 MB (15912932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ceea9dc7862bc910070631046bb01d0159fcd3afa884d913477ddea2ae4ef9`  
		Last Modified: Wed, 14 Apr 2021 20:36:02 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e773fcabbbc441abd5c250e3169866ae46ab83e23543816209ecb0e60e0f60`  
		Last Modified: Wed, 14 Apr 2021 20:36:02 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23273c3337d46e183210a490996b4c40d280c0fbeae6ad837f0be19167750c38`  
		Last Modified: Wed, 14 Apr 2021 20:36:02 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
