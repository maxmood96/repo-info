## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:98e84eb74fa514a7316b810f56ea92a933ca29a6fdebe7df9a575ac6e8b629e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `mongo:windowsservercore` - windows version 10.0.26100.32995; amd64

```console
$ docker pull mongo@sha256:faab9c4d30f9de2aa782484b081fbaa5fd55322eb7801498cb2021ad69bf0261
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3096999304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58edcb477813a39ebcdfc30d1aa7ed732d90191a5385ba7e518a2f01e348331c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Fri, 12 Jun 2026 19:14:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 12 Jun 2026 19:14:33 GMT
ENV MONGO_VERSION=8.2.11
# Fri, 12 Jun 2026 19:14:35 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.11-signed.msi
# Fri, 12 Jun 2026 19:14:35 GMT
ENV MONGO_DOWNLOAD_SHA256=564477a3abee2720e78714dd6d2d9757a2d8e5cf24ecd6665cb788be95626c36
# Fri, 12 Jun 2026 19:17:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 12 Jun 2026 19:17:19 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 12 Jun 2026 19:17:20 GMT
EXPOSE 27017
# Fri, 12 Jun 2026 19:17:21 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef6d3ff2a6a5e2c23962ee1997ba7615305410626743a9be3a64d6d4bd7e583`  
		Last Modified: Fri, 12 Jun 2026 19:17:36 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f7b0b755f344ddc57d9c86cad732456f3ee5269172e76066e5fe7dd48d1bca`  
		Last Modified: Fri, 12 Jun 2026 19:17:36 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab6dcc46ea2eb51fd00d6faf99d2bb3eac1f745f4c9969b3bc5609202e95fcc`  
		Last Modified: Fri, 12 Jun 2026 19:17:36 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d606088cc892b0d406c069dca5df0e87a11f9dce86db0fe500956874fb937675`  
		Last Modified: Fri, 12 Jun 2026 19:17:34 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78154ae0752e563c836607c3ca6b441050065819d3762bcaea3537157c7fd42f`  
		Last Modified: Fri, 12 Jun 2026 19:18:39 GMT  
		Size: 817.8 MB (817847381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8676624d09f3cb8e0bb315e0df9ad371ba1c07a1a8d55f22aa9787cb72e23060`  
		Last Modified: Fri, 12 Jun 2026 19:17:34 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a063c95eb27ec4d3f11e1276d1f49d67826cb25c6762b737fd03157b044a0ecb`  
		Last Modified: Fri, 12 Jun 2026 19:17:34 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba295ddcc9e5cdd9725853215bdbbd6503b9471e7d9d2da73ad3474701f696c`  
		Last Modified: Fri, 12 Jun 2026 19:17:34 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:windowsservercore` - windows version 10.0.20348.5256; amd64

```console
$ docker pull mongo@sha256:a2aba6cdaf6f88889ffc2401cbbb9ecc93b01f3d074b7c054986856114c5903b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2950137122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a009c8862931a2607536940d46a59fe97f49693f6d5b12b0211c85b05a852f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Fri, 12 Jun 2026 19:14:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 12 Jun 2026 19:14:59 GMT
ENV MONGO_VERSION=8.2.11
# Fri, 12 Jun 2026 19:15:00 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.11-signed.msi
# Fri, 12 Jun 2026 19:15:01 GMT
ENV MONGO_DOWNLOAD_SHA256=564477a3abee2720e78714dd6d2d9757a2d8e5cf24ecd6665cb788be95626c36
# Fri, 12 Jun 2026 19:17:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 12 Jun 2026 19:17:56 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 12 Jun 2026 19:17:56 GMT
EXPOSE 27017
# Fri, 12 Jun 2026 19:17:56 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fec8226f0d1c7493bba44ba0fee194ad800249d4d4f21d0e26ac06fef2fcc7`  
		Last Modified: Fri, 12 Jun 2026 19:18:03 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44343a0283267e872253da58810b724a8458284c7901b76ed0665788f392e49a`  
		Last Modified: Fri, 12 Jun 2026 19:18:03 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd066a69638c5e1eaf5c252c6334bca6ce42e1d94fd09307482a89f232e36cf`  
		Last Modified: Fri, 12 Jun 2026 19:18:03 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738dfc2bc709d2346a04baf7da918ab82135f14c926d69deb76b472692fd4e56`  
		Last Modified: Fri, 12 Jun 2026 19:18:01 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17eb2eb8806f34be1943286035595996748767d2a6892c1e3599505db1f88b7`  
		Last Modified: Fri, 12 Jun 2026 19:19:18 GMT  
		Size: 818.0 MB (818002369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00608cdafe6f4565621dda9f4f4c07aa5243b8ee846d6e20e1976a3348465ea7`  
		Last Modified: Fri, 12 Jun 2026 19:18:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eea30a18b0bf54040ad2da6711acaa2076ad29bf91d4d92d2131d0c6a10fd1c`  
		Last Modified: Fri, 12 Jun 2026 19:18:01 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cb2e8198a0034686ed25dd2774137e7a6295f2953b475519604d787ff59585`  
		Last Modified: Fri, 12 Jun 2026 19:18:01 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
