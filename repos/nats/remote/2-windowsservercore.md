## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:558501c81a867f2118fbfad7d8c7213e4e8021a4538caf4c716e68c0181368b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `nats:2-windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull nats@sha256:09992b8d678f6fd8e2a3707f974c2bb1541e411d40d8d5f310e1c0b7345f596e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2289612064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06aa3d694f337201e1178b83d69b6598b1f89ff4bb31842af5e27bc3edf2cdcd`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Mon, 22 Sep 2025 20:59:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 22 Sep 2025 20:59:58 GMT
ENV NATS_DOCKERIZED=1
# Mon, 22 Sep 2025 21:00:00 GMT
ENV NATS_SERVER=2.12.0
# Mon, 22 Sep 2025 21:00:02 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.0/nats-server-v2.12.0-windows-amd64.zip
# Mon, 22 Sep 2025 21:00:03 GMT
ENV NATS_SERVER_SHASUM=9e8a3a68f2f89e452d9777562e32f7f7604b0e4950f47b195d9192f2d8b35807
# Mon, 22 Sep 2025 21:00:59 GMT
RUN Set-PSDebug -Trace 2
# Mon, 22 Sep 2025 21:01:23 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 22 Sep 2025 21:01:24 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 22 Sep 2025 21:01:25 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Sep 2025 21:01:26 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 22 Sep 2025 21:01:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a72320f9f6632cb4daa3bb9d9a7c162905de55fd229f8543cdeb6b48ca301a2`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039463bd55f82b1af8358a228551dae320b37233e29b7edd048ed8f9ddb38efb`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b35d932f71b6fe1796a1ea4dbdd857282b33b799eb377f97fbc74b85475e51`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613b9503c3a85c640b072d8bedff7aca6947228931f317b645ad10861f1e10b0`  
		Last Modified: Mon, 22 Sep 2025 21:14:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b516d5be58c360dc3f16b71fdfc3798921bf14eeb9f8538c8c06411024406fc`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9eaecbab714c534c4b56eb4ec60d815e8823b3ef193aed0175f454c023dd15`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 363.9 KB (363863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b12f26cf9f027a03b2fb40f8ce56536cb605d38595f03212f1f183724ae8fcd`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 7.1 MB (7090875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c61c53885f769218328c139ee58909a061381a88f99bde516314e0921482ca`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 1.9 KB (1897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2bb5ab9f2574a4e263e1bdbb64502f119b6bd636a571067080fe9270a054824`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a08e0a654becd5b4e9d6ffd3e719be11327cc30a4dbd582a6c16639808f1a1`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978ee7da0a3eba879305069da987c91a20558418a038abe00b06f4828a1b4776`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
