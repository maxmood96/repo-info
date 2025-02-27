## `mongo:8-windowsservercore`

```console
$ docker pull mongo@sha256:f6fe4251ffced4000e2cd930250233960c0f9adbef714aa3af06c65404b282f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `mongo:8-windowsservercore` - windows version 10.0.26100.3194; amd64

```console
$ docker pull mongo@sha256:5dfc3c131eb7b45f61a68087ef28db6dd32104884749d13a2fa00075b96f22d8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3587555897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a530383b3d2b763ad535c8d058aa0dd9aa8c229c589cf88f9da8a4f339aa69`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Thu, 27 Feb 2025 18:19:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 27 Feb 2025 18:19:06 GMT
ENV MONGO_VERSION=8.0.5
# Thu, 27 Feb 2025 18:19:07 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.5-signed.msi
# Thu, 27 Feb 2025 18:19:08 GMT
ENV MONGO_DOWNLOAD_SHA256=96b835f9cd76d4edfcdaa700c6d56aac47b1242541c05238d87c568c92db590e
# Thu, 27 Feb 2025 18:20:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 27 Feb 2025 18:20:59 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 27 Feb 2025 18:20:59 GMT
EXPOSE 27017
# Thu, 27 Feb 2025 18:21:00 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eea1b5caca78df6a81cf5dbf75336d12105203526196d452d160a77b0f2ff40`  
		Last Modified: Thu, 27 Feb 2025 18:21:06 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43719fd1ef05624e5b20f83dcb6cb071de5398fc15af05fcea2db15bdd11b3e9`  
		Last Modified: Thu, 27 Feb 2025 18:21:06 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d751cc038810048e25e52a888043624ca90283ccaea705583b55572077f577c7`  
		Last Modified: Thu, 27 Feb 2025 18:21:06 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659ee272123e634b8e91ea5bea0fe600d441547608e635b20074411231b31d7c`  
		Last Modified: Thu, 27 Feb 2025 18:21:04 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2071296ce04491f0b0ec02d4dc624fde69300fcc7fea5216a154e80b52459945`  
		Last Modified: Thu, 27 Feb 2025 18:22:16 GMT  
		Size: 771.0 MB (770959254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06d41ddfeda25caac06513d817d5afd1a0cd534fdeabe9f345300f2ed666385`  
		Last Modified: Thu, 27 Feb 2025 18:21:04 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a429c66ba6b1c53398353ea6d89fb74556edc00ef74744708787c19cdab59685`  
		Last Modified: Thu, 27 Feb 2025 18:21:04 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ecb84d89e0122eb7f81ddf12f43fe56a2596f177ff7bc25f66099ac633cda15`  
		Last Modified: Thu, 27 Feb 2025 18:21:04 GMT  
		Size: 1.3 KB (1292 bytes)  
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
