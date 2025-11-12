## `nats:windowsservercore`

```console
$ docker pull nats@sha256:9c59cb12551c0dc401038b6a2a48d83bb123e2b4c464f09537d80a7e206821a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `nats:windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull nats@sha256:4194199ed6467841d479f65c4b803ef3ca56f9b26bab09840585dc91cdfd8162
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1777536942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f4e3a7b8f3ba9efe67d7cd0aefbd6e2baedd97ff76d1b60a3c8776d27705463`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:12:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Nov 2025 19:12:55 GMT
ENV NATS_DOCKERIZED=1
# Tue, 11 Nov 2025 19:12:56 GMT
ENV NATS_SERVER=2.12.1
# Tue, 11 Nov 2025 19:12:58 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.1/nats-server-v2.12.1-windows-amd64.zip
# Tue, 11 Nov 2025 19:12:59 GMT
ENV NATS_SERVER_SHASUM=64d4702f31daa2560ba7a0291d2911b36fd6199277721f8ab2aae0d12eb2763e
# Tue, 11 Nov 2025 19:13:17 GMT
RUN Set-PSDebug -Trace 2
# Tue, 11 Nov 2025 19:13:37 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 11 Nov 2025 19:13:37 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 11 Nov 2025 19:13:38 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Nov 2025 19:13:39 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 11 Nov 2025 19:13:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0eaf81f9733b26165380ca0ea9a1084857aa95f816c045dec53f5f2ef90c8b0`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7925da799fc7c936d41fef1f8c06637a98af50caf2b886e4b1c4a4cbf8cdf6b6`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ab6b858b62b926783531cd6b9e824c3c87dd94402554297ed42286a901f736`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cca028dbec288d8dde097c73c40aa77486c73f910b4c1c76aba537dcac9375`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9f589cc56a3a0d0fd6506fb02b902232939b242fafa7ed9d66eea9cbb6e8af`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7eeea4a87b7db70d2f57e2f62b109091c5f8d1692db303a9f887740eb8e71b`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 484.6 KB (484564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9d45c0695b9a43f744eae4cd475e9bd3745f0c8df70cfbecd582b0ff97e78c`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 7.1 MB (7078504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1948b28fa6498418bce0894fe98fac52fcc9ceb18eca0c217544974119e0df33`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee77c60b54d2cc421c903a438b952a8bc3dede962320511e64e088b60ff84c0`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d49e56988724611d6dc22858bac8740e49ec38ca12b82d99d7b61ea873c349c`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d706a761b634757604c3dcbbd3f27e355c8f8b8c7e2fb704e85b1919f01dca8`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
