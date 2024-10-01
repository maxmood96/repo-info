## `mongo:5-windowsservercore`

```console
$ docker pull mongo@sha256:91f1f27e56c90f40983cdc12e793678a1f091c8b5148c2484f72a952eca3761c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `mongo:5-windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull mongo@sha256:a41ce2b667d95fb5f0f07f21770ff63c91b7a50534b7aff67e06d4878a51b8ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1774704684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a1c2be79d70715b66c09589d08c3120204e5720a3c56fb3ae62f862d4339a1b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Tue, 01 Oct 2024 01:03:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 01 Oct 2024 01:03:00 GMT
ENV MONGO_VERSION=5.0.29
# Tue, 01 Oct 2024 01:03:01 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.29-signed.msi
# Tue, 01 Oct 2024 01:03:02 GMT
ENV MONGO_DOWNLOAD_SHA256=3188d1a49244ce4a6bc4d853a3d79c178a9d0ae5e6613e4f42cf4156e6b25178
# Tue, 01 Oct 2024 01:05:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 01 Oct 2024 01:05:11 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 01 Oct 2024 01:05:12 GMT
EXPOSE 27017
# Tue, 01 Oct 2024 01:05:14 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c9df6ff7cd1d9563a0f6d1006e9d1b6bd978193e11e73333568b380e6ed1b9`  
		Last Modified: Tue, 01 Oct 2024 01:05:19 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e7bea2bd705d9a1c6144634423436c3db651badd1ab9346226eb18552d18067`  
		Last Modified: Tue, 01 Oct 2024 01:05:19 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f4727e4fa60456d79fb74ee0fd45fa913f14a6b8d2aed3b3738ec18525fc3ee`  
		Last Modified: Tue, 01 Oct 2024 01:05:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f48ad21b40c826f88185739189002617427b0e7e85c81ae720d3c2e29aebae`  
		Last Modified: Tue, 01 Oct 2024 01:05:17 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ab2d80804181c69449cf09879ba2143b24b7d07bcbca0385f5c9b5fc7ccb11`  
		Last Modified: Tue, 01 Oct 2024 01:05:46 GMT  
		Size: 312.5 MB (312503238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07e522b1373cb2d3c9d7f5b2c46ff2f20ffdbe820e64a0f183229da1adb8f94`  
		Last Modified: Tue, 01 Oct 2024 01:05:17 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28db4d57549b139cd48d87fe080c670c0b486f7b92076e9a0fd652d8a376791c`  
		Last Modified: Tue, 01 Oct 2024 01:05:17 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a0a6433f90e36c30c96718c12a197ab66fc5105c27545a91282676d1749059`  
		Last Modified: Tue, 01 Oct 2024 01:05:17 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull mongo@sha256:55b9ce8287b392dff0da8e4dcd1bc1ede062c5ec991872c373b03ca0a42669c7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2032781005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ea42073547620617d2da5dc975c76f25900442e619fd4fdfb0004463067080`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 01 Oct 2024 01:50:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 01 Oct 2024 01:50:37 GMT
ENV MONGO_VERSION=5.0.29
# Tue, 01 Oct 2024 01:50:38 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.29-signed.msi
# Tue, 01 Oct 2024 01:50:38 GMT
ENV MONGO_DOWNLOAD_SHA256=3188d1a49244ce4a6bc4d853a3d79c178a9d0ae5e6613e4f42cf4156e6b25178
# Tue, 01 Oct 2024 01:52:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 01 Oct 2024 01:52:40 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 01 Oct 2024 01:52:41 GMT
EXPOSE 27017
# Tue, 01 Oct 2024 01:52:42 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de0802909f612c27aa1c2a921ff285c092ff0315298370b5219575467b76234`  
		Last Modified: Tue, 01 Oct 2024 01:52:47 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8905e420cb470bf27abe5ab72fd27d6741bae31d351b690ea492ffb3227619`  
		Last Modified: Tue, 01 Oct 2024 01:52:47 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27432b530c547fcac7da01d41a6b9737e5000ba0ebe07a5e8d1a308a6e1998ca`  
		Last Modified: Tue, 01 Oct 2024 01:52:47 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f406db03bb98bc46c633541cc0af9988484c7ceaa23554be3e1e9b36cae14746`  
		Last Modified: Tue, 01 Oct 2024 01:52:46 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb30f61184a0d013da7893e61cfa3f4dd5d725a78e1a6ff53ebbc9f3fa07ec4`  
		Last Modified: Tue, 01 Oct 2024 01:53:15 GMT  
		Size: 312.5 MB (312503543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e9544e6c7dfd311487804db08aba7bfb2e3a179a050ba37cbc9f6d239b5855`  
		Last Modified: Tue, 01 Oct 2024 01:52:45 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3200a748a95820826d3ae26d3ca21c3938d96157507dfcf81bf1fd22895c9b8`  
		Last Modified: Tue, 01 Oct 2024 01:52:46 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e69d9e18e35aef18c37f7121a274e23ab701749d55666ec91c7116759b8c1ef`  
		Last Modified: Tue, 01 Oct 2024 01:52:46 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
