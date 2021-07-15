## `mongo:4-windowsservercore-1809`

```console
$ docker pull mongo@sha256:b08fd38f6cf0bb21c862aad9ae49350501c58f55dcc01195202b5781206e375a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `mongo:4-windowsservercore-1809` - windows version 10.0.17763.2061; amd64

```console
$ docker pull mongo@sha256:9f81412c559373d4b631854cddb2c737078e01fb8e3e165c22f3bbfadbb49179
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2917200425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52175f0f3eef21c8d64b87953686780654173b35b6c24c8f3195170bacda610`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 06 Jul 2021 20:34:18 GMT
RUN Install update 1809-amd64
# Wed, 14 Jul 2021 01:07:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jul 2021 01:36:18 GMT
ENV MONGO_VERSION=4.4.6
# Wed, 14 Jul 2021 01:36:21 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.6-signed.msi
# Wed, 14 Jul 2021 01:36:24 GMT
ENV MONGO_DOWNLOAD_SHA256=ede50e8f8d8c9d23a8ca2cc1c96cdb9bcc1f617930e8bd1d46f21d95d0b555f8
# Wed, 14 Jul 2021 01:38:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 14 Jul 2021 01:38:57 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 14 Jul 2021 01:39:00 GMT
EXPOSE 27017
# Wed, 14 Jul 2021 01:39:03 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f143c6fed32d477c35b660b2e108ea62e3593c03e44bd9ced208ce52b26b0841`  
		Size: 967.1 MB (967113907 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:adcec6ff907307155c0652222cc9b95a0cc964d4c371e02767e72a5c90472192`  
		Last Modified: Wed, 14 Jul 2021 02:02:19 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a780c3e6fa770d22210417e5c5a3a4d2e668bbe4c1a7ab3b994ea2719d8228`  
		Last Modified: Wed, 14 Jul 2021 02:12:52 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46669403d8fafe018b0a4e4d6e14632750ca0a27a9a55080b629b0dfd529d4bb`  
		Last Modified: Wed, 14 Jul 2021 02:12:52 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107031e7a04ac681ff25d8535834efe05bdef0d984fef624bbae1c7d6b69e3f9`  
		Last Modified: Wed, 14 Jul 2021 02:12:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff0c2c8f7108d4eaa33602ab00eb6d39d7e1ce8824aeffd94c035465990cd1c`  
		Last Modified: Wed, 14 Jul 2021 02:13:39 GMT  
		Size: 231.7 MB (231743703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67f4d8a65c90add62186cc8ae941f212e96721c2fb2347c7ccd470da5bc2ecf`  
		Last Modified: Wed, 14 Jul 2021 02:12:49 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5c5f42452ad4c28ca80f2c09b5f68f79c632a33c951ef7671316c8fbbf10e7`  
		Last Modified: Wed, 14 Jul 2021 02:12:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea66cf39f7f3b7920dbfa9707c29937c26715c6186e25922160353777e61e527`  
		Last Modified: Wed, 14 Jul 2021 02:12:49 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
