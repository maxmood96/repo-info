## `nats:windowsservercore`

```console
$ docker pull nats@sha256:cd40ad4037d8bcb19778d0ec3407978059ea88d895747dfce3ea1be3f83f5760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:ff0d0047ceb610a0b73edcb6d12305bdf06e08a127258cf923e1aec9645ec419
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2288892735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe5b93e3cd45a63955014ff0d53cf5383f91b868d6bacf1c242ce4861d0a3fe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Thu, 14 Aug 2025 17:24:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 14 Aug 2025 17:24:18 GMT
ENV NATS_DOCKERIZED=1
# Thu, 14 Aug 2025 17:24:19 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 17:24:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.8/nats-server-v2.11.8-windows-amd64.zip
# Thu, 14 Aug 2025 17:24:21 GMT
ENV NATS_SERVER_SHASUM=3dd98465626e8c6ed92a784ef13c3f956c7e87fbbb4ee86cc198e377565eaeaf
# Thu, 14 Aug 2025 17:24:28 GMT
RUN Set-PSDebug -Trace 2
# Thu, 14 Aug 2025 17:24:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 14 Aug 2025 17:24:44 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Aug 2025 17:24:45 GMT
EXPOSE 4222 6222 8222
# Thu, 14 Aug 2025 17:24:46 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Aug 2025 17:24:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3f006d1cb294833347c0dcdeff82dda52af9acbea696337fd8408869317713`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e0fe1f9e451f5b78de6f2eabbcf9dd583e44cc8efca284c024e6fc31fea206`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4c9efb293cf4538944d58d49d978df5a06ed2586f43c0312291c6ed0854b98`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4fcdec518a7d5e9cbdbb2398711d526df04c6abd46f6dc74c91ce20cb62a28`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f32d8dbe729b86cde1eafd2da61359f32dab9aa4ff767aa70b3dc9351ba01c3`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1453289e44dd8e7a29b2a8395640bb6a2e2ebd47060a6bfe129031ce2072d7`  
		Last Modified: Thu, 14 Aug 2025 17:26:08 GMT  
		Size: 336.2 KB (336246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db38558f3d85860c055f99e79e865d42a17dd691a4f83ea93e0f8a5e391d125`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 6.9 MB (6852407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb87097b18d82c7dc42b80c5f6912e34cd08ecb316ffd445266fbb02ee18352b`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828b5772011538e3bb3bd9055b2b9e9b10bb6ffd46dc54a1d765d3e2dcfb03a6`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd3abb758a5b3c339001a04d7364df2b54b00e27711aecf5f44a76323ef676f`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366367ce039c79734b9ad15e13867ea0fd5f18ee46cc185dde59b3507a9b3392`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
