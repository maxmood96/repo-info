## `mongo:windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:2f45831e42ac446a46b242d0539ba594944a66b40c26b23bd6c33565901efbaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `mongo:windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

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
