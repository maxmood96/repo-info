## `mongo:7-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:147bace7bc6b0fed2010849dc4478ae5777d9ce1abab8ff1c7a07ee902aed190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `mongo:7-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

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
