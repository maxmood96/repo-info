## `nats:2-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:8b2a59ae57dabb40a530adeb549ffea14e796eb0bd68bc15a409f07e475ef4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:a25b38871b87a691f7c5c90cfa83f4d5437e88f040de6348cbf95733ba375ef1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130333999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ec1a6204be33c8779d1a1fcf3ab70fffb3bb380e02f6d1a3f84d2b8acb1bd0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 02 Jun 2026 19:07:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 02 Jun 2026 19:07:32 GMT
ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 19:07:34 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:07:36 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:07:38 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.2/nats-server-v2.14.2-windows-amd64.zip
# Tue, 02 Jun 2026 19:07:40 GMT
ENV NATS_SERVER_SHASUM=0ae94fc0626c89e76a95835445e36c8b1b595c00d71690966ad208f5f04392ae
# Tue, 02 Jun 2026 19:08:48 GMT
RUN Set-PSDebug -Trace 2
# Tue, 02 Jun 2026 19:09:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 02 Jun 2026 19:09:18 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 19:09:19 GMT
EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 19:09:19 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 19:09:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e8fbbec164e39825e72121dbf863209aaee281bb23d82eef45fb1b78af49bd`  
		Last Modified: Tue, 02 Jun 2026 19:09:27 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5ccc46ac0cd69fc7e5f3ba3187243d7191826c5c174d7d1a9bdf7e37437430`  
		Last Modified: Tue, 02 Jun 2026 19:09:27 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df3be6447ed8966ff4760ab36a8f65bde11ddb128890296ca784007be596571`  
		Last Modified: Tue, 02 Jun 2026 19:09:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0a04302c8e00c75114f3a2244ff5f034702d2bd875699c15d6aa753d729d94`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342b68571adc336abfdc2b191feccc656c90c865b349c3419f6d4ca6392defa2`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b755e2e1bb5b7b315f0510306d019a8ee93d6cba431bfe70f2fde14f269625d9`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8f4cf7f1be61cbdf08314357d2af1b7b697606166b30d6e09ad275f8c29a41`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 503.2 KB (503180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614768606c9a6a992dc318e3eedb9a3985d9320f1503b7b5001d9a916880349c`  
		Last Modified: Tue, 02 Jun 2026 19:09:25 GMT  
		Size: 7.4 MB (7396537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8698093e1cf89fed3786ae358d5758de15cc759aaf437f55e51155301c09d115`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f5276da588ba1823566c8e1634c157a72c38c9dbaab53122d796fb3207e83e`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba365b70485c1a2db1e0c6856a41d0a634ba9ef55bd72ebd8b86f5e617508ede`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2450f660cf8c8ababe39a2710f184cc802c5ab5f133180075efd69d6ce35116e`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
