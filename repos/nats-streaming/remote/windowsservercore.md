## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:0fd0290d10cf965f1222f90fa114908b384cb8a816e81780143f32e89185a017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2114; amd64
	-	windows version 10.0.14393.4583; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.2114; amd64

```console
$ docker pull nats-streaming@sha256:d6ba04cfbedbf1ce9e219918c40dd6989e1d50a8e2398bb1d69fb19597056636
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2694026981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54951a15532bfdfb9b767cb2b92cb384b91b1c66f44a6cfb259769a168458b7f`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 25 Aug 2021 13:46:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 25 Aug 2021 16:05:30 GMT
ENV NATS_DOCKERIZED=1
# Wed, 25 Aug 2021 19:31:01 GMT
ENV NATS_STREAMING_SERVER=0.22.1
# Wed, 25 Aug 2021 19:31:02 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.22.1/nats-streaming-server-v0.22.1-windows-amd64.zip
# Wed, 25 Aug 2021 19:31:03 GMT
ENV NATS_STREAMING_SERVER_SHASUM=4516852b493111b73ec06477be4a27e66f5abc9ca1ff4dd2b970232271611264
# Wed, 25 Aug 2021 19:31:55 GMT
RUN Set-PSDebug -Trace 2
# Wed, 25 Aug 2021 19:33:24 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 25 Aug 2021 19:33:25 GMT
EXPOSE 4222 8222
# Wed, 25 Aug 2021 19:33:26 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 25 Aug 2021 19:33:27 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:985da5cbc0735e1c422e766af23125ba345f431cb337ea43ec32298d0bb8e4ea`  
		Last Modified: Wed, 25 Aug 2021 15:45:02 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3dbdd68a4b0c278695b3e1d401d7eddfb0f0e3aa1e28aed88eb700059648f8f`  
		Last Modified: Wed, 25 Aug 2021 16:11:02 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d02eff460789c6fa51a517221660dddad01c753689cf4d911deed4be925fdfa`  
		Last Modified: Wed, 25 Aug 2021 19:36:40 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67c923b3231b172039016dd78d64494840a068f83b7c2eb0610b3916e0f880d`  
		Last Modified: Wed, 25 Aug 2021 19:36:40 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c73a6e9ff96bac535744e077e3966558cf33b742d3b384e6b77e72d96b4a49`  
		Last Modified: Wed, 25 Aug 2021 19:36:40 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652b4bfafc795b6a09e751ef642f31936038547b6223596beda9dc1bbd74f2df`  
		Last Modified: Wed, 25 Aug 2021 19:36:37 GMT  
		Size: 372.7 KB (372655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d3118388d00fe0ce41388dbed69f505de317c0d9a6551664b34909e0308b85`  
		Last Modified: Wed, 25 Aug 2021 19:36:48 GMT  
		Size: 7.6 MB (7645717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35fd537c3fc591dceb1461535c52fc98243ac3b3fea45db58c6ebc492862440c`  
		Last Modified: Wed, 25 Aug 2021 19:36:37 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f9050479fb189fc4a85ae128bcc6a114f42e9139901390f4c6ef669c1ce49a`  
		Last Modified: Wed, 25 Aug 2021 19:36:37 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e587562615088e9b1f845a826539d4c81323caf3b84153496ac0f3c1c8afc45`  
		Last Modified: Wed, 25 Aug 2021 19:36:37 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:windowsservercore` - windows version 10.0.14393.4583; amd64

```console
$ docker pull nats-streaming@sha256:b122147602333b9a276aa52c700aae01f366dcad7b0d79a86009a7f8313bbb5a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6278962413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624e3804e5c78766e9c54be1e5b1be3e39dd9aa56935b2944e21531a991f5377`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 01 Aug 2021 08:52:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 25 Aug 2021 13:59:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 25 Aug 2021 16:08:06 GMT
ENV NATS_DOCKERIZED=1
# Wed, 25 Aug 2021 19:33:53 GMT
ENV NATS_STREAMING_SERVER=0.22.1
# Wed, 25 Aug 2021 19:33:53 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.22.1/nats-streaming-server-v0.22.1-windows-amd64.zip
# Wed, 25 Aug 2021 19:33:54 GMT
ENV NATS_STREAMING_SERVER_SHASUM=4516852b493111b73ec06477be4a27e66f5abc9ca1ff4dd2b970232271611264
# Wed, 25 Aug 2021 19:34:35 GMT
RUN Set-PSDebug -Trace 2
# Wed, 25 Aug 2021 19:36:09 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 25 Aug 2021 19:36:10 GMT
EXPOSE 4222 8222
# Wed, 25 Aug 2021 19:36:10 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 25 Aug 2021 19:36:11 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c427f892fe74603ae09d4e49b25f8f7046f957054034dc9f462e0e88d7bffaa5`  
		Size: 2.2 GB (2200980134 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a869803fc3d8292f0fe1bc6ed35e1ceedbd7c797a1486767a55f88c6c28ed4c5`  
		Last Modified: Wed, 25 Aug 2021 15:45:25 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a745f96c10790ef3a2006dbd4c116eb2f1552fd3c4a38fca179a8160e9918ac1`  
		Last Modified: Wed, 25 Aug 2021 16:11:42 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb2b2f51b28100175c4c31970f69c26566bea4ec51d87a91555fe5091be241f`  
		Last Modified: Wed, 25 Aug 2021 19:37:17 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23161af967280f0d95595b25ca572083145ff8330ed8248c015bf100be1c838`  
		Last Modified: Wed, 25 Aug 2021 19:37:17 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b49b5a10129016e785edeb8fba72f2d2a8658e8239af2b0fe530c3ae5a53c5`  
		Last Modified: Wed, 25 Aug 2021 19:37:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b369c4a91f133df3608ec1e4cbb5ab7020ac16c0db6684465e735fc719da9a9`  
		Last Modified: Wed, 25 Aug 2021 19:37:14 GMT  
		Size: 336.8 KB (336786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc65df0e7918917488aea97873a4358dfad7b2914701e183c0865d4174c0dd62`  
		Last Modified: Wed, 25 Aug 2021 19:37:22 GMT  
		Size: 7.6 MB (7649022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131ab6c361a3936d54c3e6d59a85f42d4171d9639f2c4feadb13b7eae8e9ff52`  
		Last Modified: Wed, 25 Aug 2021 19:37:14 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cabe016e1cfca773de7a8d1279fe766c82e6e6e91a9cff7c4725c06a13baa8c`  
		Last Modified: Wed, 25 Aug 2021 19:37:14 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf87ca03d1c93fa8e08d0c4be5fc32f8e091424df743e3aeab09d8dd776e5e6`  
		Last Modified: Wed, 25 Aug 2021 19:37:14 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
