## `nats:windowsservercore`

```console
$ docker pull nats@sha256:b4ea117f04e89579edaa6188eafdbef6055784a0047660c6bb700d903f89ec17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats:windowsservercore` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:fe81ecaa52b3ce46c4585d9ff37b9460df2000d8e578be32b783d8755d79de47
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2086858114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7538fd1adff11e803ab8d55b7fb5330bc9c83981d1ad53ed8afc11c85f8aa5b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 21:03:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Feb 2024 21:03:17 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Feb 2024 21:03:18 GMT
ENV NATS_SERVER=2.10.10
# Wed, 14 Feb 2024 21:03:19 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.10/nats-server-v2.10.10-windows-amd64.zip
# Wed, 14 Feb 2024 21:03:20 GMT
ENV NATS_SERVER_SHASUM=d135040811bbf093dc9eb84df2db3c895d497133278e4db70f6f5b26b421838c
# Wed, 14 Feb 2024 21:04:37 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Feb 2024 21:06:28 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Feb 2024 21:06:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Feb 2024 21:06:29 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Feb 2024 21:06:30 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Feb 2024 21:06:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3486482d07b6425fcc693b0eaca3c37fbd34ec9ca8b8989ee7127a5c75155b0d`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9208e581b9c7283ab14481c804d0a464b4bbdac158f620660c16336ac0ebc5`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b7900a7e40e25cf9a49361813019b840523589f63b88cd9f460ea7818dd6e0`  
		Last Modified: Wed, 14 Feb 2024 21:10:59 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ab0722f4a80745598d6babd4e5edf6ce8bb03ed12cac0b8d9de05968176853`  
		Last Modified: Wed, 14 Feb 2024 21:10:59 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b4b390fa9a839c252f1e5cf124f1b4fb8ef427c6984422883dc7ffaedc0f86`  
		Last Modified: Wed, 14 Feb 2024 21:10:58 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76adfd4e177603f832de0627ab7fe780bb147979f91181a1d927065176e5a5bd`  
		Last Modified: Wed, 14 Feb 2024 21:10:59 GMT  
		Size: 453.7 KB (453729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ffacbcae8201c661218817627c9057e822d5b397972d72d6b146af1f12ac2a`  
		Last Modified: Wed, 14 Feb 2024 21:10:58 GMT  
		Size: 5.9 MB (5943058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeeb6a20b408451e1bcb14a09667940baa9fd2d54a15d36d79f27cddc3833572`  
		Last Modified: Wed, 14 Feb 2024 21:10:56 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091b7200bd60a4619accfce7b247c33888ad8d44da89799ed0dd76227096dcce`  
		Last Modified: Wed, 14 Feb 2024 21:10:56 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d880a03742c13f9d62e7df46eb9bb0707f6166fc10f01a53d9878c50942d53`  
		Last Modified: Wed, 14 Feb 2024 21:10:56 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86dd4f84663c5c29a330fa9b500315e1a69d0779aa34255ebe694c1b6dccd18f`  
		Last Modified: Wed, 14 Feb 2024 21:10:56 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
