## `mongo:7-windowsservercore`

```console
$ docker pull mongo@sha256:3925f1ea182c08c9961031143a17c7e4744ad8d2c4dc41acb8fa3f0523663490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64
	-	windows version 10.0.17763.7314; amd64

### `mongo:7-windowsservercore` - windows version 10.0.26100.4061; amd64

```console
$ docker pull mongo@sha256:0e1e4c9afff4f906bd7ae470f04ac0e12b4784d0a5456867c5187d6513448fa4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 GB (4046708304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34293d281221888b2d190fd49f1cf2482a287133e3233e2eb8f44406a026f944`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Wed, 14 May 2025 21:01:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 May 2025 21:01:14 GMT
ENV MONGO_VERSION=7.0.20
# Wed, 14 May 2025 21:01:15 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.20-signed.msi
# Wed, 14 May 2025 21:01:16 GMT
ENV MONGO_DOWNLOAD_SHA256=960b961edb4b01a65d209a36cefe715c0cf14aea6a886853f2a31fb143790f55
# Wed, 14 May 2025 21:02:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 14 May 2025 21:02:33 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 14 May 2025 21:02:34 GMT
EXPOSE 27017
# Wed, 14 May 2025 21:02:35 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Thu, 15 May 2025 19:25:03 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab92c5eb1943b12ca707a29d479ba07117a09af929c4ed3663d9e84108e25571`  
		Last Modified: Fri, 16 May 2025 14:05:20 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc75dc23fd65d0d8770353580d71c5770835cc10140dcb962a1d95f579f52b85`  
		Last Modified: Fri, 16 May 2025 14:05:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b78ea95e31c01a21aa26557cf613cbed286790bf3bc9a7c209e59db643c09f8`  
		Last Modified: Fri, 16 May 2025 14:05:20 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a781548c1e860888de26f31bc00d5f007a825830b0c8f99c4542e290a22fe886`  
		Last Modified: Fri, 16 May 2025 14:05:20 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aba9935c84390256923338dd2d136b7e3bebc473826dcaecbec9d98c19607f`  
		Last Modified: Fri, 16 May 2025 14:05:33 GMT  
		Size: 615.9 MB (615933438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243c76ee5866d7bb9678521a5747939e162e6b36ff531af03cdfecfc1c3f04ad`  
		Last Modified: Fri, 16 May 2025 14:05:20 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba21027b164642ae8486e8649c901cd60627291c60e172e36832b6f5e6a7d047`  
		Last Modified: Fri, 16 May 2025 14:05:21 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde9223d42495ccd8b6de2defd8ad92d7ac823850c2e5c56ad0252e926788669`  
		Last Modified: Fri, 16 May 2025 14:05:22 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-windowsservercore` - windows version 10.0.20348.3692; amd64

```console
$ docker pull mongo@sha256:b957864168e3914b19d020698ba68d25224bfadc6f85368ee59b4971b32efd28
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2889575388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a24a30fd726ae026478cf1286d3307ecff5303e5ecc428f650c4432734455244`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Wed, 14 May 2025 20:58:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 May 2025 20:58:43 GMT
ENV MONGO_VERSION=7.0.20
# Wed, 14 May 2025 20:58:44 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.20-signed.msi
# Wed, 14 May 2025 20:58:45 GMT
ENV MONGO_DOWNLOAD_SHA256=960b961edb4b01a65d209a36cefe715c0cf14aea6a886853f2a31fb143790f55
# Wed, 14 May 2025 20:59:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 14 May 2025 20:59:57 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 14 May 2025 20:59:58 GMT
EXPOSE 27017
# Wed, 14 May 2025 20:59:59 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496bf096bfec7e24fab1a9b7efe38a80e0c990f9076a663fecc528ffab96c171`  
		Last Modified: Thu, 15 May 2025 20:08:09 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01833545347aafa929648bd5afdcfe528eb5aca8df3ae5aafca7e828d3c60f92`  
		Last Modified: Thu, 15 May 2025 20:08:09 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab43e1298892ba9ebac426a66b2b1f0a8b6ee46d5752df9345231b996aa626b9`  
		Last Modified: Thu, 15 May 2025 20:08:09 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c478528ad61ae2f6591e720f4f434736e5fa23ebb8221992182ce6c4fd3bcb87`  
		Last Modified: Thu, 15 May 2025 20:08:10 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ec7a0e2b9866dd6a6f6770b9bfa994f854acc21a1ba29714d4b869779dd048`  
		Last Modified: Thu, 15 May 2025 20:08:24 GMT  
		Size: 615.9 MB (615938167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1baf057db55350ef6dfb2e8b11cd87128998462dc8a54609e89d21801c125ca`  
		Last Modified: Thu, 15 May 2025 20:08:10 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca6b16f24979300973e2d18de08b96a6ad0c2a6dadacb69a2a11b1f39433cc2`  
		Last Modified: Thu, 15 May 2025 20:08:10 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452f4acc6e3f8cb0cb69b002a40f425cf92eb401014afbde3d12777828d4ceca`  
		Last Modified: Thu, 15 May 2025 20:08:10 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-windowsservercore` - windows version 10.0.17763.7314; amd64

```console
$ docker pull mongo@sha256:6b12be476d3e09dade8d21177626a8ae4aca47563dfea03c4d6348c603c4107f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2799690617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515934fec6625f26af95c820971f6a77b498e9abb9c8bb31e0579ef5c88ffea6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Wed, 14 May 2025 20:57:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 May 2025 20:58:00 GMT
ENV MONGO_VERSION=7.0.20
# Wed, 14 May 2025 20:58:01 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.20-signed.msi
# Wed, 14 May 2025 20:58:02 GMT
ENV MONGO_DOWNLOAD_SHA256=960b961edb4b01a65d209a36cefe715c0cf14aea6a886853f2a31fb143790f55
# Wed, 14 May 2025 21:00:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 14 May 2025 21:00:15 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 14 May 2025 21:00:16 GMT
EXPOSE 27017
# Wed, 14 May 2025 21:00:17 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Thu, 15 May 2025 19:24:26 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e090bdc5f5d5235631d6ac5107374d0ae26ee943ed6327356c765c5ad41dd5d6`  
		Last Modified: Fri, 16 May 2025 14:06:35 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4462b524c275081418b1c9bcd6e41abbea33c8380337c0b344ad890126880300`  
		Last Modified: Fri, 16 May 2025 14:06:34 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a4f6fb6ead544ef11cc8147c3f9d9c8b0909b8cf4cb96c34b89fd509be37e5`  
		Last Modified: Fri, 16 May 2025 14:06:35 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bd68b843e498bef5debf7e94792ec75ca04a235833a97e0b4add1e8e2a87e4`  
		Last Modified: Fri, 16 May 2025 14:06:35 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea5f378be8aa1801d4f7d151cc4b0b5e0777d9faa4a61790c9f6b1f258d8afe`  
		Last Modified: Fri, 16 May 2025 13:19:50 GMT  
		Size: 616.0 MB (615963618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6afb42bd84a3d89b153ec97659b5dc44a2b5208759b56dc967e02d37c964fda`  
		Last Modified: Fri, 16 May 2025 14:06:35 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ae980896c7db02c46ea2ed307de06c9e61490f5c9f3c66a2d6972c8d8fb8be`  
		Last Modified: Fri, 16 May 2025 14:06:35 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d261eeb0ef4f1001cdb0e55524cd56b4c91d145544dfdd14d080869f4a0488`  
		Last Modified: Fri, 16 May 2025 14:06:36 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
