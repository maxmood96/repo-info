## `mongo:8-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:5c4c54f38ec7474f57226cd8de99ef676a4044d26dba7375a88049af44c97010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `mongo:8-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull mongo@sha256:3b2716d3b20039834317b3ba2af1634fbb31030178705f293907a67b1cea9b06
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3066595888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134cc1e4b94c0e1dd22c41f90e23ca2a34e836f696a15fe127723ab567fb9e85`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Mon, 22 Sep 2025 22:11:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 22 Sep 2025 22:11:06 GMT
ENV MONGO_VERSION=8.0.14
# Mon, 22 Sep 2025 22:11:07 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.14-signed.msi
# Mon, 22 Sep 2025 22:11:07 GMT
ENV MONGO_DOWNLOAD_SHA256=9374f9eb0449d1099b31d89376ae47ba5e088ba7a9b0f5a9155435c8bc6567bb
# Mon, 22 Sep 2025 22:19:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 22 Sep 2025 22:19:21 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 22 Sep 2025 22:19:21 GMT
EXPOSE 27017
# Mon, 22 Sep 2025 22:19:22 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89a4021f8dc5fa397787c8c655f52bf5cf772acc20291d6286769158d5f83b9`  
		Last Modified: Mon, 22 Sep 2025 22:20:54 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b49840f8d9036c19e77e8434120e0338f532e38fc45265953846f20fd8922e`  
		Last Modified: Mon, 22 Sep 2025 22:20:54 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4ea5d94dc94bf92d43fe8953bedf8829431c223f4a434d2d57fa5d555c50e5`  
		Last Modified: Mon, 22 Sep 2025 22:20:54 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f73042271b3c7be7e2788969b8f68a78f0e2d8c429b2297aa881f665f8ff21`  
		Last Modified: Mon, 22 Sep 2025 22:20:54 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2bce694a973b9260face23883989156975dc4c629a489fcdcce2865338f71b`  
		Last Modified: Mon, 22 Sep 2025 23:11:54 GMT  
		Size: 784.4 MB (784441725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e441b680d7ac73c0d11b31cf8128033a2c9d4621b8221c8ec06ed16228a7fa`  
		Last Modified: Mon, 22 Sep 2025 22:20:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8c1f111134326750e8c74806ff90ffe8096ad57bbca8f462092353aa60f66c`  
		Last Modified: Mon, 22 Sep 2025 22:20:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d42ef08ca9bf87eb1dd2990fdc8645bedc2a95a366d92901dbb87a70ab88a0a9`  
		Last Modified: Mon, 22 Sep 2025 22:20:55 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
