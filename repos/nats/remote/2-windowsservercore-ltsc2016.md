## `nats:2-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:b54ef6b58efd31523be8c864e843428ca2d8976ce534b058079a389666f4fa90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4402; amd64

### `nats:2-windowsservercore-ltsc2016` - windows version 10.0.14393.4402; amd64

```console
$ docker pull nats@sha256:a1afdd3ea8f102dcc62a70bfb082588bc4b184becad2469e752c8e126ab6df53
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5815946596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b825a3f2e49865904aba44cc6f5a2c8b80c0189b1c372477e32ad2c3545888`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 26 Apr 2021 17:25:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 May 2021 23:58:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 May 2021 15:44:16 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 May 2021 15:44:17 GMT
ENV NATS_SERVER=2.2.3
# Wed, 12 May 2021 15:44:18 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.2.3/nats-server-v2.2.3-windows-amd64.zip
# Wed, 12 May 2021 15:44:19 GMT
ENV GIT_DOWNLOAD_SHA256=7f1ad2f52a6983b2ef9a1bf909ecebe2d0d3c3f5a84b84dacc63bf7fd8948c46
# Wed, 12 May 2021 15:45:40 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 May 2021 15:47:49 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 12 May 2021 15:47:50 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 12 May 2021 15:47:51 GMT
EXPOSE 4222 6222 8222
# Wed, 12 May 2021 15:47:52 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 May 2021 15:47:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7f532f88613ca85064b055f6b93f8517bd05feba8fdce495a6ad1421573e765e`  
		Size: 1.7 GB (1725791397 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:50d0f4595a2bdc5dc0623fbee162be09d0631373eb9e82a0b1ec387ce1512c49`  
		Last Modified: Wed, 12 May 2021 00:46:32 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7998d92dbbcfc4e6dc106e75206a3cfde70fe601eb46b0515658f23dcd53ae`  
		Last Modified: Wed, 12 May 2021 15:49:26 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6646c0a4909dd219ffb3eb6eb3709b768fde40ba969a0416a73716211f2a2ef1`  
		Last Modified: Wed, 12 May 2021 15:49:24 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d117e0e9fd386f6d4c004ecf8c18fe24981e5dcf7396ba7935598c16d63d2e24`  
		Last Modified: Wed, 12 May 2021 15:49:24 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c98fa15ec3d078cc3f3da05a4adc67ef14ad1abad5f9e06af54f26121a1d298`  
		Last Modified: Wed, 12 May 2021 15:49:23 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac43c7bec6bd3c410f67cd8fc3336f2ff913251c6251c48f877908df661c8ab3`  
		Last Modified: Wed, 12 May 2021 15:49:25 GMT  
		Size: 5.7 MB (5705594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af8fbf17e86d247bfd4abf90eca1d1e8682d466716786f01230a300844d893f`  
		Last Modified: Wed, 12 May 2021 15:49:24 GMT  
		Size: 14.5 MB (14450465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236726b5e955bfd7dd64337c1e1f23a903cfa204639b0a377b13f86297815f66`  
		Last Modified: Wed, 12 May 2021 15:49:20 GMT  
		Size: 2.0 KB (1978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231f23209351216b06233ad4059b5a5e3eef3e3f5d38896f2306d69bca7efa56`  
		Last Modified: Wed, 12 May 2021 15:49:20 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64daeb968b2f9ad52152de233e969ab4a7acbd81b939b6d12ce9476c61284b7`  
		Last Modified: Wed, 12 May 2021 15:49:20 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6af4f8b0031c6ff433713d50b0f460a68c589538710d23ff6b592b4b1e575e`  
		Last Modified: Wed, 12 May 2021 15:49:20 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
