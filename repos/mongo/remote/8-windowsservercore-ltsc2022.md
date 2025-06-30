## `mongo:8-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:a6e0bad8bda6e06b1979645de3cc587c50e37cde95960402cf81ad1d36bd17b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `mongo:8-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull mongo@sha256:54d8bb048b8810ca92f8e4bced97a98382b3eeba4e67567af52624d29d5f18f8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3055879801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f455d0fc0b2bbe396880ecf71422304e0823db1cb60e098032ab6752319210`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Mon, 30 Jun 2025 17:27:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 30 Jun 2025 17:27:23 GMT
ENV MONGO_VERSION=8.0.11
# Mon, 30 Jun 2025 17:27:23 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.11-signed.msi
# Mon, 30 Jun 2025 17:27:24 GMT
ENV MONGO_DOWNLOAD_SHA256=887b2869804fec5f7412f4d848ab6bc587819fb2ee1ab49e2fac1538ccc53a91
# Mon, 30 Jun 2025 17:28:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 30 Jun 2025 17:28:44 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 30 Jun 2025 17:28:45 GMT
EXPOSE 27017
# Mon, 30 Jun 2025 17:28:46 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f719d54f40344d1f06ae72ea3d918295e9070130c07b6b67a23ecd457abcf2`  
		Last Modified: Mon, 30 Jun 2025 17:29:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf5ac817fd80b4bcb5442cd3e27188a9709b7df446e510df175eaef0171333f`  
		Last Modified: Mon, 30 Jun 2025 17:29:57 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8177af34a2a0a2735dc40be6a7189d5854c2e8be271550cabfbd3af50c2f9624`  
		Last Modified: Mon, 30 Jun 2025 17:29:57 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcda42e73cbf2d3676f05a32d0b7e3fbeef49935203b6d3a8a2325d03e2bd4a3`  
		Last Modified: Mon, 30 Jun 2025 17:29:57 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c18b7acfe7c9364937692224bdbf0bfe4f2e1611fb572e3c204b1325cb80e9`  
		Last Modified: Mon, 30 Jun 2025 17:36:53 GMT  
		Size: 775.6 MB (775619222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e69835ec0dff50ac4476db553949e116c13ec27a1499772ce18034ec2dd475`  
		Last Modified: Mon, 30 Jun 2025 17:29:57 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c22e6b0a404b0082f6274e06fa0f4a8975e1a54bbbf32e0c07073769d3ce4e`  
		Last Modified: Mon, 30 Jun 2025 17:29:57 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6526556be0e00104bb9641575b698a32747333be17472aba87d960e448201d0`  
		Last Modified: Mon, 30 Jun 2025 17:29:57 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
