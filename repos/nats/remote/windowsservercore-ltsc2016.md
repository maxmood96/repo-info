## `nats:windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:b192069a4cfd70392063967b2ce1090d6f8a094812fa4be622ffa35843463560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4530; amd64

### `nats:windowsservercore-ltsc2016` - windows version 10.0.14393.4530; amd64

```console
$ docker pull nats@sha256:491f727092d1f1cc50faa02fa4b0c23d1dec175367f55291964468853737ab05
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6279205071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69fec2ab6a3510ab48fb94d8e3122a4055cca848ef1c6e2560c443fc31346f2d`
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
# Wed, 14 Jul 2021 02:35:51 GMT
ENV NATS_SERVER=2.3.2
# Wed, 14 Jul 2021 02:35:54 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.2/nats-server-v2.3.2-windows-amd64.zip
# Wed, 14 Jul 2021 02:35:57 GMT
ENV NATS_SERVER_SHASUM=9278a3709c874f1dc5125fece7e7803e0cd4361cd97dc847826ef95838ea1e3e
# Wed, 14 Jul 2021 02:37:14 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Jul 2021 02:39:29 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Jul 2021 02:39:32 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Jul 2021 02:39:35 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Jul 2021 02:39:38 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jul 2021 02:39:41 GMT
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
	-	`sha256:f301246d6a689a00ca80c879c7036294c7c08f9628a3f7e143d00600f5fae9a2`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1135fddfb2a7acb97ec630ed1c2c9c9f7c53cdc995ae9ce746a18b8b67463f17`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c522e9c4ef7e0c5d6366bc22e9dd4ccd99d4e97501eec8ee9d83a0584f452e6`  
		Last Modified: Wed, 14 Jul 2021 02:40:54 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f11d018be60739ca143906be9e8a5d7833e083c9e76f9b4c5ad679dd62e546`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 325.3 KB (325309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef654d127a05fa7be2581174b3af9056cd84a24b53d639b29790480363fd13a`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 9.2 MB (9235231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62edb8d00046240ed89b64b658216821381a04ad85d9e93148a87633dceebad`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af7ff0ca1393713d4ada7de795553fe6e3ba4c1eb050652a87f27fc1cc293fb`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034662c21f82b31e87a354b8351637cedaeae62586649149d223908bd4c06b62`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07aed375d2f1ee02071c44422a10de0afa5fa38501cb09fa40125ad504ad6bd8`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
