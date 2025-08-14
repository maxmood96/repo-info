## `mongo:8-windowsservercore`

```console
$ docker pull mongo@sha256:000f1d8c6bd564fe2b2f66883430f64108f2a0409b472b93ab00674aeab64a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `mongo:8-windowsservercore` - windows version 10.0.26100.4946; amd64

```console
$ docker pull mongo@sha256:9559700aa5023d07104d2d75dafc7c566cd7eb048618a1c128d864e3dd7c43c1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 GB (4276638366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85353faeaa4db214a5c390f901fb3897aaf7ab2efdc9836114b2b03e99b5f923`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 12 Aug 2025 20:27:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 Aug 2025 20:27:59 GMT
ENV MONGO_VERSION=8.0.12
# Tue, 12 Aug 2025 20:28:00 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.12-signed.msi
# Tue, 12 Aug 2025 20:28:00 GMT
ENV MONGO_DOWNLOAD_SHA256=19d8820364f55dfde5724b2d99520be8aadb62d15486a71295457ff071565d80
# Tue, 12 Aug 2025 20:29:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:29:00 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 12 Aug 2025 20:29:01 GMT
EXPOSE 27017
# Tue, 12 Aug 2025 20:29:01 GMT
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
	-	`sha256:05f3c18358d440940935dae03d80a368bb02a6119703702b547e204ae36c27de`  
		Last Modified: Tue, 12 Aug 2025 20:56:46 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa149a3e25d7c087c46afb7ee19527b7ee779218b193f3cdafdeed8d4b5e878`  
		Last Modified: Tue, 12 Aug 2025 20:56:49 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16894e7775d0a35ed307a9ab6bfefcd3024f1d52823fdc23484182158f632637`  
		Last Modified: Tue, 12 Aug 2025 20:56:52 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4cc0084928bc6300be0b4aba74ecdfa5807b70420b64b3c5bd3d7ced0d2249`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036f82926034406f23fa96ef6f2dbd1d93b4526d1d90b64d11a0bc68e80b7a4c`  
		Last Modified: Tue, 12 Aug 2025 22:10:03 GMT  
		Size: 777.8 MB (777798694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267346b8dbdf8c7445884a8e1ed23c828a22eb0081858392c09cb8bda5fff50b`  
		Last Modified: Tue, 12 Aug 2025 20:56:57 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbf2542c25e605c70d304cadf9bcaedb29335a25ab53bac5631418f5f487bc4`  
		Last Modified: Tue, 12 Aug 2025 20:57:02 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ccaf0ff385a09da18f6a5e9424312ca4a11e30397e6693bcb005f05d1e551b`  
		Last Modified: Tue, 12 Aug 2025 20:57:06 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:8-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull mongo@sha256:8036c766cb5e63777a8bc8a37dc00309ea7a44f7d13c14c3d1e0aa05376ec0a8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3059536716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ea3e6b7f695600bb28c794c1b19f4a138c20648e01d9538f3c02ceee41eb24`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:27:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 Aug 2025 20:27:22 GMT
ENV MONGO_VERSION=8.0.12
# Tue, 12 Aug 2025 20:27:23 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.12-signed.msi
# Tue, 12 Aug 2025 20:27:24 GMT
ENV MONGO_DOWNLOAD_SHA256=19d8820364f55dfde5724b2d99520be8aadb62d15486a71295457ff071565d80
# Tue, 12 Aug 2025 20:28:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:28:33 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 12 Aug 2025 20:28:34 GMT
EXPOSE 27017
# Tue, 12 Aug 2025 20:28:35 GMT
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
	-	`sha256:4535cb6567046f6692dd2ddb6e91a32b70370f5732e7cb7bdf6cf698ac6573c7`  
		Last Modified: Tue, 12 Aug 2025 20:30:11 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fee7bb3c3e8b641d8dc88237b0f370188d595b2617ad35654bb263e8e1f869f`  
		Last Modified: Tue, 12 Aug 2025 20:30:10 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51be72a6173875ab91192e4b7992fa2e06b2fba88115393408335a5c18926eb7`  
		Last Modified: Tue, 12 Aug 2025 20:30:10 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4380aeb953ae1e8abd721eb16328f2a962254b6e7873ca9ef4fb82311af0b91`  
		Last Modified: Tue, 12 Aug 2025 20:30:02 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4d07a5cfa1f25f486ff5c28726e73e6f432f398f87c36469d0eb235290e98d`  
		Last Modified: Tue, 12 Aug 2025 20:45:31 GMT  
		Size: 777.8 MB (777835516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c23f55f453346fb227106c4263761fd8016aaf0f73b8dfa31af0e3637f518ef`  
		Last Modified: Tue, 12 Aug 2025 20:30:02 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92edad597286f386feb17c0dd3eba9cace21a996dab8c4bca0d8583b3b97741c`  
		Last Modified: Tue, 12 Aug 2025 20:30:02 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0f899b7f265c367aea22006826848401ecbdaeee2e9cff6a8ca7799ae5691a`  
		Last Modified: Tue, 12 Aug 2025 20:30:02 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
