## `mongo:4-windowsservercore-1809`

```console
$ docker pull mongo@sha256:b0d4d606ab3e2eff2e2dca1ec5c8fd18db97ab66262f77e8ca7921ad1ebda49a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5206; amd64

### `mongo:4-windowsservercore-1809` - windows version 10.0.17763.5206; amd64

```console
$ docker pull mongo@sha256:6031ed47aee981bee621dcb5059ad3c5858f88ce3889803babe323dd83efc6b3
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2305899016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1234ba6321fb35a412ef277aeddfdd0432d1d4db327ad9c99bb0aae91841054`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Thu, 04 Jan 2024 19:56:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 04 Jan 2024 19:56:45 GMT
ENV MONGO_VERSION=4.4.27
# Thu, 04 Jan 2024 19:56:46 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.27-signed.msi
# Thu, 04 Jan 2024 19:56:46 GMT
ENV MONGO_DOWNLOAD_SHA256=ab6b645db3ec289fb199a5ee2e1d99704add3fb9e801ebe4d87158eb2716aeb4
# Thu, 04 Jan 2024 19:59:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 04 Jan 2024 19:59:19 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 04 Jan 2024 19:59:20 GMT
EXPOSE 27017
# Thu, 04 Jan 2024 19:59:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751655b5a5697fec0ea76f626cfc302cb3478d86e92935c95b319f001b69168d`  
		Last Modified: Thu, 04 Jan 2024 19:59:27 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a97b091ad76a4e2f6fba843fa588b1c77ba70e02b0950ed7554a58d6eac90b`  
		Last Modified: Thu, 04 Jan 2024 19:59:27 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76444a38ecd5ea88238dc85544820279b41c473e4ff6857ba139070ad5fb3ead`  
		Last Modified: Thu, 04 Jan 2024 19:59:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4271f9e562b1f9c8d42ae6b15805c9a84b0ecaefe61288e9f9efd37222c756`  
		Last Modified: Thu, 04 Jan 2024 19:59:25 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6bb60b97f4c8097702a7b9949d102686663e2e6f38d03e6d055c320a8704c9`  
		Last Modified: Thu, 04 Jan 2024 19:59:49 GMT  
		Size: 246.2 MB (246180891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4780cd0eaa59e96c190221879ae535ca6e0be9c10391fcd1a1dd1faaed80ca0`  
		Last Modified: Thu, 04 Jan 2024 19:59:25 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8545f6734858360588c1b33dcf02b73d8f575e1a74a3d9102d2392ed32a68eb1`  
		Last Modified: Thu, 04 Jan 2024 19:59:25 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f0079860f288413d1118249ba44313850a9bba5da957b3ba774de973936ca3`  
		Last Modified: Thu, 04 Jan 2024 19:59:25 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
