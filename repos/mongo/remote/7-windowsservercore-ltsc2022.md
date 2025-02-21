## `mongo:7-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:c0f3712318f61e5788df67b869ac12afb0093b918ba16876d1586dd29c041307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `mongo:7-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull mongo@sha256:1b4ba29a3d36cd6187431b6c54dcae4088bddb68251224334dd7ff41f2245f23
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2875647252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d83a72c8adc356fdbeb8338010b22dc1ab98ec5f76cf765a4d8ae171ecea6b0`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:36:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 13 Feb 2025 00:36:13 GMT
ENV MONGO_VERSION=7.0.16
# Thu, 13 Feb 2025 00:36:14 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.16-signed.msi
# Thu, 13 Feb 2025 00:36:15 GMT
ENV MONGO_DOWNLOAD_SHA256=88fe05d7f324e72b9d17cbfe9bde652053c398efc7cffc0249c944faf4f32b34
# Thu, 13 Feb 2025 00:37:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 13 Feb 2025 00:37:26 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 13 Feb 2025 00:37:27 GMT
EXPOSE 27017
# Thu, 13 Feb 2025 00:37:29 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85c1d0b043025e5ff4eb2b1b2fc08dc2131faf1800454c83f3374771ef50c1a`  
		Last Modified: Thu, 13 Feb 2025 00:37:36 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d140fe7b7b8516ff1f344389d25d042baffa78c00d8a468ec01f47b08fdd077`  
		Last Modified: Thu, 13 Feb 2025 00:37:36 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97bf68423e172f496307a58e517ed024f1fc1ea67b4b9dc4121b278b1960bd5f`  
		Last Modified: Thu, 13 Feb 2025 00:37:36 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c966ea38dd5ada59ae08ba37ec0daa6165605d996eb58ed5724fbd18a941a5`  
		Last Modified: Thu, 13 Feb 2025 00:37:34 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4a29cc29a0f98cab25a683ad2e317be24e8114e1d215979ca1af9b408b4bd3`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 611.8 MB (611780174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c7d9f54532c00d4300bac9364cd3d52d26a3926d954dd8fae94b737319e602`  
		Last Modified: Thu, 13 Feb 2025 00:37:34 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ecd60024325747224f132d00e5b0581d866bfd006a6ecbee7bc0e676e033dbd`  
		Last Modified: Thu, 13 Feb 2025 00:37:34 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f98c9c8c3793cd6869ac3c7befbf3a9415a4b8be5887b7e066478a415e4071`  
		Last Modified: Thu, 13 Feb 2025 00:37:34 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
