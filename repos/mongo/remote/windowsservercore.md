## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:7277090c376c0ef8a248a96e75b8b06729224fa2b4ddf2179fdae5a00eb78a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `mongo:windowsservercore` - windows version 10.0.26100.3775; amd64

```console
$ docker pull mongo@sha256:156d32d6e5d6c4e258367c0547300e586181383fd7ce44df5d301ad72926357d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 GB (4165014464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3dd7f6d282fc634f83b507a56dd2b5c2380b7034a0d3539a3e88673d27ee195`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Mon, 14 Apr 2025 23:04:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 14 Apr 2025 23:04:27 GMT
ENV MONGO_VERSION=8.0.8
# Mon, 14 Apr 2025 23:04:29 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.8-signed.msi
# Mon, 14 Apr 2025 23:04:30 GMT
ENV MONGO_DOWNLOAD_SHA256=4bf700912876c337697fa02bf4c38db0baed89604033b138e5e27d4e3eb743ee
# Mon, 14 Apr 2025 23:06:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 14 Apr 2025 23:06:03 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 14 Apr 2025 23:06:04 GMT
EXPOSE 27017
# Mon, 14 Apr 2025 23:06:05 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82028042ef11bde09d30dfc8e76c04bb0549ef5343f040d0f35211f18c922f16`  
		Last Modified: Mon, 14 Apr 2025 23:06:09 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43868b7b7ed83ddd09a90df0280281b5acc55b6b00ed9f7678e2287cd4517565`  
		Last Modified: Mon, 14 Apr 2025 23:06:09 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b82926b66a6b878b37c07f222b6117186b25e64dbd4e3f75a0679164c2e23a`  
		Last Modified: Mon, 14 Apr 2025 23:06:09 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8fc0295e5d9dc3c8a7da88556d324f0cb4f141f64421abb63ad66d07a3b461`  
		Last Modified: Mon, 14 Apr 2025 23:06:08 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5681951b04cc47982ae75d3bd6e4182235b9fd2c8982bf0eb7cf46104a964f`  
		Last Modified: Mon, 14 Apr 2025 23:07:21 GMT  
		Size: 770.3 MB (770325704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7bc91a9e00753d2ec07332142a5e238e2b2a96e2e6abc6fbe0a7cc215577e34`  
		Last Modified: Mon, 14 Apr 2025 23:06:08 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a9ec1eac9d9c10aba98576cffdde6a77c63dac0dded08194c5355075a58aae`  
		Last Modified: Mon, 14 Apr 2025 23:06:08 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5be0fa93a35a40def8901bc87cb62976e71f71d800ea8a7b9b1e98eba5ef26`  
		Last Modified: Mon, 14 Apr 2025 23:06:08 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:windowsservercore` - windows version 10.0.20348.3453; amd64

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

### `mongo:windowsservercore` - windows version 10.0.17763.7136; amd64

```console
$ docker pull mongo@sha256:58103ae024c00b16ed46b55189fc2218a86cd354458b479a36615667c0b9e97a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2933050052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebea519f0c160bb90e3dc16480e64595e3204ff09e64b6f84dc18c3eff71b39`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Mon, 14 Apr 2025 23:07:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 14 Apr 2025 23:07:09 GMT
ENV MONGO_VERSION=8.0.8
# Mon, 14 Apr 2025 23:07:10 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.8-signed.msi
# Mon, 14 Apr 2025 23:07:11 GMT
ENV MONGO_DOWNLOAD_SHA256=4bf700912876c337697fa02bf4c38db0baed89604033b138e5e27d4e3eb743ee
# Mon, 14 Apr 2025 23:09:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 14 Apr 2025 23:09:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 14 Apr 2025 23:09:18 GMT
EXPOSE 27017
# Mon, 14 Apr 2025 23:09:18 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba63a614e4961406ee57f2b3cbbf0e9f2f575d620b30e1c4d0d3587d7dd908b`  
		Last Modified: Mon, 14 Apr 2025 23:09:22 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6083570406ee1589ca6f567b74f28f6cd28ece847e898feea5318b29257ca5`  
		Last Modified: Mon, 14 Apr 2025 23:09:22 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94f6dbd82b369ee4f4463a1c11a2e119c9b079f1ecf258919133788e8f8b43c`  
		Last Modified: Mon, 14 Apr 2025 23:09:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f463dee2349393ec3d7c86edf41226311943db5213411471b6b81530bb18a2`  
		Last Modified: Mon, 14 Apr 2025 23:09:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84273db5c5b344d59a16022ebed0cd2008087d9fb794392de7b24b99a275171d`  
		Last Modified: Mon, 14 Apr 2025 23:10:23 GMT  
		Size: 770.3 MB (770315156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afb484edc3ec136e9329243d3942a86b67c2374a5305fb99514e399b9c0e41d`  
		Last Modified: Mon, 14 Apr 2025 23:09:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7636dc854e4edfb4d9c26e90420ce3253ac61782cf47859fccb3e8d012548a6`  
		Last Modified: Mon, 14 Apr 2025 23:09:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382d52a299fe0a0570c9ec85876bedf3e6005d4584f248db2d495d3dc646ef91`  
		Last Modified: Mon, 14 Apr 2025 23:09:21 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
