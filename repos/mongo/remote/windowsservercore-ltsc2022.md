## `mongo:windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:81112fb94d1d68513d3d521bfccc7d90b4b4e683512257f2677566516e99f615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `mongo:windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull mongo@sha256:bab61028b9138688ab10f60d7a97f7ae593f1166afbf61f1757877681173111d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3055530116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c27b5b99ec10cdc6698615cf7adc2af4479896dab9fe214e404d0dbc2e53bf2`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Tue, 10 Jun 2025 21:26:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Jun 2025 21:26:03 GMT
ENV MONGO_VERSION=8.0.10
# Tue, 10 Jun 2025 21:26:04 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.10-signed.msi
# Tue, 10 Jun 2025 21:26:05 GMT
ENV MONGO_DOWNLOAD_SHA256=ae5f02f81ba456ee9fcf819c362255ccae9a961f039435a09b6887f46732c940
# Tue, 10 Jun 2025 21:27:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 10 Jun 2025 21:27:35 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 10 Jun 2025 21:27:36 GMT
EXPOSE 27017
# Tue, 10 Jun 2025 21:27:37 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee01c7b0c4b12e40af7644c0d32373eaa10e5087c02545fa5c8924aef6fdffb4`  
		Last Modified: Tue, 10 Jun 2025 22:09:22 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b941dd59fcd8e5673d42319466f804c80352a10811aee45d2b553cfb98e2e95f`  
		Last Modified: Tue, 10 Jun 2025 22:09:22 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5f2d737890d7350b5979699f3ca034c7d5b722855dbe0e4813eae9f6a0c46a`  
		Last Modified: Tue, 10 Jun 2025 22:09:23 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e36338bb739ffdf93168946db99399e81b31a18cfe600913613972c07461368`  
		Last Modified: Tue, 10 Jun 2025 22:09:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff5ebae3500cf0fd4cbac4354b72b4b351ef7dff6064a57f828696b28e76093`  
		Last Modified: Tue, 10 Jun 2025 22:09:34 GMT  
		Size: 775.3 MB (775269555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a21dde5bd2a2a73cd15d2a8178bb5ed5bed199cfaeb6469bbb68837d313c4ff`  
		Last Modified: Tue, 10 Jun 2025 22:09:23 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93cfafacf15055c801cb1ff470b4e46d919b5a8f2a2cf61691239db14d8cb31`  
		Last Modified: Tue, 10 Jun 2025 22:09:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f8d25940f7a8c8f2ea73286342cd9656a407e4e1f05a08f71417dab1a1596c`  
		Last Modified: Tue, 10 Jun 2025 22:09:25 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
