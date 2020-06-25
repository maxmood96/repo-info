## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:a3cf18102bec632be2795c497e01477397d754cf29d6a8f71f4b28e99f209c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64
	-	windows version 10.0.14393.3750; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.1282; amd64

```console
$ docker pull nats-streaming@sha256:fccf91ec6703587be4343172ce28aafedeaa70a0e124e6e6692a423165fa1b8a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2309404710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d133672bcd5cfbbacf6b0a64ea13bc17159ad634ba3a26595d3d070ab81a4c31`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jun 2020 16:02:03 GMT
ENV NATS_DOCKERIZED=1
# Thu, 25 Jun 2020 19:14:32 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Thu, 25 Jun 2020 19:14:33 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.18.0/nats-streaming-server-v0.18.0-windows-amd64.zip
# Thu, 25 Jun 2020 19:14:34 GMT
ENV GIT_DOWNLOAD_SHA256=a0c0261df2ce589fe9706617323e06c5bcae70511112eae921681b1169674bc8
# Thu, 25 Jun 2020 19:15:08 GMT
RUN Set-PSDebug -Trace 2
# Thu, 25 Jun 2020 19:16:23 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Thu, 25 Jun 2020 19:16:24 GMT
EXPOSE 4222 8222
# Thu, 25 Jun 2020 19:16:25 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 25 Jun 2020 19:16:26 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2192add29c9167423d378daa499903c4488337cdc2cf961ebeb0e4c0b492f9`  
		Last Modified: Wed, 10 Jun 2020 16:08:35 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fdc3ac2d9ccd0382babff697996c03e73078cea8cd708ae249f9f7e440a495a`  
		Last Modified: Thu, 25 Jun 2020 19:20:29 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08db7f0f23bcbaf120f7ce31d3b645acbd51ec9ec2b9c5f0de02713ce1a20846`  
		Last Modified: Thu, 25 Jun 2020 19:20:28 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a14a4e817fcb29d1f6c15cfe682270eab5b418e5368ab5d33d98b941e580c41`  
		Last Modified: Thu, 25 Jun 2020 19:20:28 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be6a9189710ce278b6d6e9e49b49ff0891d78bdd64ebfb2c5a2c36dd987fc95`  
		Last Modified: Thu, 25 Jun 2020 19:20:27 GMT  
		Size: 4.8 MB (4787569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b3a8c2acc0287c3ef79dd6c22afecade9ed9deaa5295912427651209679dfd6`  
		Last Modified: Thu, 25 Jun 2020 19:20:29 GMT  
		Size: 10.7 MB (10693762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a914cfe5af6c345eaa54dfdcfc9774913b1f1c9f5a10a74b50941305a0bfa454`  
		Last Modified: Thu, 25 Jun 2020 19:20:26 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7235d4bb5ccdbdcf9eed6b2d280b46d296002871faa1fb4d2bd21e90cce7a48`  
		Last Modified: Thu, 25 Jun 2020 19:20:26 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca308b080197d582de4106f74424ad989679cbd06b09832c832607a3776d5411`  
		Last Modified: Thu, 25 Jun 2020 19:20:26 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:windowsservercore` - windows version 10.0.14393.3750; amd64

```console
$ docker pull nats-streaming@sha256:1114f61e45775a36a2bbfa0b3404c65f9c57ee01c48de00cb7c7295fdc8eb88e
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5755256249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c3dc35de6edc22e58f63b69b5b54363526d18f429fb85b27f37bc15c32ae04`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jun 2020 16:04:27 GMT
ENV NATS_DOCKERIZED=1
# Thu, 25 Jun 2020 19:16:55 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Thu, 25 Jun 2020 19:16:56 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.18.0/nats-streaming-server-v0.18.0-windows-amd64.zip
# Thu, 25 Jun 2020 19:16:57 GMT
ENV GIT_DOWNLOAD_SHA256=a0c0261df2ce589fe9706617323e06c5bcae70511112eae921681b1169674bc8
# Thu, 25 Jun 2020 19:18:01 GMT
RUN Set-PSDebug -Trace 2
# Thu, 25 Jun 2020 19:19:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Thu, 25 Jun 2020 19:19:59 GMT
EXPOSE 4222 8222
# Thu, 25 Jun 2020 19:20:00 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 25 Jun 2020 19:20:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f945dc3cc7d024d3f86a74f177545b57d99c3209592a625bb655bf01921d2c`  
		Last Modified: Wed, 10 Jun 2020 16:09:12 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3713b83b4c75d0a80e8687bc45df0c5bd354e620902411ad1b3028c9dceb2bf5`  
		Last Modified: Thu, 25 Jun 2020 19:21:03 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c381803b95a9448680f1e9ff9ef8386e9acd31f7481b2a2035b3465d15cf25`  
		Last Modified: Thu, 25 Jun 2020 19:21:03 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8435805852c6bcef95774603f6342eee8cb5011e45e0df4bd6748a44a16a69e9`  
		Last Modified: Thu, 25 Jun 2020 19:21:03 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf82c782533604d6df3b87130cef3e947dadecf3e6901038e69bdcc42d1432c9`  
		Last Modified: Thu, 25 Jun 2020 19:21:02 GMT  
		Size: 5.4 MB (5391316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23a41a97ee171205d62ebd2014d3048882dee3fadd09cdb07b4aaf2bdf4ff94`  
		Last Modified: Thu, 25 Jun 2020 19:21:03 GMT  
		Size: 15.9 MB (15858190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373353a28d2cec1c03404ca3f978e36be91bd0101fc6833d413336688c879d1f`  
		Last Modified: Thu, 25 Jun 2020 19:21:00 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8695528b591a7419d30570a035a97b0a041ad7951e26210e29b1236b61f86d04`  
		Last Modified: Thu, 25 Jun 2020 19:20:59 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6562c9c2a1ce35eb664d14dcf45dab39154e7954e54029ddf893b339a7e0df5`  
		Last Modified: Thu, 25 Jun 2020 19:21:00 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
