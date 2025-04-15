## `mongo:8-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:8777f4b3a405d591716c38f79024848793a142ac38a1b18f5d9ca9cea53ba765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `mongo:8-windowsservercore-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull mongo@sha256:e8bcf0d8c7475ff19ded55abb42cbb18d95fe158faacde3120ba9ad00bc1e8f8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3041275098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e064556c5e900230e011e620084e501443e5855d1f2ccc7bf7daff5704fcb7b7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Mon, 14 Apr 2025 23:03:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 14 Apr 2025 23:03:41 GMT
ENV MONGO_VERSION=8.0.8
# Mon, 14 Apr 2025 23:03:42 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.8-signed.msi
# Mon, 14 Apr 2025 23:03:43 GMT
ENV MONGO_DOWNLOAD_SHA256=4bf700912876c337697fa02bf4c38db0baed89604033b138e5e27d4e3eb743ee
# Mon, 14 Apr 2025 23:05:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 14 Apr 2025 23:05:03 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 14 Apr 2025 23:05:04 GMT
EXPOSE 27017
# Mon, 14 Apr 2025 23:05:05 GMT
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
	-	`sha256:ad1fd0946bff7769e52756ac4fb71b013def6d583cb8b8d181b379924abdcc8b`  
		Last Modified: Mon, 14 Apr 2025 23:05:11 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a974129f19e62e6ccecf5154fafe3de2f8b21a000c753320cdeddc2db37acf`  
		Last Modified: Mon, 14 Apr 2025 23:05:11 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea6431b46122a9dcefbafd16c3289aa49cef946e64ad6646a7400f106bce83a`  
		Last Modified: Mon, 14 Apr 2025 23:05:11 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1e988b68efbdb256d633d53c20bee421e845ee887994b984e63e8c9b3a5866`  
		Last Modified: Mon, 14 Apr 2025 23:05:09 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a413782c10c8fc752d4f3328181b3c6e39f42dab887574674414df26208cb2f4`  
		Last Modified: Mon, 14 Apr 2025 23:06:11 GMT  
		Size: 770.3 MB (770270486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9021cd22df773d5591333e7e76eda695893c1d82cb4f6d1cfbc16aea188c49d1`  
		Last Modified: Mon, 14 Apr 2025 23:05:09 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a0b5e0a5b00294d15b1fbb9f82c4498846c302e5672ffe73eefeef2dfdcaf0`  
		Last Modified: Mon, 14 Apr 2025 23:05:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c016cb5d8f2a9ee35868171a912da2cf3fdeb6a329078dd94a22154de3388a17`  
		Last Modified: Mon, 14 Apr 2025 23:05:09 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
