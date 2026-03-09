## `nats:windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:c91c98a2c0f9e1201ce950a576a16a68fe9783b0b6cc1a2fc224df32aefb5023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `nats:windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull nats@sha256:a61f936611e277e770cef1b7230218f2998d66e741f5eb9ae26b4a157cf5bf71
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1870342697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3593bdd5088c3a2186450f3ec67c2b1b24dc05580e5de499e17c34b7e085851`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Mon, 09 Mar 2026 18:32:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 09 Mar 2026 18:32:15 GMT
ENV NATS_DOCKERIZED=1
# Mon, 09 Mar 2026 18:32:16 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 18:32:17 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 18:32:19 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.5/nats-server-v2.12.5-windows-amd64.zip
# Mon, 09 Mar 2026 18:32:20 GMT
ENV NATS_SERVER_SHASUM=29d6eca9ce085731bd63b32eeff7fae076938d31dd095acccfc70f2496d07ea7
# Mon, 09 Mar 2026 18:32:44 GMT
RUN Set-PSDebug -Trace 2
# Mon, 09 Mar 2026 18:33:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 09 Mar 2026 18:33:06 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 09 Mar 2026 18:33:06 GMT
EXPOSE 4222 6222 8222
# Mon, 09 Mar 2026 18:33:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 09 Mar 2026 18:33:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d981d44f9a73d3b8117934af1bd55be51f3be889d584f55580c32c43344b818b`  
		Last Modified: Mon, 09 Mar 2026 18:33:15 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48113d5ee1472c1abbd6f07308981c5501f252ca8e6f744d1e3bfcda61c86e81`  
		Last Modified: Mon, 09 Mar 2026 18:33:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea810515587d754733aa4d5c64441823eeaf29c52d819469ab2935b6ce2e9929`  
		Last Modified: Mon, 09 Mar 2026 18:33:15 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b135b7025028e4a05b5de8e80f92ba477d820b2f18df307610f3f55e2813e939`  
		Last Modified: Mon, 09 Mar 2026 18:33:14 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8213b71e9da14b21094a1b11e880bf1328a146efaa14a80eda89f3514c5da2b4`  
		Last Modified: Mon, 09 Mar 2026 18:33:14 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c10ad115281eabdb32190d3a97cac7b90e85241abaf4257f88ec1ac6a48274`  
		Last Modified: Mon, 09 Mar 2026 18:33:14 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f2163d32b8d29385ef65fbab33d8621f869188a38d83a7e1a1296eaa44ae6e`  
		Last Modified: Mon, 09 Mar 2026 18:33:14 GMT  
		Size: 497.6 KB (497616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0854c5b6aaf7b32d7c5106183b2ca967e093c695b61ae92c2e7d7cce37f25c26`  
		Last Modified: Mon, 09 Mar 2026 18:33:14 GMT  
		Size: 7.2 MB (7174263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf56a1c80eb5969fc4d6f3bfb0a5a88a7fd38d505cd708934b3bdef93186ef7`  
		Last Modified: Mon, 09 Mar 2026 18:33:12 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8912ae2f28d5544ec3d636ccbd0788d20f6c5964b84cc829c3d72831376706a`  
		Last Modified: Mon, 09 Mar 2026 18:33:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f9dcf419a47d35d6e029313fb5ba5f86c73da99e8d0f0ae908b0b8a427762f`  
		Last Modified: Mon, 09 Mar 2026 18:33:12 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8c31cb4f1978494c82d29fe1454311700e0794247abc6e581f4eba9941e4b5`  
		Last Modified: Mon, 09 Mar 2026 18:33:12 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
