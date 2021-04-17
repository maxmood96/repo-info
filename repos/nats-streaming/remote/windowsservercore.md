## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:98b9617ca151407afacb114ff81aff503c2ea4577b96209c8c5676361ca9557a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:46a11494d76fc259b7a9f8a0c27873460bf913594ca6f05a299234525b15094a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2485739262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b666c7480c5c11601af2df96a1489969fe78538e0945930ef51de2fe96c389a1`
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
# Fri, 16 Apr 2021 21:15:14 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:15:14 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.2/nats-streaming-server-v0.21.2-windows-amd64.zip
# Fri, 16 Apr 2021 21:15:15 GMT
ENV GIT_DOWNLOAD_SHA256=5d4367fea29116fcd70c364c8e808d6bc8e74214effbde83dd9548455bd06df2
# Fri, 16 Apr 2021 21:16:09 GMT
RUN Set-PSDebug -Trace 2
# Fri, 16 Apr 2021 21:17:42 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Fri, 16 Apr 2021 21:17:43 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:17:44 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 16 Apr 2021 21:17:45 GMT
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
	-	`sha256:63694c9279bb4c7122e4c15326493b2ffac8c6df264b45b2bc1542aa4763c785`  
		Last Modified: Fri, 16 Apr 2021 21:23:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7109d9070f9055006a72b16519d93e1ff1ba1e5421bc264c2197ef4e6a3edb0d`  
		Last Modified: Fri, 16 Apr 2021 21:23:46 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6023c32ca8ac978165d5409ef9087006ee445e04c5b93d707b0fb484faa1b3c3`  
		Last Modified: Fri, 16 Apr 2021 21:23:46 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc9c54c2bcc706204b7d4feaf8b3e66c9efaab5f43babd81045e31c318bc25c`  
		Last Modified: Fri, 16 Apr 2021 21:23:45 GMT  
		Size: 5.1 MB (5096185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208b0279ea22aad1e519ba1f2f927cf4598bdfbddf3a33b2c14e6356331b2f48`  
		Last Modified: Fri, 16 Apr 2021 21:23:47 GMT  
		Size: 10.9 MB (10877752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d04869441fc428a1ea7711da8ca9b0c8b6bdee6622751b6c44d98633fc9ded`  
		Last Modified: Fri, 16 Apr 2021 21:23:44 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a25017dc98d8b32009d962f73fcf54adb74971347a78fb4f94b35da8c92179`  
		Last Modified: Fri, 16 Apr 2021 21:23:44 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cc3678ca9e1a8f67aca7150e64f25b9f0a28cf4c07ecdaae86095d9fe09523`  
		Last Modified: Fri, 16 Apr 2021 21:23:44 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:windowsservercore` - windows version 10.0.14393.4350; amd64

```console
$ docker pull nats-streaming@sha256:2855b5d29b6f04637f9552d71cda49dcb3dc4d542d7ed205bfe8d97be393545f
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816479551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbec025bd002885ef7f70a46dec4fe05d03313f3821b9d4f905ebe807c1f3f6`
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
# Fri, 16 Apr 2021 21:18:08 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:18:09 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.2/nats-streaming-server-v0.21.2-windows-amd64.zip
# Fri, 16 Apr 2021 21:18:10 GMT
ENV GIT_DOWNLOAD_SHA256=5d4367fea29116fcd70c364c8e808d6bc8e74214effbde83dd9548455bd06df2
# Fri, 16 Apr 2021 21:20:14 GMT
RUN Set-PSDebug -Trace 2
# Fri, 16 Apr 2021 21:22:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Fri, 16 Apr 2021 21:22:44 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:22:46 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 16 Apr 2021 21:22:47 GMT
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
	-	`sha256:bb633935c8262a169f8ce0f1c047198f3f981cf5315ebbdfb8aa7ba7e7d72bb5`  
		Last Modified: Fri, 16 Apr 2021 21:24:18 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65576d29a65010c1357bcc65b8be2b2b1fdc9c4e43886372b8906fe1e108992b`  
		Last Modified: Fri, 16 Apr 2021 21:24:18 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5de8efb2c9f3c99d2381a169ff4f442ca3b804a8a822584c54fa8673ef2f18`  
		Last Modified: Fri, 16 Apr 2021 21:24:18 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a185c587f57ffd591baafd272bad6bdd76759232c6fb38c93ae2f951ef672d58`  
		Last Modified: Fri, 16 Apr 2021 21:24:18 GMT  
		Size: 5.7 MB (5660316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58dea9968ebcd0bab739582d83245d50a4866d2bcbd2153d5dfa856e285fc810`  
		Last Modified: Fri, 16 Apr 2021 21:24:20 GMT  
		Size: 15.9 MB (15924139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d5db835b40ab66c30271634885e8fae5e1ba4c40c486a8cea2f021882824f8`  
		Last Modified: Fri, 16 Apr 2021 21:24:15 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2a1a71345bf095f4133c7fad40e22ecde64b60261ca6035b69111680d7f576`  
		Last Modified: Fri, 16 Apr 2021 21:24:16 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffed13d909a2d6c0c79217cee06b023d0e1bbe267704ea88f3d26b5b3fd6b5e9`  
		Last Modified: Fri, 16 Apr 2021 21:24:15 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
