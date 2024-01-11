## `mongo:6-windowsservercore-1809`

```console
$ docker pull mongo@sha256:651550a5fc9a0d5cc8e0fa1ee08057dace94ff3659ef9a381b945ef777d5d993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `mongo:6-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull mongo@sha256:bb5b2c12422751932441531928dc74ac897cb4739eb5de6273db824bbdfe29bc
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2588346315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce2c46864f9a078a6a18879f857c860af0a3a9b482032919ccf119afda3b533`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:07:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:07:38 GMT
ENV MONGO_VERSION=6.0.12
# Thu, 11 Jan 2024 00:07:39 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.12-signed.msi
# Thu, 11 Jan 2024 00:07:39 GMT
ENV MONGO_DOWNLOAD_SHA256=126024e5292da3470eb119d798d11862ce1f0472836bce7d3210dcb522b80aa3
# Thu, 11 Jan 2024 00:09:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 11 Jan 2024 00:09:44 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 11 Jan 2024 00:09:45 GMT
EXPOSE 27017
# Thu, 11 Jan 2024 00:09:45 GMT
CMD ["mongod" "--bind_ip_all"]
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
	-	`sha256:b789a9aac1d8b2ec4d759df7c09e5c0a2495ebfcdcf72b85d5ea56b020639d35`  
		Last Modified: Thu, 11 Jan 2024 00:09:49 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8cde4e17cb781b45652d6079d4bc63a30313ee83baf60dfa887dba63ef7125`  
		Last Modified: Thu, 11 Jan 2024 00:09:49 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8459cd2004f6521a829a870469291271095f5484deca5159b7db1005298a4595`  
		Last Modified: Thu, 11 Jan 2024 00:09:49 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1937ab9df095127b757511239b8ec925f66eb099a2de2ac64f92324dd116fede`  
		Last Modified: Thu, 11 Jan 2024 00:09:48 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1965060d4b247288d1c6453f81915608c963503a89a5f0e0f7040dfeeb5aa335`  
		Last Modified: Thu, 11 Jan 2024 00:10:33 GMT  
		Size: 518.6 MB (518614710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8e8096cf270f2f1eb4a46e0490ffcac22f8791c249aa5ec746745afd3d7d96`  
		Last Modified: Thu, 11 Jan 2024 00:09:48 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbe31b49f859b45d444b6912cbb40c8d976840d7ae4aec12c6b62a1e5c75a61`  
		Last Modified: Thu, 11 Jan 2024 00:09:48 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05918e0592943d2536b3d15b4e3f373a9d2ff107a9c2dd831d57592bff645d33`  
		Last Modified: Thu, 11 Jan 2024 00:09:48 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
