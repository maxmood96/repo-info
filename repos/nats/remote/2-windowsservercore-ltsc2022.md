## `nats:2-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:217c6a522081d3fe0db0fe837fcf746fc680b43c858480cde3100999215cdc50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `nats:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull nats@sha256:32572d0121c3da0061e431ce739957c70f407ff41f727e24ff8685b22b02db87
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1870296672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9901fcd0212b354dae1e22803de6ba4b8745afa4967bc1a8d158cd7817a3cb52`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Tue, 10 Feb 2026 22:53:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Feb 2026 22:53:41 GMT
ENV NATS_DOCKERIZED=1
# Tue, 10 Feb 2026 22:53:42 GMT
ENV NATS_SERVER=2.12.4
# Tue, 10 Feb 2026 22:53:43 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.4
# Tue, 10 Feb 2026 22:53:44 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.4/nats-server-v2.12.4-windows-amd64.zip
# Tue, 10 Feb 2026 22:53:46 GMT
ENV NATS_SERVER_SHASUM=99efb643ef399299ed5736e4fc7220551e8450fe9351adc3c2f678b5737815f5
# Tue, 10 Feb 2026 22:54:04 GMT
RUN Set-PSDebug -Trace 2
# Tue, 10 Feb 2026 22:54:24 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 10 Feb 2026 22:54:25 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 10 Feb 2026 22:54:25 GMT
EXPOSE 4222 6222 8222
# Tue, 10 Feb 2026 22:54:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Feb 2026 22:54:28 GMT
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
	-	`sha256:7956f5ffa15a400fe4905921a932f0612357f6db74ba106c217282ed10c18d62`  
		Last Modified: Tue, 10 Feb 2026 22:54:36 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133be5d7f3fed421e8cf3fd0552815824e31b7ca2f50264b0dc898aee607627e`  
		Last Modified: Tue, 10 Feb 2026 22:54:36 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4093f674f67bd250957712a364c4b031ecbcde0d8f737714a109aa6310abc9`  
		Last Modified: Tue, 10 Feb 2026 22:54:36 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d17e24e9facc12d3ef84240431f1374737f9c53a8d45947652f676f7e66e17e`  
		Last Modified: Tue, 10 Feb 2026 22:54:34 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da974e57a91c96119b033a48455fa48e0f40461f3d67ce764ae4fe26fab7963`  
		Last Modified: Tue, 10 Feb 2026 22:54:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06194d5db0799b67c3742286bd8ff995c0a89d983dec8c5ed00d95c4c94c193a`  
		Last Modified: Tue, 10 Feb 2026 22:54:34 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b4d8e3fadf34383f7917204ad7a6cef55c7cfc1261b0b8fe0ba3cf4634f1ef`  
		Last Modified: Tue, 10 Feb 2026 22:54:34 GMT  
		Size: 491.0 KB (490983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be105b1ab2dc7b0f3c864943547b46c21007b5ddc18226701cb0f305576e251`  
		Last Modified: Tue, 10 Feb 2026 22:54:34 GMT  
		Size: 7.1 MB (7134920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea626997c0b78b63dfaaaa5c5411a090dcfe00fe83eab5e8787a020bc7473df`  
		Last Modified: Tue, 10 Feb 2026 22:54:32 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765918d9c0dcbcd0792797631b37a482e01e1ba24c03ae360657e83efab1c57e`  
		Last Modified: Tue, 10 Feb 2026 22:54:32 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb4fe93c6ff2875328222a23589f3c473d123349b0b417a6e46e8001dad731e`  
		Last Modified: Tue, 10 Feb 2026 22:54:32 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be36063b8f64654bd84131d13a28b49826e095ae1db908974d88bf96696758df`  
		Last Modified: Tue, 10 Feb 2026 22:54:32 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
