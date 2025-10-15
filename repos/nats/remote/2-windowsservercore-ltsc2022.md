## `nats:2-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:ca6c4c01c59f186bf801bc22ad3523dac53ce9529971a45755457b746336dca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `nats:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull nats@sha256:463842e31e4ca9a69d2eb193c55c3cfea47618382f1f02c13f0e339b2bb0f010
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1496438010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cabe7a5fcb744df1f0b87b074c7312e091a5f0db87f6d117b16d5ca2aea0a35a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:43:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Oct 2025 20:43:33 GMT
ENV NATS_DOCKERIZED=1
# Tue, 14 Oct 2025 20:43:33 GMT
ENV NATS_SERVER=2.12.1
# Tue, 14 Oct 2025 20:43:34 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.1/nats-server-v2.12.1-windows-amd64.zip
# Tue, 14 Oct 2025 20:43:35 GMT
ENV NATS_SERVER_SHASUM=64d4702f31daa2560ba7a0291d2911b36fd6199277721f8ab2aae0d12eb2763e
# Tue, 14 Oct 2025 20:43:50 GMT
RUN Set-PSDebug -Trace 2
# Tue, 14 Oct 2025 20:44:10 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 14 Oct 2025 20:44:10 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Oct 2025 20:44:11 GMT
EXPOSE 4222 6222 8222
# Tue, 14 Oct 2025 20:44:11 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Oct 2025 20:44:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0e5801ded6353758de3eb5774ad87180b42728fe5dde8da5dbd6891e9b7e8f`  
		Last Modified: Tue, 14 Oct 2025 20:47:48 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a663816a911cc828da2b6aff7e1ff9791ba577e7abdfdde8be5c201e9dc67c`  
		Last Modified: Tue, 14 Oct 2025 20:47:48 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73cdf3f3ad5fcd75356d10b1fde49fa85a07743dbf12381d162da6559138f0c`  
		Last Modified: Tue, 14 Oct 2025 20:47:48 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4267c74fd2b5bab82628d01182e066bedf48f16addc75b363c2bcfe36b3ddc6`  
		Last Modified: Tue, 14 Oct 2025 20:47:48 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f464b879dca0b03860ecdd4b38744913c0be15d235eb1e7a4994e34b180f94ba`  
		Last Modified: Tue, 14 Oct 2025 20:47:48 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8659a242e0ea1551ffc514e532fd4e39526a7dc8203cd9cc8b72c12c69a010e1`  
		Last Modified: Tue, 14 Oct 2025 20:47:48 GMT  
		Size: 328.8 KB (328807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4235a5f7c802404198588c8fc564242588ebc2528b3ca352fac8098be590ae43`  
		Last Modified: Tue, 14 Oct 2025 20:47:49 GMT  
		Size: 7.1 MB (7077668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a011f2055a08eb11c8b631ed80dbe6f71b26bf84d8eccb3c80fcdf6b52b1016`  
		Last Modified: Tue, 14 Oct 2025 20:47:48 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4430845412e0daab3ca84931f4c62c6cf9c296cf1c58340bd64c88ab003ae1f7`  
		Last Modified: Tue, 14 Oct 2025 20:47:48 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c90803d48731e1c81c15a96e7cd44b938751cc72cba7b486595c32abc0e17aa`  
		Last Modified: Tue, 14 Oct 2025 20:47:48 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f03d9258a063c3fa1c398ec5580fa466fb2365d9dda34e2440ff048081d26db`  
		Last Modified: Tue, 14 Oct 2025 20:47:48 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
