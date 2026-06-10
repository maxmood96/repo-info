## `mongo:7-windowsservercore`

```console
$ docker pull mongo@sha256:8cf33f7ddb2c61b9fa144e5f90220f3e455ace88dc7bda46deb44c0358d2a1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `mongo:7-windowsservercore` - windows version 10.0.26100.32995; amd64

```console
$ docker pull mongo@sha256:1e3c493876e64731b5d02e7275b65386ecbf5b79b5e06616f8ed9d2e9bff76d5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2902668267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c77245182944fb21a8adac68b72c818f7a8304866f138f6da7facc074232aa9`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Tue, 09 Jun 2026 22:24:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Jun 2026 22:24:30 GMT
ENV MONGO_VERSION=7.0.34
# Tue, 09 Jun 2026 22:24:31 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.34-signed.msi
# Tue, 09 Jun 2026 22:24:32 GMT
ENV MONGO_DOWNLOAD_SHA256=87a344eba774c38d0ee7261b3c0a12fb3bd2e16241ff4026ae7220c789cf06bc
# Tue, 09 Jun 2026 22:26:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:26:12 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 09 Jun 2026 22:26:12 GMT
EXPOSE 27017
# Tue, 09 Jun 2026 22:26:13 GMT
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
	-	`sha256:e621d7b6d909a79e2a132ebdb9714d86bb42c92f6d0a6a1ab17dcd95d1861ab5`  
		Last Modified: Tue, 09 Jun 2026 22:26:26 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449ebe445ccd65c558ae645efcaa4544e4b7efd011e85134f88c50a37b3f95a1`  
		Last Modified: Tue, 09 Jun 2026 22:26:26 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc3e0d0ef8c8b2057cf99db167fe526da14763b615792ac46da9f56fb9e5253`  
		Last Modified: Tue, 09 Jun 2026 22:26:26 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782df7aeccae752b0311f3e39e9dbe58827b345791b7ed54e5674178e4400a50`  
		Last Modified: Tue, 09 Jun 2026 22:26:24 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb5dfbde087b98a32ab0a7535fdf42d35721f5caeb8bdd22018fda8fbd12e60`  
		Last Modified: Tue, 09 Jun 2026 22:27:26 GMT  
		Size: 623.5 MB (623516316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976c0b003fb4838a5a9beaae28efb840ea1d98649fac55fcc7a978aeb98ed161`  
		Last Modified: Tue, 09 Jun 2026 22:26:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2ffacdbbb18128ec62c5dc61987fd31057370aa801cb760fe5a1126e8d64a3`  
		Last Modified: Tue, 09 Jun 2026 22:26:24 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2972e339f85d433d06ae657e39e2edb49acab61d0eaa2313e62d7dc598856bc`  
		Last Modified: Tue, 09 Jun 2026 22:26:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-windowsservercore` - windows version 10.0.20348.5256; amd64

```console
$ docker pull mongo@sha256:5d0d3ae153d0e550c1e3e122e5be2c484808aaa36e7118a32e170b7c89a74122
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2755791892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbba5441d8756d3f1f1da54dcc091ada04b25848a505a924ebb16a29a4d923c8`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:21:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Jun 2026 22:24:20 GMT
ENV MONGO_VERSION=7.0.34
# Tue, 09 Jun 2026 22:24:21 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.34-signed.msi
# Tue, 09 Jun 2026 22:24:22 GMT
ENV MONGO_DOWNLOAD_SHA256=87a344eba774c38d0ee7261b3c0a12fb3bd2e16241ff4026ae7220c789cf06bc
# Tue, 09 Jun 2026 22:27:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:27:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 09 Jun 2026 22:27:25 GMT
EXPOSE 27017
# Tue, 09 Jun 2026 22:27:26 GMT
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
	-	`sha256:a42bd05c6eace9b3d2b7a54918556307d072055152009d32427e3187ac0f09af`  
		Last Modified: Tue, 09 Jun 2026 22:24:03 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000926e3ebde9855c9a2f9d36ebd91b039f7272e8d284068af15d11a706b8dd0`  
		Last Modified: Tue, 09 Jun 2026 22:27:42 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6b81a3c2f1507bbe2eb0b79ddbe08710e763ed0a9a59816ebd63e5f22bb476`  
		Last Modified: Tue, 09 Jun 2026 22:27:41 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd56347fb19584d22431fc65426af1d163f032b1a42e1035484ea79731216c6`  
		Last Modified: Tue, 09 Jun 2026 22:27:40 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c6e38f0879d3d12e20ff3163252db8029bdebf4f7bca57d3539899ce1f4cce`  
		Last Modified: Tue, 09 Jun 2026 22:28:38 GMT  
		Size: 623.7 MB (623657269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad305332cd57b13e374bbabade17cf78b6116d6105fc8b82d8fd24427d70d6d8`  
		Last Modified: Tue, 09 Jun 2026 22:27:40 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66a54078386a31a13f444e1401f1d48910bfa866ceca3702254b6184260252e`  
		Last Modified: Tue, 09 Jun 2026 22:27:40 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734d5b45c86c7b487d50edcd38969549a1cf3c257040f9032918e5a6be3719e7`  
		Last Modified: Tue, 09 Jun 2026 22:27:40 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
