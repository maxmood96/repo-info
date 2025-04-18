## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:0872d7ff7f55bd18f2e00854a7932546bfeeb0401928ab7e9206b5d3d3061c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `mongo:windowsservercore` - windows version 10.0.26100.3781; amd64

```console
$ docker pull mongo@sha256:ff06eb44cf6a11f6a5e6f5add2283480aa9e6d0274d4f4167a5caf8a63765dd9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 GB (4165469554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b03eb4a4de5001e6e4a956170cb68b7638a513357e6abc05d56c3c8777ba1e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Fri, 18 Apr 2025 03:15:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 18 Apr 2025 03:15:40 GMT
ENV MONGO_VERSION=8.0.8
# Fri, 18 Apr 2025 03:15:41 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.8-signed.msi
# Fri, 18 Apr 2025 03:15:42 GMT
ENV MONGO_DOWNLOAD_SHA256=4bf700912876c337697fa02bf4c38db0baed89604033b138e5e27d4e3eb743ee
# Fri, 18 Apr 2025 03:17:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:17:19 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 18 Apr 2025 03:17:19 GMT
EXPOSE 27017
# Fri, 18 Apr 2025 03:17:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ba2336fb9edc233889dd58d0a99ab12f5b5acf04de49d7ee3aa450cd7e8cec`  
		Last Modified: Fri, 18 Apr 2025 03:17:24 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553011d5ffaa7f6953c13c78daad8464ae82332eb12dbb6b9bce5056eecaa344`  
		Last Modified: Fri, 18 Apr 2025 03:17:24 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2791125331c75ddd43318abfeda2e1792876441b4620a1e72da55488046eb47c`  
		Last Modified: Fri, 18 Apr 2025 03:17:24 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d846f19fea476a630d970cf569774e963b960da6688019fc9dcda8d8e855db7`  
		Last Modified: Fri, 18 Apr 2025 03:17:23 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16dfbf7e9002fe593df2c6e3aa07cca48072d6148c871610746cd4646a6435a5`  
		Last Modified: Fri, 18 Apr 2025 03:18:36 GMT  
		Size: 770.3 MB (770298942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f15d00179ee682aea38643c863135d9c46d1fe4c78c3c171d3edf2e97a4ff57`  
		Last Modified: Fri, 18 Apr 2025 03:17:23 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ebc27c8de7fcbfa381ec8a19ec0a5981ea01c4eab3a38dcf9eb578366ada8af`  
		Last Modified: Fri, 18 Apr 2025 03:17:23 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102bc816db28bb4d9308aff47e5d34d11943265a480eaa0b1c76caec0fc77019`  
		Last Modified: Fri, 18 Apr 2025 03:17:23 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:windowsservercore` - windows version 10.0.20348.3566; amd64

```console
$ docker pull mongo@sha256:84ff67a7a24d9208322f58a11866513ea9b60d43f9871f67d334b3331c1262fd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3043903363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba0bca9b66b575156489428fa8e4f103f68180a31888b926ead2cd23e1bbe7d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Fri, 18 Apr 2025 03:22:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 18 Apr 2025 03:22:08 GMT
ENV MONGO_VERSION=8.0.8
# Fri, 18 Apr 2025 03:22:09 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.8-signed.msi
# Fri, 18 Apr 2025 03:22:10 GMT
ENV MONGO_DOWNLOAD_SHA256=4bf700912876c337697fa02bf4c38db0baed89604033b138e5e27d4e3eb743ee
# Fri, 18 Apr 2025 03:23:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:23:35 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 18 Apr 2025 03:23:35 GMT
EXPOSE 27017
# Fri, 18 Apr 2025 03:23:36 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0a799ed0baa2f08b457f4262f3681003590d226c51897e208f0ad4446a9f8f`  
		Last Modified: Fri, 18 Apr 2025 03:23:40 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c996944d9075a66673187943a5f15bebda3a7fa5edc6373e2e3fdb752ebf40bc`  
		Last Modified: Fri, 18 Apr 2025 03:23:40 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a4892383e4ce5ad2cd72d4214ecefff8d7e204b5515a2c3988a1a890e785b5`  
		Last Modified: Fri, 18 Apr 2025 03:23:40 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12debd4a8faf494521a140fdf5cbb3618d02ab3ea5ae37a37ec925ccf4cf42d5`  
		Last Modified: Fri, 18 Apr 2025 03:23:38 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3827c422be56a23d274a26d5f041950f768051ebe2adc6b6a4651cb73d5e807`  
		Last Modified: Fri, 18 Apr 2025 03:24:41 GMT  
		Size: 770.3 MB (770311827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6588518bb36c4adbc1d16c228d3bd8a60f91fe182cb5d6dccdd2e27d834a3f1c`  
		Last Modified: Fri, 18 Apr 2025 03:23:38 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e281d7ba2aec66d5ad3fff066e157e7c00142878b53a0f89838a3de966fb45`  
		Last Modified: Fri, 18 Apr 2025 03:23:38 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1da6b3b829ec1ae637036628cf9fb2bdf3800173a32af4aac02356b1bbb248`  
		Last Modified: Fri, 18 Apr 2025 03:23:38 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:windowsservercore` - windows version 10.0.17763.7249; amd64

```console
$ docker pull mongo@sha256:78412e6dcbbaaee1ad2591a64b56202326876d7cba85a00b5dbfb001cccce7b6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2935867325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26572edf84dc7d7b7c5deda6c75890e3a41a856320de57097026915b54b15abc`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:28:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 18 Apr 2025 03:28:40 GMT
ENV MONGO_VERSION=8.0.8
# Fri, 18 Apr 2025 03:28:41 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.8-signed.msi
# Fri, 18 Apr 2025 03:28:41 GMT
ENV MONGO_DOWNLOAD_SHA256=4bf700912876c337697fa02bf4c38db0baed89604033b138e5e27d4e3eb743ee
# Fri, 18 Apr 2025 03:31:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:31:06 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 18 Apr 2025 03:31:06 GMT
EXPOSE 27017
# Fri, 18 Apr 2025 03:31:07 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2f43a262d308cfe1f268287e4fe56c5ef247a93dee890eba1f83fc06ea2927`  
		Last Modified: Fri, 18 Apr 2025 03:31:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8693d0a96489660d79cc622375e5a68b93f769d636262b560e16c24981c831a9`  
		Last Modified: Fri, 18 Apr 2025 03:31:10 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6c5bd9c1e8cfa1f8894962056e9cfacdf08d8f949e9b563c2c586652cf49aa`  
		Last Modified: Fri, 18 Apr 2025 03:31:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23591c367ea3efce2db797fbe89ee62ead09fb3ebe93b7662c1db5a0defd9519`  
		Last Modified: Fri, 18 Apr 2025 03:31:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b595492909e0d220b0044379bd60f637e565fe24df29d5ef535655ebd56dd15e`  
		Last Modified: Fri, 18 Apr 2025 03:32:11 GMT  
		Size: 770.3 MB (770332486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9e1cd493039565bb8392cbef46fdb31c898536e6e86b12bea0b2f374eb6913`  
		Last Modified: Fri, 18 Apr 2025 03:31:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13f3c38e97424c30cb2ffe6b9ea782388b4965196cf42b6907b5f7482b39a85`  
		Last Modified: Fri, 18 Apr 2025 03:31:09 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0a1a5c4a5f14d76766678956edc63e6c7ac69f70bbf40fcf5d5b39cf35f30f`  
		Last Modified: Fri, 18 Apr 2025 03:31:09 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
