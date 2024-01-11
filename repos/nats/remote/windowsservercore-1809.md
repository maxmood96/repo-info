## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:3c45a5aa02ed8b5abb2bb7e1bd23820c814722e04dcba27e53467c7b51187d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:7646add34d96720013cda9262f8f799793ffda44b5990ad5fadc169bcdbfdda5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2076059383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b34b0a476ad4184a540f5d9c5af99dcb407bcc8a691407375bce4e45806bb4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:11:23 GMT
ENV NATS_SERVER=2.10.7
# Thu, 11 Jan 2024 00:11:23 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.7/nats-server-v2.10.7-windows-amd64.zip
# Thu, 11 Jan 2024 00:11:24 GMT
ENV NATS_SERVER_SHASUM=92c4883cdf608c1e096feabcc9a0f46935ba34fce72210520ba2e66207968630
# Thu, 11 Jan 2024 00:12:22 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 00:13:56 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 00:13:56 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 00:13:57 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 00:13:58 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 00:13:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffde501e47c09b0f152cc1497c82477ce0c6c078482b1fa8d88e78279cbdd36`  
		Last Modified: Thu, 11 Jan 2024 00:17:47 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7a05a9cc4a7074e0c902afd3da9d05a311e38461deaca2f08837eaefcd1e39d`  
		Last Modified: Thu, 11 Jan 2024 00:17:47 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78625a69c655e225c9bd0fe8e4d1379ec8d94a80228d484fede0f800ce2b725e`  
		Last Modified: Thu, 11 Jan 2024 00:17:47 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce61e9c932e4906820870265cee7f5495e861ba8b57f0f47650e1280d574335`  
		Last Modified: Thu, 11 Jan 2024 00:17:47 GMT  
		Size: 442.0 KB (441970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71aaa4b94e8a11f899ef7719c77b8cc1fd16aaf98a35a0388f260552823b9b61`  
		Last Modified: Thu, 11 Jan 2024 00:17:47 GMT  
		Size: 5.9 MB (5882159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d700cdc9210b76b84c088cca296a7253e3be2f9de023e8393bf2ddf53c68033c`  
		Last Modified: Thu, 11 Jan 2024 00:17:45 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe5c44c6c8bdb028170831fbc7dc96e8b5da54a016d038951951e86f0974c78`  
		Last Modified: Thu, 11 Jan 2024 00:17:45 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d9fdd76825d609f04ff6dcabad4616eb23804171db87e174dd34118319a979`  
		Last Modified: Thu, 11 Jan 2024 00:17:45 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d85ef6ed16f02b4147c8da0b3813ef70303e9b705c007843e9e1ba5095d91b0`  
		Last Modified: Thu, 11 Jan 2024 00:17:45 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
