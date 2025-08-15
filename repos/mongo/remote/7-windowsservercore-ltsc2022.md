## `mongo:7-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:65056c163ea7c2802a48e8a2987767e7530ec7fb8c15d056601bcff2c745508b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `mongo:7-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull mongo@sha256:4f186e6fb1d24dd59e69ff03d796a1028be9c342c588cc4c0ca2d1b6fa98896c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2899528179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d06893e3ab96e84e8d584f0cf079c4f2cd5e41df1c1d9fb5065faa4aafc941c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Thu, 14 Aug 2025 22:51:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 14 Aug 2025 22:51:57 GMT
ENV MONGO_VERSION=7.0.23
# Thu, 14 Aug 2025 22:51:58 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.23-signed.msi
# Thu, 14 Aug 2025 22:52:00 GMT
ENV MONGO_DOWNLOAD_SHA256=930756f059e218a427192156655066a1c900b9493d7c107077ed89aca6fc950a
# Thu, 14 Aug 2025 22:52:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 14 Aug 2025 22:52:58 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 14 Aug 2025 22:52:59 GMT
EXPOSE 27017
# Thu, 14 Aug 2025 22:53:00 GMT
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
	-	`sha256:9eaf540acad7884bab042411faaf42af3baf649d0c21b0b6846479a0003e59bb`  
		Last Modified: Thu, 14 Aug 2025 22:54:29 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4c156e840a0ef404a3297b854968d81c96ac185d1957bc17c794917565296f`  
		Last Modified: Thu, 14 Aug 2025 22:54:28 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75abb23230cc9b05041014a793b7a87a67936b5da212f4c902b296a38123ed5b`  
		Last Modified: Thu, 14 Aug 2025 22:54:28 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf613535492993c025582d676a24906d8f5f724c0d9995deb256542d5abdae0`  
		Last Modified: Thu, 14 Aug 2025 22:54:29 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70f2c9343bd0c7d49f400d53c847ba41c8211656f30a100916699e5b7b25059`  
		Last Modified: Thu, 14 Aug 2025 23:09:14 GMT  
		Size: 617.8 MB (617827180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ed5de8e48ffecaf2652feef58afb90dbb18a7232dbb65d34ea00c7aa870254`  
		Last Modified: Thu, 14 Aug 2025 22:54:29 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5116eb1767c4fe64231d2add030ffe3ca5a2c7a7a223f7cbec94c694626fbf`  
		Last Modified: Thu, 14 Aug 2025 22:54:29 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b61553df5a379d80dc33b01974544ed65a4a858b7190df65bd0f24cd1e63d14`  
		Last Modified: Thu, 14 Aug 2025 22:54:29 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
