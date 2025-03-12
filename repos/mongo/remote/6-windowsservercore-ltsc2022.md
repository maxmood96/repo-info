## `mongo:6-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:fe7c5c3a2294b92f41a99929f01693d025ae6a9e41e13573015d06c31e58876c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `mongo:6-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull mongo@sha256:6f83eb6bb974203b0acec19c0090cb63f508aacad72c0f1440624c902efeb1da
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2796910135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f119d0bb1a23400c638d9e66e14275550ff8ae7acfdf8d741bf6a3e8ab1c825`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 19:04:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Mar 2025 19:04:55 GMT
ENV MONGO_VERSION=6.0.20
# Wed, 12 Mar 2025 19:04:56 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.20-signed.msi
# Wed, 12 Mar 2025 19:04:57 GMT
ENV MONGO_DOWNLOAD_SHA256=518cf974540402bd2992996372d29dd13912e2662d2288649e7984ed091a5e5c
# Wed, 12 Mar 2025 19:05:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 19:05:49 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Mar 2025 19:05:54 GMT
EXPOSE 27017
# Wed, 12 Mar 2025 19:05:58 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0afbc4e1d04e2b02e6e42793ea6cbbade206b3699fe3d2a7ae125324966388`  
		Last Modified: Wed, 12 Mar 2025 19:06:02 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f17034db3e62273fe3e8187afb8f09210ce01692a56edd857dff271a396bb9`  
		Last Modified: Wed, 12 Mar 2025 19:06:02 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670b15f8d99ca9f4c7b527d8a17419a5bc2832f9249e8d3ce0bd153c95456000`  
		Last Modified: Wed, 12 Mar 2025 19:06:02 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eac54680bd572582c9ae1467c48242cbce37606bd91dd511308f74ce052f155`  
		Last Modified: Wed, 12 Mar 2025 19:06:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd96020f9551a42d686557bf4be92c8be3352efc4b2ec675b31ab5442607b452`  
		Last Modified: Wed, 12 Mar 2025 19:06:45 GMT  
		Size: 527.0 MB (526959888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:422bb1b83d7d27308419e429d3cc1bd7fd62766b71698159534b2ad7d1321960`  
		Last Modified: Wed, 12 Mar 2025 19:06:01 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ff1164291a3472fe99cfabe4c9ae2fe79cb5a0fbe9ad3c8c58331e81f35d2e`  
		Last Modified: Wed, 12 Mar 2025 19:06:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99e0f78d6e4115a2150b3b51ed3acedd5b7872075010ef7f9617c6efc37a6c`  
		Last Modified: Wed, 12 Mar 2025 19:06:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
