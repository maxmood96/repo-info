## `mongo:8-windowsservercore`

```console
$ docker pull mongo@sha256:db7a2595c7a61492c27b9b876e74cc09c0cb719728769664ef4e64c6cd597eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `mongo:8-windowsservercore` - windows version 10.0.26100.4946; amd64

```console
$ docker pull mongo@sha256:ee911d38a94c375bb93bde321949a49ce93914561c6263765ff41059b8897380
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 GB (4280121658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e46750dfff5e141f14f82bad49ade8426bcdc5f3932b00f5232f1f121df97a8`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Thu, 21 Aug 2025 19:01:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 21 Aug 2025 19:01:20 GMT
ENV MONGO_VERSION=8.0.13
# Thu, 21 Aug 2025 19:01:21 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.13-signed.msi
# Thu, 21 Aug 2025 19:01:22 GMT
ENV MONGO_DOWNLOAD_SHA256=f301e2272fb222bf53b76883bbf95d07c54b116ad1e9e694234f002ad9abd0c4
# Thu, 21 Aug 2025 19:02:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 21 Aug 2025 19:02:49 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 21 Aug 2025 19:02:50 GMT
EXPOSE 27017
# Thu, 21 Aug 2025 19:02:51 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6731ebade47b83d0456704ba060b05ecede0c7a869279fa61d549108479c09`  
		Last Modified: Thu, 21 Aug 2025 19:06:45 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368aa22bccd0dceda3731de39b933efe36bd67fdd1ef67df9e4f14479648f436`  
		Last Modified: Thu, 21 Aug 2025 19:06:46 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcca905f4846901fe5206b8232f494d4e782e58399ff6134a6fa0de09c70821`  
		Last Modified: Thu, 21 Aug 2025 19:06:46 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e3cc73f048374c0b1393afc12e1a6c3c9f78670b46e74e5116ee215431368a`  
		Last Modified: Thu, 21 Aug 2025 19:06:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8207d831e25b20bf47ada7f98da235ae497d18cc34f99cc2b45051ef206a1839`  
		Last Modified: Thu, 21 Aug 2025 22:08:34 GMT  
		Size: 781.3 MB (781282009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6c1638c586fe492441f9b61d8b9afa8605500c71de6c683e1ee59b3f6fc423`  
		Last Modified: Thu, 21 Aug 2025 19:06:46 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a361b2fb064475060eaeb228ad07c22d25a009e38442bec6faa49be0a4033a`  
		Last Modified: Thu, 21 Aug 2025 19:06:46 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25f0198fe276e448151796772c8875644dbf8ebd11c001c96ac6bd9ea1c0153`  
		Last Modified: Thu, 21 Aug 2025 19:06:46 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:8-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull mongo@sha256:370fcba765597fddce561f88260ee64458bd74ac19468cb2f0418b852fbbf817
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3062918164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522dbc4a88105789e8c0bfc4b669f7c65c0038f2b14cfb855df2fbaa80cc2476`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Thu, 21 Aug 2025 18:55:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 21 Aug 2025 18:55:23 GMT
ENV MONGO_VERSION=8.0.13
# Thu, 21 Aug 2025 18:55:24 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.13-signed.msi
# Thu, 21 Aug 2025 18:55:25 GMT
ENV MONGO_DOWNLOAD_SHA256=f301e2272fb222bf53b76883bbf95d07c54b116ad1e9e694234f002ad9abd0c4
# Thu, 21 Aug 2025 18:57:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 21 Aug 2025 18:57:03 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 21 Aug 2025 18:57:05 GMT
EXPOSE 27017
# Thu, 21 Aug 2025 18:57:07 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a398ffdf2116e8203153d4a2010d3b8335ed46ace39b69c11d43c677b5b68773`  
		Last Modified: Thu, 21 Aug 2025 18:59:15 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01664d6b316dd43339b7ce9951677445d98dd306ebb579f2d33fe336d4165011`  
		Last Modified: Thu, 21 Aug 2025 18:59:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242519e4adbb04a23597f8d8354c9a9eae7592bf850d687f087ad69cdab0dbe3`  
		Last Modified: Thu, 21 Aug 2025 18:59:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa1155a342e54463039bbcf0b9ab67d92166e4bb14d52d0259815c4176ee590`  
		Last Modified: Thu, 21 Aug 2025 18:59:26 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5714e93de7889e806e04cd791163ebea19f916e61b0611e6616deb428da849ce`  
		Last Modified: Thu, 21 Aug 2025 19:08:50 GMT  
		Size: 781.2 MB (781217187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37286c77c1ed1801c4c7191b0ca558b90e40a46955293bcdae0b5898ecc8b5e`  
		Last Modified: Thu, 21 Aug 2025 18:59:48 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cf436510482e28fbf108a65ad198e78a9e09fe128fb98a836a8ecee69872df`  
		Last Modified: Thu, 21 Aug 2025 18:58:45 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb18df2a82fc3950680865b4adf062cf38bb8e4221ad2ee9ab60cfc4c164770`  
		Last Modified: Thu, 21 Aug 2025 18:58:45 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
