## `nats:windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:7d611980e8b0160efe98f0d693f97b1733f156f87a1fbba62f20d8264d2296a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4530; amd64

### `nats:windowsservercore-ltsc2016` - windows version 10.0.14393.4530; amd64

```console
$ docker pull nats@sha256:d6a80df594b9c79713e2e081ee4745d866c2e22d200cf6c6313bcfd3c11dab24
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6274950599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d32b272b39dcd6b458d9516034bb382ae8d518db805e3fbcf74057d97981a6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 09 Jul 2021 05:02:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Jul 2021 01:14:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jul 2021 02:35:48 GMT
ENV NATS_DOCKERIZED=1
# Thu, 05 Aug 2021 01:17:24 GMT
ENV NATS_SERVER=2.3.4
# Thu, 05 Aug 2021 01:17:26 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.4/nats-server-v2.3.4-windows-amd64.zip
# Thu, 05 Aug 2021 01:17:28 GMT
ENV NATS_SERVER_SHASUM=729dc0609e0461aa5fb893c85c04c6b6afa40945183d8d8324d03186d1678a99
# Thu, 05 Aug 2021 01:18:30 GMT
RUN Set-PSDebug -Trace 2
# Thu, 05 Aug 2021 01:20:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 05 Aug 2021 01:20:07 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 05 Aug 2021 01:20:09 GMT
EXPOSE 4222 6222 8222
# Thu, 05 Aug 2021 01:20:11 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 05 Aug 2021 01:20:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a567de41cc349380b25967f180fb1b6b2431bda61ccaaf69d78a33bc9523614a`  
		Size: 2.2 GB (2199646155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fed351b78c876c55ec9c7e75d3b9d1b146c5c5dfeb4b5480c0a7c384322df98c`  
		Last Modified: Wed, 14 Jul 2021 02:03:37 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf08cae8b8db8f3f89e1a9192d393f2da55b44efce4e778fdb58debe2d608275`  
		Last Modified: Wed, 14 Jul 2021 02:40:57 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1c44d1c9a8f9d7ad841c012f6de896b6b36c94f648f369709ec714de6a0561`  
		Last Modified: Thu, 05 Aug 2021 01:21:25 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a36861d11e97c8f3cd60182e69d6547fd3c7dd681fd5b892bf674d263cfa55`  
		Last Modified: Thu, 05 Aug 2021 01:21:24 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2af8594f437c6c2c3ae701f3a8ef3f49d2860254568fe9cdcb902236a8b2ea`  
		Last Modified: Thu, 05 Aug 2021 01:21:24 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847d098f9f9ff94b78c44a267a8eee1f258171e94527ef03da4e0a2e4630720c`  
		Last Modified: Thu, 05 Aug 2021 01:21:24 GMT  
		Size: 364.9 KB (364876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce96aca778ab04bb9b2b258bb6c0b4af50f1293387a21bb7ecab954e1df51f7`  
		Last Modified: Thu, 05 Aug 2021 01:21:23 GMT  
		Size: 4.9 MB (4940388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86c1babce557e9804d282d3f84516018239e1953d2f331882c347ab4405c0af`  
		Last Modified: Thu, 05 Aug 2021 01:21:21 GMT  
		Size: 2.0 KB (1968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ac7eea6fd5241c5e955f00a169cfbec20397f9a877ccef20e110666b809032`  
		Last Modified: Thu, 05 Aug 2021 01:21:22 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f36c1ea25dfc115b0ec159e748c702ce956653eda92844ecf60770259892cc5`  
		Last Modified: Thu, 05 Aug 2021 01:21:21 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36bfc5e3a0934ddca0f2028862fe5255420db252cc34f75fcd7707565180e3a`  
		Last Modified: Thu, 05 Aug 2021 01:21:22 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
