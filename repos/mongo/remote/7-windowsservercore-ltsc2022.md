## `mongo:7-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:3d147ed3a44b37c5c9c267ec7c557946fbf777006555245306be2706d7ecfbd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `mongo:7-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull mongo@sha256:26faeab38bef8e730abdf3167a608c0ba8cd3fd06b1b1e22c2a00c49af4b15d6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2874142532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2159ba3da5ca34919d5a0a4e2b1df62e9f5a503feb834da5300bb4e92e6ddf11`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:38:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Jan 2025 23:38:30 GMT
ENV MONGO_VERSION=7.0.16
# Tue, 14 Jan 2025 23:38:30 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.16-signed.msi
# Tue, 14 Jan 2025 23:38:31 GMT
ENV MONGO_DOWNLOAD_SHA256=88fe05d7f324e72b9d17cbfe9bde652053c398efc7cffc0249c944faf4f32b34
# Tue, 14 Jan 2025 23:39:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:39:29 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 14 Jan 2025 23:39:32 GMT
EXPOSE 27017
# Tue, 14 Jan 2025 23:39:32 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 21:54:27 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99da154f03cda75cb9e265eda863c10d649b2cb0e007df8d5f49361ea3c17a0b`  
		Last Modified: Thu, 06 Feb 2025 06:04:54 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d63ca1aa2aa20bc350bee462be98293a3b646528fb101cef50057ebfd2bd156`  
		Last Modified: Thu, 06 Feb 2025 06:04:55 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfed260c290681dc38b0c4e2c9119e2a2d7482172edf2667d951aec3ff27c7c1`  
		Last Modified: Tue, 04 Feb 2025 10:31:28 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2566f755c76d01602d1c73d2d266e96a8be4f11d4fd011796bd387c3286a30d8`  
		Last Modified: Wed, 05 Feb 2025 17:04:13 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516fc85399234656cf0d4d7d6a870ffb733270721b5f54b3752380dd64ed5e2d`  
		Last Modified: Tue, 04 Feb 2025 18:43:50 GMT  
		Size: 611.7 MB (611748274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e82ff92b7acff039be424b820f535a3c1fdb17dfc993487b96c9e301b2d9be`  
		Last Modified: Thu, 06 Feb 2025 06:04:58 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9109d97f7d15c60eb382391c9ed858597367fe6f4294df809bfad4f6ae0d958f`  
		Last Modified: Wed, 05 Feb 2025 06:03:47 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0eb9a4429420d5da43e6c3bcd2fa2e752dc880d214878fbba9a6257da56367e`  
		Last Modified: Tue, 04 Feb 2025 18:43:33 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
