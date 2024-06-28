## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:5195ecf10c2b516fec5bfb6ae487b75b5ec433338cc704c9a6971ec907e617f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:b246a667c2242326002d7d1ed0294cb23f4abac2d32d409e67e4ef4affb0b148
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227279692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6e57f49ed021a3dc329373285295a6d9d6f9166ef80f220dc96f820433a67a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:59:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jun 2024 18:59:30 GMT
ENV NATS_DOCKERIZED=1
# Fri, 28 Jun 2024 00:15:18 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:15:19 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.17/nats-server-v2.10.17-windows-amd64.zip
# Fri, 28 Jun 2024 00:15:20 GMT
ENV NATS_SERVER_SHASUM=05590ce7be8802cbd8a75ce84fd74bd4f6ffd65f141277363936143f264d2f47
# Fri, 28 Jun 2024 00:16:47 GMT
RUN Set-PSDebug -Trace 2
# Fri, 28 Jun 2024 00:18:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 28 Jun 2024 00:18:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Jun 2024 00:18:45 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:18:45 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Jun 2024 00:18:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b6e3a886b0409dde5276640ebcea6a4dac570684e6e28fbc210293a21af0dd`  
		Last Modified: Wed, 12 Jun 2024 19:06:59 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06141158aebc1921afac5da541cf6a80846edb4296669ef6f8370783d67dfd2`  
		Last Modified: Wed, 12 Jun 2024 19:06:58 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5ee191911514cca388e8d1ebf484f9f3944a19fb91eaf9ed76f653bca33a89`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdab00343c3faca0fb40fd3134a76287e1b4beeb1f7ea80d08a563cf7cc81c6`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c5e764e166ec7aa93a112437a4b66b16d215188f86c8419d7e62381d1e9028`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0462ddb79019e553acb5349dd73d085d500a4ee9420cc7b93cf89b7938b6dc36`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 469.0 KB (468968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc23581425fe55182e7fc54a0004f41d7f58797172de12751103aadf12e9011`  
		Last Modified: Fri, 28 Jun 2024 00:19:55 GMT  
		Size: 6.1 MB (6116261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c19fb7e5ee2395b6497f5c95cf0864cd65dee59545d651c82b053c9d7de2323`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afdce20e5095d9ab2ceb3523be142be0b3050f0e233346a0cccc9b689970ffe5`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d3dcaf7d2d9287f586f2b3984ccbeb8361b9b6983c7c26e6401cf7e8bfb0d9`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32f6f0d9b837ab19a8a1e340aa6154847732e81f5f99140cc06a3cfb0e55f49`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
