## `nats:2-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:30c6818895521b905434c83a874393e80e00eeb16c99cb406aabc52f6e841305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:d40e99fe0996b55c987f43318922f0126afdf833dc64b80e4f671b914e531139
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2140004525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5f698c6ee75b2e0c38f746a238c8b58fc571f69d8b228708313334088f21b5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Jun 2026 22:09:23 GMT
ENV NATS_DOCKERIZED=1
# Tue, 09 Jun 2026 22:09:25 GMT
ENV NATS_SERVER=2.14.2
# Tue, 09 Jun 2026 22:09:28 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 09 Jun 2026 22:09:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.2/nats-server-v2.14.2-windows-amd64.zip
# Tue, 09 Jun 2026 22:09:30 GMT
ENV NATS_SERVER_SHASUM=0ae94fc0626c89e76a95835445e36c8b1b595c00d71690966ad208f5f04392ae
# Tue, 09 Jun 2026 22:09:49 GMT
RUN Set-PSDebug -Trace 2
# Tue, 09 Jun 2026 22:10:13 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 09 Jun 2026 22:10:13 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 09 Jun 2026 22:10:14 GMT
EXPOSE 4222 6222 8222
# Tue, 09 Jun 2026 22:10:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Jun 2026 22:10:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09f22a9628ef0d5b0cc16feadb876572bfdd0fed92378ff8e8777f451c62ae3`  
		Last Modified: Tue, 09 Jun 2026 22:10:23 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a64864617250f652dc21c56c17bc9e201bd6efaaaada8ecb0a289739097c68d`  
		Last Modified: Tue, 09 Jun 2026 22:10:23 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963c12e26fa7cc56f2895b0da6e1e2d663354df97d44ac2608b1b8a1e2efa36f`  
		Last Modified: Tue, 09 Jun 2026 22:10:23 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1b3ab9ee4bdedf123268ce980d9b19d98aa3d3de2daf1d225b362a2d2ec90f`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080f2b59d6248c1199ff79acaba8ff2fa41389c65f9a3408b946e558476599ce`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8304c7e0c6a110a2e1de5b1db6ee30548c1f9b35cdb8bf2dc2d8943f8e98ece`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faefef94c2375e90b22da5d12ab47156f4ee851848a1c5659e082cf88d307f1b`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 482.4 KB (482407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6105388623f6f433b4ca5aa8d008cd1aa1e17cbfc5fe71d61e59bb6dc076eeb8`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 7.4 MB (7382856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f98553f597398b2c6201727d08ba6c5c0f84e754f2ea050675bb48eba199a8`  
		Last Modified: Tue, 09 Jun 2026 22:10:20 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6358666bb0ef21de38462ae43661dca2ddf92df690f233904c8846efeea044af`  
		Last Modified: Tue, 09 Jun 2026 22:10:20 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ed5830658244188816a211d85b730ad98d8a17d9356480f8b99bbf4249b58c`  
		Last Modified: Tue, 09 Jun 2026 22:10:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462c0f6d3e6997ffe7696032948f9230f3093a8323b995cb6636f7fab7a04bb9`  
		Last Modified: Tue, 09 Jun 2026 22:10:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
