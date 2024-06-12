## `mongo:5-windowsservercore-1809`

```console
$ docker pull mongo@sha256:685c7c1344d2132f1bc9d4bdb020429fd5abb4b67e37d09b2656a54e0ebfedf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `mongo:5-windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull mongo@sha256:90d019da03de4ab3475bfb72ded4c60d047ac0f94ef99d8c8085a1c336c5195c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2533364113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2daa97cace31565640dd454c6a0d6d04c51cef62884d6574a2d791c3d9320c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:08:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jun 2024 18:08:23 GMT
ENV MONGO_VERSION=5.0.27
# Wed, 12 Jun 2024 18:08:24 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.27-signed.msi
# Wed, 12 Jun 2024 18:08:25 GMT
ENV MONGO_DOWNLOAD_SHA256=3da3dc8c13ddb8405c230c8495d4412d9a847b6c24e937b63c6b67437984a175
# Wed, 12 Jun 2024 18:09:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 18:09:57 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Jun 2024 18:09:58 GMT
EXPOSE 27017
# Wed, 12 Jun 2024 18:09:58 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f5d5fab7e7e90fe807405848691803dd708611ebe13339878beb4c9dd3a5a1`  
		Last Modified: Wed, 12 Jun 2024 18:10:05 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3379cb2f35d91a12775d1dd42d0fe0de28c395d4a980ea4f457cefbe1f76bcfa`  
		Last Modified: Wed, 12 Jun 2024 18:10:05 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6666bcabde464ce835a869137478487c75da69471c732687d5d71ea8cdeccb`  
		Last Modified: Wed, 12 Jun 2024 18:10:05 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8892d1daf4e3436888bd27dd5a1ea655f027c5615de96609a1c657d763ebc4e6`  
		Last Modified: Wed, 12 Jun 2024 18:10:03 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270d5d09ff286d30a69d5556a9c992ef6def3d43740c9a2c3593907e8bb91154`  
		Last Modified: Wed, 12 Jun 2024 18:10:33 GMT  
		Size: 312.7 MB (312673859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e66479dca153dc6cce858ff067207540a60afa627f5890d72c5b18d0fb5f1e`  
		Last Modified: Wed, 12 Jun 2024 18:10:03 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbbee1fb9646e229ff50fc47d71cd04f01bc08d6db59412d27c2ef60737540f`  
		Last Modified: Wed, 12 Jun 2024 18:10:03 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3caefeebdbcefa5939641a020c632e61c56825acf60c932575e49701ba61de`  
		Last Modified: Wed, 12 Jun 2024 18:10:03 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
