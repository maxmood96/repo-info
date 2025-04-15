## `mongo:6-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:632b5cc5fc723dde9770c46c633db3164cc0f34fcfbea6459cb6419ae645066a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `mongo:6-windowsservercore-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull mongo@sha256:dafbb8462ce44e6e134bdffe2c9822a23a3c5cbe26afb5e5493d9f94becea925
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2797955597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f09d5b438899609aeb011c93702ac29a5098a4a8a686b02e8c9038ad1f9c2af`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Mon, 14 Apr 2025 23:10:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 14 Apr 2025 23:10:40 GMT
ENV MONGO_VERSION=6.0.22
# Mon, 14 Apr 2025 23:10:41 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.22-signed.msi
# Mon, 14 Apr 2025 23:10:42 GMT
ENV MONGO_DOWNLOAD_SHA256=8d15563eae81fe7ec7530ab84cb04a9f7af16391dffbaa27d02ae9937b7e9c3c
# Mon, 14 Apr 2025 23:11:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 14 Apr 2025 23:11:42 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 14 Apr 2025 23:11:43 GMT
EXPOSE 27017
# Mon, 14 Apr 2025 23:11:44 GMT
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
	-	`sha256:f702fc94dc524ce8daf5f1bd3d3c718f9ef2196e155d111c8d515aeb5863120b`  
		Last Modified: Mon, 14 Apr 2025 23:11:47 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85c2b1634ebc569be146d9d0b54c43e902f5b1a9ae6ea3f5d88b9956ae91c80`  
		Last Modified: Mon, 14 Apr 2025 23:11:47 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d9e37c94646e2347efefb1460e4db716c346521f5799b0ef0d894b140047a0`  
		Last Modified: Mon, 14 Apr 2025 23:11:47 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781d439ae5ac7369da2dffd785e40fac2c0122bd4d812695dac43565ce3ff4f5`  
		Last Modified: Mon, 14 Apr 2025 23:11:46 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5f9b3abb5d7478407beb7956cba27263d8aee5c5758d5796878c90f538542d`  
		Last Modified: Mon, 14 Apr 2025 23:12:32 GMT  
		Size: 527.0 MB (526950961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8946c87fdcae33a21864535dbf4f7d8af599023727e495862784e7908b5270c5`  
		Last Modified: Mon, 14 Apr 2025 23:11:46 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c97b443d3f44ce66012a9d4f53b26014c4d6975982595a248409ea469b9702`  
		Last Modified: Mon, 14 Apr 2025 23:11:46 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91f99ec53560cf1377c811799e6dba5360519e9734b185a96a1b74af9b09805`  
		Last Modified: Mon, 14 Apr 2025 23:11:46 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
