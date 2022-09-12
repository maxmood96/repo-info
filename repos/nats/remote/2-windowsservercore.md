## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:b37318e22e6c2bca5e2d092fbab4905b4dd53290044c8dbd8cbd677261d3a9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.3287; amd64

```console
$ docker pull nats@sha256:4a559a5453abebb4d56e482d381590b2b1d61191be333c254172c1d27773a84b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2683377209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0f6380d1357690f0092632218fce699a83134468e03023479e9e67e7317588`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 06 Aug 2022 18:30:32 GMT
RUN Install update 10.0.17763.3287
# Wed, 10 Aug 2022 13:44:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Aug 2022 15:27:50 GMT
ENV NATS_DOCKERIZED=1
# Mon, 12 Sep 2022 19:16:00 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:16:01 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.0/nats-server-v2.9.0-windows-amd64.zip
# Mon, 12 Sep 2022 19:16:02 GMT
ENV NATS_SERVER_SHASUM=7bd8f5e4940b67e34cffddbaad058f1d2af1c3bd326dd2879528a6cb72c6a4ac
# Mon, 12 Sep 2022 19:17:19 GMT
RUN Set-PSDebug -Trace 2
# Mon, 12 Sep 2022 19:18:50 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 12 Sep 2022 19:18:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 12 Sep 2022 19:18:51 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:18:52 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 12 Sep 2022 19:18:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:294d77ac553d7210b662d07674ef9e39a6c2e88dc15b9d2788d51e509bc8b54e`  
		Size: 800.5 MB (800546641 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:da71148bcd96afa7027d6172acee93aad6002bfbe87cadf468260667c09b3a89`  
		Last Modified: Wed, 10 Aug 2022 15:05:54 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dc1c1069568772f0068cef343e37284e5f5e488dbfc15e037d95bce032d917`  
		Last Modified: Wed, 10 Aug 2022 15:30:56 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5dc5196335dbb75c5b511c3b7f88d1ea863a5fd9c948ed2284c61bce8d05f7`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cab5aeb6f1c72acf727c92921b388759093ed4f8109a731f08a93ccce6df92`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221a14b7e5d70af9acd178b843943bf573128c25c44b9085c9afb843132d103f`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0945be30f32456b0704b1bf873985926e899f43099f0473ac39a6b1bc59dce55`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 355.5 KB (355476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f9c99958ecc108eb4d345fcce1858463fbca041d04da8f36ffb117bf0b34b1`  
		Last Modified: Mon, 12 Sep 2022 19:19:47 GMT  
		Size: 5.3 MB (5295678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ddb96d7096a0d1a680c5ff1fe7b31e8135bef30b4f0fe5b9290ec90520213e`  
		Last Modified: Mon, 12 Sep 2022 19:19:45 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238f15e23683198de7411b9a1a6508b91b3e7a2335b39bc952824eaa754d27d3`  
		Last Modified: Mon, 12 Sep 2022 19:19:46 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af56027e9880bd41ea09c2f65aa361a6f3a8d18b43c467f3aa55d8eb0497778`  
		Last Modified: Mon, 12 Sep 2022 19:19:45 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1693476cfeceab25d4ab31b997456d983001a60e1d7f0e9256423648e0acc357`  
		Last Modified: Mon, 12 Sep 2022 19:19:45 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
