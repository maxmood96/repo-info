## `mongo:5-windowsservercore`

```console
$ docker pull mongo@sha256:4b119f02a7754fee4375daeaf2ceb6568f57841f59e1b7a4f810ecc1f7941671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2527; amd64
	-	windows version 10.0.17763.5936; amd64

### `mongo:5-windowsservercore` - windows version 10.0.20348.2527; amd64

```console
$ docker pull mongo@sha256:d5ce1ef95f9c4e7fd3e6636123455c5edc654d666a508d41e11406dd83333f5f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2430708526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11469d3a262c7720146c9fa54ce5921166eccd08f398107fe7ec281798d6ecfc`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jun 2024 09:02:12 GMT
RUN Install update 10.0.20348.2527
# Wed, 12 Jun 2024 18:11:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jun 2024 18:11:39 GMT
ENV MONGO_VERSION=5.0.27
# Wed, 12 Jun 2024 18:11:40 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.27-signed.msi
# Wed, 12 Jun 2024 18:11:41 GMT
ENV MONGO_DOWNLOAD_SHA256=3da3dc8c13ddb8405c230c8495d4412d9a847b6c24e937b63c6b67437984a175
# Wed, 12 Jun 2024 18:12:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 18:12:32 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Jun 2024 18:12:34 GMT
EXPOSE 27017
# Wed, 12 Jun 2024 18:12:35 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedf08888525e83e4a050655b4ec0d81647e59a69f7007a560df774a656da9bb`  
		Last Modified: Tue, 11 Jun 2024 17:49:21 GMT  
		Size: 729.6 MB (729579921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ef61f61f6d49355740531a8749d9a306e3d2340c6b91a611b085a8698a4176`  
		Last Modified: Wed, 12 Jun 2024 18:12:38 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b70b86ac1f6979b98fb1bc3ad41c2af507fc211bfe98e1973ab23909f96480d`  
		Last Modified: Wed, 12 Jun 2024 18:12:38 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d06448a25de6746ca2efdd02eaeb68a94525cb488a4b400f0ecb8a9afb6df09`  
		Last Modified: Wed, 12 Jun 2024 18:12:38 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257af852bc1b548f43ab734055ba76a8c342bb7d4b947a5c4764030090264b32`  
		Last Modified: Wed, 12 Jun 2024 18:12:37 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bfdd9dea5735fa0c6915f777e4f9a0cf21b79898826c88dba8df27543dbcd60`  
		Last Modified: Wed, 12 Jun 2024 18:13:08 GMT  
		Size: 312.5 MB (312520779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20a7b0c5208f5e6809442e2c2bd1c8e071c9d2982bd50e26df061f6f430dc23`  
		Last Modified: Wed, 12 Jun 2024 18:12:37 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d03e7619fc64cc74c3aecee651eb04ad0d9b41db5393b079cbea0d12c46acbe`  
		Last Modified: Wed, 12 Jun 2024 18:12:37 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1127ed2e7e3fb0d5c790719d9355a9579aad9369eac4e05587b6cd9cd6fb996a`  
		Last Modified: Wed, 12 Jun 2024 18:12:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-windowsservercore` - windows version 10.0.17763.5936; amd64

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
