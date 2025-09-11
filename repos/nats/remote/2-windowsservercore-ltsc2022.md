## `nats:2-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:ee1642b51a1cd4c98a4faf0bef3edaa556d3d01c1046fcb17588f6c5656aff29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `nats:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull nats@sha256:329abd66cb04d28dd53c8560f8f4263e2ffc753266def46aa5d368d0ea828f27
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2289390773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a70304680d5c23466643321d23a8688dc4e6c0ff0f124ffe8eb9b369a73e37d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Sep 2025 21:49:22 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Sep 2025 21:49:23 GMT
ENV NATS_SERVER=2.11.9
# Wed, 10 Sep 2025 21:49:24 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.9/nats-server-v2.11.9-windows-amd64.zip
# Wed, 10 Sep 2025 21:49:25 GMT
ENV NATS_SERVER_SHASUM=841a953d9be1d55b5f2b990c624b239f7f938baaf00d5627ac34d6c363a2fda3
# Wed, 10 Sep 2025 21:50:10 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Sep 2025 21:50:35 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Sep 2025 21:50:36 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 10 Sep 2025 21:50:37 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Sep 2025 21:50:38 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Sep 2025 21:50:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd6494b5c72082f044472dd8680009c6600963291041425599259e646ce1c92`  
		Last Modified: Wed, 10 Sep 2025 21:59:53 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673b8abccf74627b6c46f4cbfb529bdb907477192896aecf6c567c5c8bcaec9e`  
		Last Modified: Wed, 10 Sep 2025 21:59:53 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f5f13c5894bea7f74a0cb843f93a20cfcbab925fe6ba85e4ff8876e4cf313d`  
		Last Modified: Wed, 10 Sep 2025 21:59:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790b29e4ada28f06a47a1b9ab685f72c2262c7db6dfcf1d22b9a1b15d95fcd48`  
		Last Modified: Wed, 10 Sep 2025 21:59:53 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c14bdc8e7a4b3fcde9336d171eea21f402bf8d715817ccd1bc2df1dba1613a8`  
		Last Modified: Wed, 10 Sep 2025 21:59:53 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189fe576d1c157668d34f1a828eb52dbdd9b13d1ea24eda0cfb9ece9cebd5e46`  
		Last Modified: Wed, 10 Sep 2025 21:59:53 GMT  
		Size: 349.7 KB (349681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb5860388cf7ab2058b1a828285ad1d9e04168b0f4841c30e5ee3346582811a`  
		Last Modified: Wed, 10 Sep 2025 21:59:54 GMT  
		Size: 6.9 MB (6883734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d424f63dd6e36f5c0235d92e5158f811b0184ddc04fb2ec51bb216fdf662fe2`  
		Last Modified: Wed, 10 Sep 2025 21:59:53 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a760abe4d2bc3a58dd8dbd85c6f53a7b750fbf8891a19eee3844b0c4145f9e48`  
		Last Modified: Wed, 10 Sep 2025 21:59:53 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec050bedfa0dc744b00b229173bc66c474816b08e8df356bc893e4db4e049a9`  
		Last Modified: Wed, 10 Sep 2025 21:59:54 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e19faf1abdd5ac24e164ea282131b6dacfb4436ee1fc4995f1f257133849246`  
		Last Modified: Wed, 10 Sep 2025 21:59:53 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
