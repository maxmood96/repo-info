## `mongo:8-windowsservercore`

```console
$ docker pull mongo@sha256:5619e53568ed01e4e8a86d766e277684baa4253936f65cb51b1c0ec089a2a8b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `mongo:8-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull mongo@sha256:5d7921c7a8df385add3bbae49de746d010c797719b8e8258290337c977a74ca0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3271274287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47dc70993579a2bb5272675ac5e0340defd9d489aefdd8ec669be468a3f729d3`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Mon, 24 Feb 2025 21:31:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 24 Feb 2025 21:31:48 GMT
ENV MONGO_VERSION=8.0.5
# Mon, 24 Feb 2025 21:31:48 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.5-signed.msi
# Mon, 24 Feb 2025 21:31:49 GMT
ENV MONGO_DOWNLOAD_SHA256=96b835f9cd76d4edfcdaa700c6d56aac47b1242541c05238d87c568c92db590e
# Mon, 24 Feb 2025 21:33:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 24 Feb 2025 21:33:22 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 24 Feb 2025 21:33:23 GMT
EXPOSE 27017
# Mon, 24 Feb 2025 21:33:24 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5c6f86bc5b91f6ce3021beaed74ff0007edd67d426d7f8efca89424459181b`  
		Last Modified: Mon, 24 Feb 2025 21:33:30 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e1fdaf741b797803ef5291e504bd0ea2881db1fdae54cf0a87ca311c3d5d1d`  
		Last Modified: Mon, 24 Feb 2025 21:33:30 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53545ccba179ca5c05bd36ff6d66620de259a4d3e53a4402938aab06f9e26a5`  
		Last Modified: Mon, 24 Feb 2025 21:33:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee20ec398a053ccc3f71067da1b6ec1e14cffcc2102de6a98e2917c3745da198`  
		Last Modified: Mon, 24 Feb 2025 21:33:28 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1801578596dd19be7f0a964f602ad91877864f8dcbcceefdf6c72c441e7633f7`  
		Last Modified: Mon, 24 Feb 2025 21:34:40 GMT  
		Size: 771.0 MB (770987566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9f1a7b48a714ff4466630e3054babe8260ae748a2fb9b0874d99174efe85ee`  
		Last Modified: Mon, 24 Feb 2025 21:33:28 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4001265539cbc3afcdd7d95e57ed51826f3607d2da9b71a06731f19f26f587be`  
		Last Modified: Mon, 24 Feb 2025 21:33:28 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bdba0f6991d8ced8e4505ab318ef9da3bc33eff424dd06c4da5884e0aebebe`  
		Last Modified: Mon, 24 Feb 2025 21:33:28 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:8-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull mongo@sha256:ac1f75e90aa981f7c05b62783d6b8fe281faaf950b8621ff84d9d97803808e22
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3034851783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eb92b7fddceb4425fd294cf9a989f1441e384c9f7d967d989a06b8facbf266e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Mon, 24 Feb 2025 21:38:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 24 Feb 2025 21:38:38 GMT
ENV MONGO_VERSION=8.0.5
# Mon, 24 Feb 2025 21:38:39 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.5-signed.msi
# Mon, 24 Feb 2025 21:38:39 GMT
ENV MONGO_DOWNLOAD_SHA256=96b835f9cd76d4edfcdaa700c6d56aac47b1242541c05238d87c568c92db590e
# Mon, 24 Feb 2025 21:40:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 24 Feb 2025 21:40:03 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 24 Feb 2025 21:40:04 GMT
EXPOSE 27017
# Mon, 24 Feb 2025 21:40:05 GMT
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
	-	`sha256:aed1955a54a0ada7d85bb224eaed23cd71f69440b545ca678531da009ebdfe29`  
		Last Modified: Mon, 24 Feb 2025 21:40:08 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557ab84b8249961b603325cd527d684cdd7cbdb13e83af81f5e5cb706a751072`  
		Last Modified: Mon, 24 Feb 2025 21:40:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0819825956ea690559527900402c65eb93f6dd246f97846a921cff69083a37`  
		Last Modified: Mon, 24 Feb 2025 21:40:08 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709f47f19a7c43b9648e31ddb529c646dce1525b5cde13be7c6c358df027631c`  
		Last Modified: Mon, 24 Feb 2025 21:40:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b003af40a6c1a7d520f85690d04d29b7cb394d58b9d002784df77c7470ade03`  
		Last Modified: Mon, 24 Feb 2025 21:41:11 GMT  
		Size: 771.0 MB (770984775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c635ad6951ee996a89ac6826edc17b154455a9813d9f2da44442943c0241a6c8`  
		Last Modified: Mon, 24 Feb 2025 21:40:07 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e78fd5b0ff882752dc87c43e803bb8ce3ecc4604ad03b8c9125d9c476ff372`  
		Last Modified: Mon, 24 Feb 2025 21:40:07 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d426b8bb15e7e59c9e5bcdca0d41d0deedf29dd5e1e39b23e26e4422262ffa02`  
		Last Modified: Mon, 24 Feb 2025 21:40:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:8-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull mongo@sha256:228241efe4b41daab2f2c5767db8c12b802e4158988628d1c442f757481788ff
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2907863718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838fb1be539f949cb1efd1d780c27b7231809ed42f4ada35f43b37a28e6f8dde`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Mon, 24 Feb 2025 21:33:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 24 Feb 2025 21:33:08 GMT
ENV MONGO_VERSION=8.0.5
# Mon, 24 Feb 2025 21:33:09 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.5-signed.msi
# Mon, 24 Feb 2025 21:33:10 GMT
ENV MONGO_DOWNLOAD_SHA256=96b835f9cd76d4edfcdaa700c6d56aac47b1242541c05238d87c568c92db590e
# Mon, 24 Feb 2025 21:35:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 24 Feb 2025 21:35:11 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 24 Feb 2025 21:35:12 GMT
EXPOSE 27017
# Mon, 24 Feb 2025 21:35:12 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e92e68724dfaaa9ab772da2da3d441ab5947bbff8b75d114e0b557c823f2bc9`  
		Last Modified: Mon, 24 Feb 2025 21:35:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0961beb41658f1922d56a249dc7c19c24b0434e4a421c5a45e0cf0265c7c1b2`  
		Last Modified: Mon, 24 Feb 2025 21:35:18 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed85ab2560ecb47e2ce805fc9a1fce9bc5d9a62412217c4480f3005874a6953e`  
		Last Modified: Mon, 24 Feb 2025 21:35:18 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03114086ce5239124a5b4bf04f0612059da21e93a0047ea984c7600df27d9063`  
		Last Modified: Mon, 24 Feb 2025 21:35:17 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a20f05c8746210ba5e05512edcba0f57f4680b8a8d808ffe64d4539e051a2ff`  
		Last Modified: Mon, 24 Feb 2025 21:36:17 GMT  
		Size: 770.9 MB (770945810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b0d72be10c3e166bc67839b897e831637b2044295758fa3e524f2bb23be185`  
		Last Modified: Mon, 24 Feb 2025 21:35:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39520b4e63544ba886cc8ecff7e9604fe5e8e5fac39751291ddf55405adda45f`  
		Last Modified: Mon, 24 Feb 2025 21:35:17 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990479fef073e7e15cceb2e7120d3413c647851ded815e582d4848a888e83855`  
		Last Modified: Mon, 24 Feb 2025 21:35:16 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
