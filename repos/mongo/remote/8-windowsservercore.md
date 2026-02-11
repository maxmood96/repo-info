## `mongo:8-windowsservercore`

```console
$ docker pull mongo@sha256:c042c93a1a1d590e55602f09c4adb1c873a42ad130b6261de3d2a864ba323f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `mongo:8-windowsservercore` - windows version 10.0.26100.32370; amd64

```console
$ docker pull mongo@sha256:3996669790c1847bbbdfcf636a24a6dccc5da6ac8dba75eab4c9746ac6ce3c81
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2780408960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ddc79181f4ac354719d422e7f048b6930a4bad0d133b11f309f3753e952a9d8`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Tue, 10 Feb 2026 22:58:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Feb 2026 22:58:18 GMT
ENV MONGO_VERSION=8.2.5
# Tue, 10 Feb 2026 22:58:19 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.5-signed.msi
# Tue, 10 Feb 2026 22:58:19 GMT
ENV MONGO_DOWNLOAD_SHA256=02d42062a64b88b68b385dbd723fc2110ef2d43a83642324d94f2f2a6268befb
# Tue, 10 Feb 2026 23:00:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 10 Feb 2026 23:00:11 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 10 Feb 2026 23:00:11 GMT
EXPOSE 27017
# Tue, 10 Feb 2026 23:00:12 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a34ca08cf4aba145005c8c79ba38ccd008fc1424e50063c0de853b0dbf7a2a7`  
		Last Modified: Tue, 10 Feb 2026 23:00:19 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bae381db804c298e3d75193342e61c35c5d56cbc8f2796d4c63df00fff1970d`  
		Last Modified: Tue, 10 Feb 2026 23:00:18 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665308e4f8dc2612c4d59b4f775cc4630be5040610bb17a70a2e6e2dd682e0b3`  
		Last Modified: Tue, 10 Feb 2026 23:00:18 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e159c4826cd06e2bce1648c6dc57bfc8ccc9726e3eb3d4a485af6c91d4c58a5`  
		Last Modified: Tue, 10 Feb 2026 23:00:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58eb441c92b2889a2363e5bf3476a3756cb922542668fbbd4d0be6d4d3a196f`  
		Last Modified: Tue, 10 Feb 2026 23:01:31 GMT  
		Size: 815.6 MB (815639857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e994b54fa6a439cd8ea3386d09d5457187005af669142938669f0374c17ac8a`  
		Last Modified: Tue, 10 Feb 2026 23:00:18 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f50c4703f341ea70eb818ee86b051fe6e560e90618e797614981cb72673f59`  
		Last Modified: Tue, 10 Feb 2026 23:00:16 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9cdc6fcb58650d9d2a40ed6c2e1f7d9312b9e6ad3f6bc87b7a95d78c5fecf1`  
		Last Modified: Tue, 10 Feb 2026 23:00:17 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:8-windowsservercore` - windows version 10.0.20348.4773; amd64

```console
$ docker pull mongo@sha256:59a5d1c65a6f2564cdc9ff9a34cf01a2aa55deeee8e0254564d3c105b55b689b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2678305709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d13c4504a0cd5f83fdba4b9e07a6d44befdc196e93fd501ec7d482511cf51a6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Tue, 10 Feb 2026 23:03:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Feb 2026 23:06:23 GMT
ENV MONGO_VERSION=8.2.5
# Tue, 10 Feb 2026 23:06:23 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.5-signed.msi
# Tue, 10 Feb 2026 23:06:25 GMT
ENV MONGO_DOWNLOAD_SHA256=02d42062a64b88b68b385dbd723fc2110ef2d43a83642324d94f2f2a6268befb
# Tue, 10 Feb 2026 23:08:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 10 Feb 2026 23:08:03 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 10 Feb 2026 23:08:04 GMT
EXPOSE 27017
# Tue, 10 Feb 2026 23:08:04 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a9fd4b568d862245d76458065007c3dc78714ecd05e3b55812aa67f53958c6`  
		Last Modified: Tue, 10 Feb 2026 23:06:08 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8d8780e082cb147d57a8572b30936a4bbf2bab316ff68242bb1a67e917647d`  
		Last Modified: Tue, 10 Feb 2026 23:08:17 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e253cd6218c68c25cb58dc412bacd4a430646baceee15837e11ae37a37bffe92`  
		Last Modified: Tue, 10 Feb 2026 23:08:17 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f6df2e24a9d52d00afa6ac5a58b121e11361dbbe8640646d3f16d2082061f6`  
		Last Modified: Tue, 10 Feb 2026 23:08:15 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb8171f0ec86a0073fac030c3cb1ea87a9477fdb93a6ff4034ae4445ac94dda`  
		Last Modified: Tue, 10 Feb 2026 23:09:27 GMT  
		Size: 815.6 MB (815639387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f2b50415a3a09980803374be2d489ee239676006b3be98c5cb2c90c8918189`  
		Last Modified: Tue, 10 Feb 2026 23:08:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517a7ea87f02095a60cce615c3f9012673565f27f5863001ad8217bd746644c4`  
		Last Modified: Tue, 10 Feb 2026 23:08:15 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0a9bd398ba9ccbbd7613aceae8a3e957de54318158fae73470de2dde92fd2e`  
		Last Modified: Tue, 10 Feb 2026 23:08:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
