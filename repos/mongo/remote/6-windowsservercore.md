## `mongo:6-windowsservercore`

```console
$ docker pull mongo@sha256:d744fbd2352a07d640c97157ed66693432f99aa46c6d19c7df54cc0adddd9baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `mongo:6-windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull mongo@sha256:97847a1ca19be0f0c4a4c8499c14151747c21db6332f85cfe8e6fc16087fdfb4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1986955818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a448133d74607114bd51cf51a7d7afa745024f92e160f6eba52eb97ac8fffbfc`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 00:01:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Sep 2024 00:01:40 GMT
ENV MONGO_VERSION=6.0.17
# Wed, 11 Sep 2024 00:01:40 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.17-signed.msi
# Wed, 11 Sep 2024 00:01:41 GMT
ENV MONGO_DOWNLOAD_SHA256=90c6014610d9351763c59985460c915bb87227ecea619cb2d93e962787b87cc1
# Wed, 11 Sep 2024 00:02:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 00:02:42 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Sep 2024 00:02:43 GMT
EXPOSE 27017
# Wed, 11 Sep 2024 00:02:43 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3284b0821fbd1944a34b4a72a3b0fe634b0f48f3b90730898dbdecd7076bb4`  
		Last Modified: Wed, 11 Sep 2024 00:02:47 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96adbe0bf947d4006652f432ef051e8e5e2fb0078b77fa16c949ef9a0db7a4e7`  
		Last Modified: Wed, 11 Sep 2024 00:02:47 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1af5e6c4c5317a253c2014ff65cf051a236395f4b6074b44ce63072998e80f`  
		Last Modified: Wed, 11 Sep 2024 00:02:47 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7588d08872a0aaaca3053bce9a53cac27788891483c283194e062da17148db25`  
		Last Modified: Wed, 11 Sep 2024 00:02:46 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e32f8901f06fada4eacd93d797f3eafc4aea48fb91b81918da54626ccd3294`  
		Last Modified: Wed, 11 Sep 2024 00:03:30 GMT  
		Size: 524.8 MB (524754109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66773cf70419a80e74ce32d857f4b045bb4bd9301b2dd3fc29930d8379e7a6fe`  
		Last Modified: Wed, 11 Sep 2024 00:02:46 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5785c43caa11c70fa77fed6285d082f307887d2fdeea36b38f6f737517845b7f`  
		Last Modified: Wed, 11 Sep 2024 00:02:46 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f88c1ad68bb8d3e04aa49a25f639f354778dcc814649ffaec9d282fab5c4562`  
		Last Modified: Wed, 11 Sep 2024 00:02:46 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull mongo@sha256:177b43c2a185ceeac80baa0b825ff2b64c4eb262fdea7ad84be01cf7fee799a7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2245022323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2042b5afac1dc2f81331cea792fcee252c50a9803c571aa5f03f73d04d355e51`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:04:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Sep 2024 00:04:29 GMT
ENV MONGO_VERSION=6.0.17
# Wed, 11 Sep 2024 00:04:30 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.17-signed.msi
# Wed, 11 Sep 2024 00:04:30 GMT
ENV MONGO_DOWNLOAD_SHA256=90c6014610d9351763c59985460c915bb87227ecea619cb2d93e962787b87cc1
# Wed, 11 Sep 2024 00:05:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 00:05:48 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Sep 2024 00:05:48 GMT
EXPOSE 27017
# Wed, 11 Sep 2024 00:05:49 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfcf6db89e54ae948e29717a7b939e6f6813574fc548d8854c47794f0b34355`  
		Last Modified: Wed, 11 Sep 2024 00:05:53 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c4e775240ca57c111c2c34ef26c3958b9091f3b864d9c0523809dc955282ee`  
		Last Modified: Wed, 11 Sep 2024 00:05:53 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3600d9b2bf8891d095e60a5a1151e48517a691e65bbfbfd077f628682c73b1ab`  
		Last Modified: Wed, 11 Sep 2024 00:05:53 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2406d73c78b4356cd24bbebc4488ff9afb476a8b959942d3b9a519b29fc0f0c`  
		Last Modified: Wed, 11 Sep 2024 00:05:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac001986e738f1386fb6d2e22d730ab5995d8a3df326e8a0e2ffb47547348de7`  
		Last Modified: Wed, 11 Sep 2024 00:06:35 GMT  
		Size: 524.7 MB (524744880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64d4c02c3d6888f0630f8dbb86a06edc2affecc45c2d4e916a10001929a7eb8`  
		Last Modified: Wed, 11 Sep 2024 00:05:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da0ae244a5a0674aad1649e38b5dd04d0f9fc422d869eb778c4c05fdeef20097`  
		Last Modified: Wed, 11 Sep 2024 00:05:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc15ce74f15a681505e660aa2b8af8289c6b8fd109add708c14c57a61c8f6650`  
		Last Modified: Wed, 11 Sep 2024 00:05:52 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
