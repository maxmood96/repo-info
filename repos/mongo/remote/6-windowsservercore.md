## `mongo:6-windowsservercore`

```console
$ docker pull mongo@sha256:6008dd1df9a7f0ba9b09a65da55d5acd07ae553fe88420da789aebb6bb0be19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2113; amd64
	-	windows version 10.0.17763.5122; amd64

### `mongo:6-windowsservercore` - windows version 10.0.20348.2113; amd64

```console
$ docker pull mongo@sha256:88c0d7fec6d7adc19d7dab65014a33c4cba0097abb0359d878a3b98bc31a91ab
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2405357076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94adafc1dfb2f988c5b5d61ea7daa58a7fcf8f0101f49f88ec918377b0a0c99`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 03:18:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 29 Nov 2023 01:25:51 GMT
ENV MONGO_VERSION=6.0.12
# Wed, 29 Nov 2023 01:25:51 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.12-signed.msi
# Wed, 29 Nov 2023 01:25:52 GMT
ENV MONGO_DOWNLOAD_SHA256=126024e5292da3470eb119d798d11862ce1f0472836bce7d3210dcb522b80aa3
# Wed, 29 Nov 2023 01:27:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 29 Nov 2023 01:27:49 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 29 Nov 2023 01:27:50 GMT
EXPOSE 27017
# Wed, 29 Nov 2023 01:27:51 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a73dc3dec59ae25ff1232f5fdf2ab39df387f3bf86ba48717ff271d76c2feb`  
		Last Modified: Thu, 16 Nov 2023 04:19:26 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732d892349deaff33a45e30c8756808d574a17744b699e3dda8d7d364d3cc198`  
		Last Modified: Wed, 29 Nov 2023 01:55:30 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4535a542dbfab69d2c3d48d64f25e559fec23c5530cc3c3d933f2482aa626545`  
		Last Modified: Wed, 29 Nov 2023 01:55:29 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea3c88b6ea544690563fe9f82e116915f0fa825641fc1e85b570a875e4ba38f`  
		Last Modified: Wed, 29 Nov 2023 01:55:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1739394a86b4792bb47737b8ee7c2ffe5bfa63fe19015b2b71ebbfe1d025aa2e`  
		Last Modified: Wed, 29 Nov 2023 01:56:50 GMT  
		Size: 518.6 MB (518566127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40e6ed9eb1c759afef0c63352338598aef89930d523f0a5ae584055bad1dc16`  
		Last Modified: Wed, 29 Nov 2023 01:55:27 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b056128864ae26c17316bd619ffe2d7028065794a4e8bdb2cbe42c549fbdc33`  
		Last Modified: Wed, 29 Nov 2023 01:55:28 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78874cad1a15c0141d0302c239ebde5a4ec36c4df97e50df896a1463d2988432`  
		Last Modified: Wed, 29 Nov 2023 01:55:27 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-windowsservercore` - windows version 10.0.17763.5122; amd64

```console
$ docker pull mongo@sha256:3194646e5901cb68301d53d7718df615d954bedfd015c90a5cfb5843967f24f4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2576062059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633e1ef024f3242a484e25e44591fe6283db2764562862004840228a5921e653`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 03:20:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 29 Nov 2023 01:28:04 GMT
ENV MONGO_VERSION=6.0.12
# Wed, 29 Nov 2023 01:28:05 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.12-signed.msi
# Wed, 29 Nov 2023 01:28:06 GMT
ENV MONGO_DOWNLOAD_SHA256=126024e5292da3470eb119d798d11862ce1f0472836bce7d3210dcb522b80aa3
# Wed, 29 Nov 2023 01:30:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 29 Nov 2023 01:31:01 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 29 Nov 2023 01:31:02 GMT
EXPOSE 27017
# Wed, 29 Nov 2023 01:31:04 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e4111e1324ff2110def2382c3796071edd92a76a262efa6c0657d549b64496`  
		Last Modified: Thu, 16 Nov 2023 04:21:07 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a8cff90a7f6d7cbf33d1b6618bb7460391e65df4052f7271d4d3f640e07571`  
		Last Modified: Wed, 29 Nov 2023 01:57:04 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64e6f5d202d36b005b43e3f432c51d07f0cdeeb8da538e676fdc4bde6bf9345`  
		Last Modified: Wed, 29 Nov 2023 01:57:04 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137793d682091952db56593758a585d6a28831510365f14acc7dd3b8ef04f192`  
		Last Modified: Wed, 29 Nov 2023 01:57:02 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:629f946bfe29f99c72b6dc0422cb373da8eae06e4fd7b271427427c6b329c9a6`  
		Last Modified: Wed, 29 Nov 2023 01:58:24 GMT  
		Size: 518.6 MB (518620629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d77944d1e6a1735a0096f3634ccd28c98c32c6be373b3f20062e95f2b79c809`  
		Last Modified: Wed, 29 Nov 2023 01:57:02 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7995644d2f34c266d4dbf40a275c8071cf5ad132bf3a58eeb8e6fa7b768d5a`  
		Last Modified: Wed, 29 Nov 2023 01:57:02 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5656d44405902b9a06976024b696ee8eba4166b91a8a5f67deb8546ccf6ed7b`  
		Last Modified: Wed, 29 Nov 2023 01:57:02 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
