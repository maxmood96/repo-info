## `mongo:7-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:7fd11e825357f16edb317c1bd0cef002e5bba4917d5fc5a624f0cff311309211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `mongo:7-windowsservercore-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull mongo@sha256:3772820480569a0262a8a9b9dd6082996220478f5c4f355191ef78dc6940290a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2883520013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b701b1fe18fb6f2606d25ec4387b351f0d2b7a0bfcd40b7620baeb25551a872a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Wed, 09 Apr 2025 00:54:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Apr 2025 00:54:26 GMT
ENV MONGO_VERSION=7.0.18
# Wed, 09 Apr 2025 00:54:27 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.18-signed.msi
# Wed, 09 Apr 2025 00:54:28 GMT
ENV MONGO_DOWNLOAD_SHA256=ab23d0e0488dd0b9ab07bae73e481271c7574e212b4bb61b1331400a3cffb02b
# Wed, 09 Apr 2025 00:55:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:55:24 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Apr 2025 00:55:26 GMT
EXPOSE 27017
# Wed, 09 Apr 2025 00:55:28 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ba84c62c8a2f5796c0bd11a358e3d08f16e5501c7b92cd7e1963203f19361d`  
		Last Modified: Wed, 09 Apr 2025 00:55:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62443d65c328c415dffbcc6556a049e485af3b54641800ad9536d734e50563a8`  
		Last Modified: Wed, 09 Apr 2025 00:55:35 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25a77d365c9ef02ad5c20115b5d3fac183b4c77d7e0ec07c1e7c9103c349efc`  
		Last Modified: Wed, 09 Apr 2025 00:55:35 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983ae19fbc49d9786bd06802c5524fde750d466541bce15417cf3ba9261504ec`  
		Last Modified: Wed, 09 Apr 2025 00:55:33 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bcbd6ac2faf4c7b39b8f4213a31a99bf54bc58fff77c12712e30f46ba93c842`  
		Last Modified: Wed, 09 Apr 2025 00:56:24 GMT  
		Size: 612.5 MB (612515359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340b28441176f30f16b08022098e1cfcba382a44ffb4d5c8e122e3590b1db792`  
		Last Modified: Wed, 09 Apr 2025 00:55:33 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7610b817ef782934709b818d5ec544b25ca5dda60381ba42776c32e188237c39`  
		Last Modified: Wed, 09 Apr 2025 00:55:33 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c97b0fa6128f1c88ddc60705c6e067aaf5d1fcc38034d1be40dcdd8eeea621`  
		Last Modified: Wed, 09 Apr 2025 00:55:33 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
