## `mongo:6-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:d9d7a9facd1eadeca1400ac14176c1de49c9ef441e5c71cc9c8a6814a03d2160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `mongo:6-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull mongo@sha256:8b58ed845abd4881f48fcda85d6106cc6358a6f6879f57ac62ffd64745f58f9d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2808734068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b62712364934bc777b9deec5d1f7410e06179c31b01a765a5ba95a2a4d0b0fd`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Wed, 27 Aug 2025 16:57:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 27 Aug 2025 16:57:21 GMT
ENV MONGO_VERSION=6.0.26
# Wed, 27 Aug 2025 16:57:22 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.26-signed.msi
# Wed, 27 Aug 2025 16:57:23 GMT
ENV MONGO_DOWNLOAD_SHA256=b32578a8d982810c6a9a0b2f962bd45053701d97415f901030b796ec93dea75a
# Wed, 27 Aug 2025 16:58:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 27 Aug 2025 16:58:45 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 27 Aug 2025 16:58:46 GMT
EXPOSE 27017
# Wed, 27 Aug 2025 16:58:47 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5210f22f651917d5f30b881601183c7f02abfe8bec67864725d1fb117d522758`  
		Last Modified: Wed, 27 Aug 2025 17:00:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92bf2e59143f446ade8927ccad98985b236847ce5be956fc9fa689a65f4cf095`  
		Last Modified: Wed, 27 Aug 2025 17:00:29 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe2bf2650e8edcb25861363a08fb39b3aa37734389827c98ee63798ccf10cdc`  
		Last Modified: Wed, 27 Aug 2025 17:00:30 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4af7475aef95587bf35f2e4fbfd8e034d6b2e9d6140457547dc09d3858b1353`  
		Last Modified: Wed, 27 Aug 2025 17:00:30 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd6c8708b7498e7e3d1b8a413897e67d0ed73732449c604a588cf1214fb5472`  
		Last Modified: Wed, 27 Aug 2025 17:12:16 GMT  
		Size: 527.0 MB (527033131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4ee2c03ea8852601adfa777ea283396a4d080f32b3737b0ae396afe91f50e`  
		Last Modified: Wed, 27 Aug 2025 17:00:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6c62f1cd25f97be0758e68f51e9b0507d6ab9cb4223860d269c3b34b7f1a3a`  
		Last Modified: Wed, 27 Aug 2025 17:00:30 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0376b1068728e1f0ed734cf1d87bf4aebb5cbd72df9c1af777a97da0cdc10f92`  
		Last Modified: Wed, 27 Aug 2025 17:00:30 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
