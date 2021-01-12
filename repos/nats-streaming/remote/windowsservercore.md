## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:ab4f90fa36638c93e8552a653422527a599d4a73f996c21353c484c6dc0a154e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64
	-	windows version 10.0.14393.4104; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats-streaming@sha256:1e9246d04cadc2e2c8c9f393c081c3f899ee17cc0c2604e670f4b2dfb473ae78
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2410998451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880b431ca994738c273eb95d89d0200e5faf1def000165c43c3b6d2195fb6ac7`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 04 Dec 2020 02:13:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Dec 2020 14:02:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:36:04 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Jan 2021 00:20:16 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Tue, 12 Jan 2021 00:20:17 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.20.0/nats-streaming-server-v0.20.0-windows-amd64.zip
# Tue, 12 Jan 2021 00:20:18 GMT
ENV GIT_DOWNLOAD_SHA256=26ae310d3ec11617d380106a769236a6dc2209769c0c36d15cb6736db1b589cb
# Tue, 12 Jan 2021 00:20:50 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Jan 2021 00:22:08 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 12 Jan 2021 00:22:09 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:22:10 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 12 Jan 2021 00:22:11 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aa4f58cd6da1aaf1a0b44d443bd88e7fbe5b0a6f193995a1a61d6bd63990f314`  
		Size: 672.5 MB (672541583 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:240407eb82b6591b0574396ec829a4a5cd9a75257a4663f9876942995275965d`  
		Last Modified: Wed, 09 Dec 2020 17:10:14 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b9257be76bd37cad15d45905ec5910266409794a9dbd8a0428174f8b2f352a`  
		Last Modified: Wed, 09 Dec 2020 17:42:00 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ea2225c77eadc0189bc20fb84afed780b270881cda1af919808b4659ddfde4`  
		Last Modified: Tue, 12 Jan 2021 00:26:38 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e11834207f6dd2d9b771b24f539c5e44ba9c03e436eab5fb3d14b440761244`  
		Last Modified: Tue, 12 Jan 2021 00:26:36 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3d13a0cbb1f04703c664ea56832b37d3c72620db9f1322e3987b5939e63be7`  
		Last Modified: Tue, 12 Jan 2021 00:26:34 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1b5c2d8ee1e18e7fd1d2758bb1d910114688b48e87b48b612bc04e7f9ab565`  
		Last Modified: Tue, 12 Jan 2021 00:26:35 GMT  
		Size: 4.9 MB (4866042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3b650e7eae667685fbdb190173a13f5d5f514356e6f86b28a5e117d8d365e5`  
		Last Modified: Tue, 12 Jan 2021 00:26:34 GMT  
		Size: 15.2 MB (15248954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f14a725380678eee4b1fb7eb05c4604f8bcf3d3dbe55a664242327d3a889d9`  
		Last Modified: Tue, 12 Jan 2021 00:26:33 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3968d5703b7cafe8fb35b9c28e5f6d99df9c64e2b9272652cd585e1505eda409`  
		Last Modified: Tue, 12 Jan 2021 00:26:34 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd142e8fb60d24af64f85a7309313043c3e90c22e5f9ad18b37fcb2b05bb10cf`  
		Last Modified: Tue, 12 Jan 2021 00:26:30 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:windowsservercore` - windows version 10.0.14393.4104; amd64

```console
$ docker pull nats-streaming@sha256:1c76108446fc8743e3272a3e5ebe44713cb0f271f791afbcb180b164eeceb30a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5790486404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677b831b855e37cf8ca7b05f3d97e02d9acd7b7f88c3e2cb94350d97dfd45506`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 02 Dec 2020 17:42:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Dec 2020 14:41:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:38:10 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Jan 2021 00:22:38 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Tue, 12 Jan 2021 00:22:39 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.20.0/nats-streaming-server-v0.20.0-windows-amd64.zip
# Tue, 12 Jan 2021 00:22:40 GMT
ENV GIT_DOWNLOAD_SHA256=26ae310d3ec11617d380106a769236a6dc2209769c0c36d15cb6736db1b589cb
# Tue, 12 Jan 2021 00:23:47 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Jan 2021 00:25:46 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 12 Jan 2021 00:25:47 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:25:48 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 12 Jan 2021 00:25:49 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d2696dc2a40dc121fc5acaa02242817ac416c69d17c113e2ac5136d21a3942d8`  
		Size: 1.7 GB (1698858125 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5a79f8be42bf1c358ccc82f32c1481de95c393ef97e712a321c1440d132fda9`  
		Last Modified: Wed, 09 Dec 2020 17:11:03 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d972336c8bcee0026c76e8f199cef405112a70aeef9917f07d2859f15162c1`  
		Last Modified: Wed, 09 Dec 2020 17:42:56 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36f4ebf3f9e4f08ccee6bfa20099991e715ee2894afc2a5ab488f99abde352e`  
		Last Modified: Tue, 12 Jan 2021 00:27:18 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbb72f3ad396e481a0b277ce3e34e967c03d0508866752c073f88ba79fe5ad9`  
		Last Modified: Tue, 12 Jan 2021 00:27:16 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5b181e3fbbd7a07117dea46bb1665bf7cb7d1c63893ba7e34253bc80329005`  
		Last Modified: Tue, 12 Jan 2021 00:27:17 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f188787bf90e9475900fcfe23b4560d8a3c339da882a6bd6a627200f050de787`  
		Last Modified: Tue, 12 Jan 2021 00:27:16 GMT  
		Size: 5.5 MB (5540955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648f80f9fceb0f132e4ecd6f30d636df20cfb7fd51954ae9945a657d622e7875`  
		Last Modified: Tue, 12 Jan 2021 00:27:32 GMT  
		Size: 16.1 MB (16092606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89c59b6b1299bdb040513b474b6d8a594a4bc7dbaded7aa867723807a1fc11a`  
		Last Modified: Tue, 12 Jan 2021 00:27:13 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec9cf99b11036b9be139f4bc0016e3ec80a666200e52ff82978706a12fa30b3`  
		Last Modified: Tue, 12 Jan 2021 00:27:13 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7278eff7db06794f2daef6b524a6e0ae1a8fc04d3924fb1bac92b6e449b539`  
		Last Modified: Tue, 12 Jan 2021 00:27:12 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
