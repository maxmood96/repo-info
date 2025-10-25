## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:71168e770d7fdd30dbb5aeaca3edcbd1b32debf35552ad68036e6ebabdc6d56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `nats:2-windowsservercore` - windows version 10.0.20348.4297; amd64

```console
$ docker pull nats@sha256:92cc76537e2ace4c421b02794f4b01a5f5c9c65a8a9c0b8c434c6416ba82191c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1584774400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69105e97a96903d7cd693657ab47ee7904b027f4b30e8c0310daeb872765192e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:11:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 24 Oct 2025 18:11:26 GMT
ENV NATS_DOCKERIZED=1
# Fri, 24 Oct 2025 18:11:27 GMT
ENV NATS_SERVER=2.12.1
# Fri, 24 Oct 2025 18:11:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.1/nats-server-v2.12.1-windows-amd64.zip
# Fri, 24 Oct 2025 18:11:29 GMT
ENV NATS_SERVER_SHASUM=64d4702f31daa2560ba7a0291d2911b36fd6199277721f8ab2aae0d12eb2763e
# Fri, 24 Oct 2025 18:11:47 GMT
RUN Set-PSDebug -Trace 2
# Fri, 24 Oct 2025 18:12:07 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 24 Oct 2025 18:12:08 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Fri, 24 Oct 2025 18:12:09 GMT
EXPOSE 4222 6222 8222
# Fri, 24 Oct 2025 18:12:10 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 24 Oct 2025 18:12:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d7307306bfcd17eaeb00efbf6127b2df301ed63abbd9a720307ba2c78fe3cf`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d51dbfb4fb009c1d33f755c7b908dfccaef2a34d137217b52bf75183afe2598`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da2171bf9678c699d6934fb532b157e6fa6f1c3d995eae3f49d46700a0d0d36`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae9bd9f6e3c16688c8f3944c972e99914b4b88d2daa3f31d1391cc20224fd89`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91b69edfb2452aba8dad6cb0fe68f0fa7d34db85b010026ed81d09fab73dd62`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa4f4f2d8eaf3be2cbf7c860b0bf1596d1a1391ab4e0eb63c5751deea5c5b3a`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 490.9 KB (490867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33235eeb6c16d9e64b33a4ecc51071c17d3b2e3e11cf81a98b558075fc2dbdfc`  
		Last Modified: Fri, 24 Oct 2025 18:20:52 GMT  
		Size: 7.1 MB (7078239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a0da6d717dee72f35419de6f71da94e625b4df148b1c5403a5b48758ae7933`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecb326d65c52856210a041193fe524502414765ae5832bc33865e10eae2a67f`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8e9d625f467e53bf38f38564291ed7341e18e85be8247f661699a95730fab5`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116de05ff7102e1886d142218b36152664af8093a45533517aa878f7f72b312b`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
