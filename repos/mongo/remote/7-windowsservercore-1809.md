## `mongo:7-windowsservercore-1809`

```console
$ docker pull mongo@sha256:21612aedf8d865517123efac8db04b68bbca55a0189f2d7e4e643a4489ff494b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `mongo:7-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull mongo@sha256:c5c7810551db18d9139a18217bf9686ef24fb9aa4ea94c67494eb6b8ef828a01
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2782242027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d10663513160181e3e33ab6aad166870460628358f2db8bd59ec23a77c9e9d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:55:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Apr 2024 23:55:35 GMT
ENV MONGO_VERSION=7.0.8
# Tue, 09 Apr 2024 23:55:35 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.8-signed.msi
# Tue, 09 Apr 2024 23:55:36 GMT
ENV MONGO_DOWNLOAD_SHA256=30b8b6a96c5887a49e671ba72a7995279be7f232a666acd6717a59f7c68295f3
# Tue, 09 Apr 2024 23:57:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 09 Apr 2024 23:57:45 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 09 Apr 2024 23:57:46 GMT
EXPOSE 27017
# Tue, 09 Apr 2024 23:57:47 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb03856aa02b25ea345552422faf6679ec617be786f320ea02bb6db9aebdad1c`  
		Last Modified: Tue, 09 Apr 2024 23:57:53 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6fb1ebb7faf84bf58c74310b5b6af8643a5d110a081d3760c03d2a59cd012a`  
		Last Modified: Tue, 09 Apr 2024 23:57:53 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5f4d141e21ea4a0736f360a604a9c496e67d54ad743f874368c3eb68c0334e`  
		Last Modified: Tue, 09 Apr 2024 23:57:53 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddeec4f18bc6c6f54193d31873a7abeb49523e4babcbfeb664d9ff821ee6535c`  
		Last Modified: Tue, 09 Apr 2024 23:57:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea22064598a4516497927f12aec6e374bde3737213865e5171c73c1ed7b6bb82`  
		Last Modified: Tue, 09 Apr 2024 23:58:44 GMT  
		Size: 617.8 MB (617804988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b84ab6bd22a2f053b7d48f8872ce9d761e436c8aa6a0ec6ce60e64de4da1072`  
		Last Modified: Tue, 09 Apr 2024 23:57:51 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c089f9af27e5f3273765ddbbe23f79d6a783a83a5b59e09fc8202118a33933b`  
		Last Modified: Tue, 09 Apr 2024 23:57:51 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5659c97dfcab63f6bde47f8cbdbc929c4c66d6a1fb89bebaeb879b78a753a92a`  
		Last Modified: Tue, 09 Apr 2024 23:57:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
