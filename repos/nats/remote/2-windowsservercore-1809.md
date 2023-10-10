## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:0987e4605a3a22dce3598ec052621ba8ac2688f06a87001fdedd79b03f9a58ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:c551f774b1a4e50e377c61ac629700b520ad2b5157e11d5bd926b6d27b10288d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2022628787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac884d71c8f8413c688b4b8892c59d8d0791c9a74cf83af92a152eaf59065058`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 29 Aug 2023 17:09:18 GMT
RUN Install update 10.0.17763.4851
# Wed, 13 Sep 2023 03:56:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Sep 2023 05:05:36 GMT
ENV NATS_DOCKERIZED=1
# Tue, 10 Oct 2023 00:15:01 GMT
ENV NATS_SERVER=2.10.2
# Tue, 10 Oct 2023 00:15:02 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.2/nats-server-v2.10.2-windows-amd64.zip
# Tue, 10 Oct 2023 00:15:03 GMT
ENV NATS_SERVER_SHASUM=ce8eed07736cc6e008b0d26808ec0cae5871a419d8e38b020cfd121d0f88b935
# Tue, 10 Oct 2023 00:15:59 GMT
RUN Set-PSDebug -Trace 2
# Tue, 10 Oct 2023 00:17:33 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 10 Oct 2023 00:17:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 10 Oct 2023 00:17:34 GMT
EXPOSE 4222 6222 8222
# Tue, 10 Oct 2023 00:17:35 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Oct 2023 00:17:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179757339e051b99f9a62375fed8f87ffcc4df0eeedb984d20b485bdd089ad08`  
		Last Modified: Tue, 12 Sep 2023 19:41:25 GMT  
		Size: 365.7 MB (365709508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b21bbf840142288ae2bce3465085b591133cf10f78f7dda43277db4838332d8`  
		Last Modified: Wed, 13 Sep 2023 04:36:45 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54f616fe064e9d4e73bf2aec9a4fe9c58837ec84c2fc998a54ab7a77b52e109`  
		Last Modified: Wed, 13 Sep 2023 05:08:32 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47719ca95def3ac4a93a0bfcd3bce32d0329da6a4505d20c954d15de4ab8839`  
		Last Modified: Tue, 10 Oct 2023 00:18:34 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfc1820bc3dc99cc9f150e546646668b573047a3d1c7bb88827712e6809ac62e`  
		Last Modified: Tue, 10 Oct 2023 00:18:34 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996fb0318eac725d5efd2d750caa9d17a30aca592f9af439dcb2fea76e2be3b9`  
		Last Modified: Tue, 10 Oct 2023 00:18:34 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb619629f8cb29a2eb4c863d28b2c661b953c5e6531438c767a1aedad6f0e8d`  
		Last Modified: Tue, 10 Oct 2023 00:18:34 GMT  
		Size: 242.9 KB (242914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a60e8d303076fe03f915b3f1e9e84663c01559c6b869ee02d78d053eaea5b3`  
		Last Modified: Tue, 10 Oct 2023 00:18:34 GMT  
		Size: 6.0 MB (6042725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c5e3620ea18091039cbe627800ad0f13cc1137deb10c0387a498d5b93ab3dd`  
		Last Modified: Tue, 10 Oct 2023 00:18:33 GMT  
		Size: 2.0 KB (1965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07582ea268df1b282107d66e0569f5f018e740ea3272ec51ebd9c5615e309376`  
		Last Modified: Tue, 10 Oct 2023 00:18:32 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41397f0185b0d94c74926402aa966ca83d9f27b4d7b815a0128f63216c880428`  
		Last Modified: Tue, 10 Oct 2023 00:18:32 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a772aa3a10ac68cfdbbbcca8b2985f2b84c28ac72c872bd6df7100592e67aea1`  
		Last Modified: Tue, 10 Oct 2023 00:18:32 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
