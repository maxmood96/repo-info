## `mongo:7-windowsservercore`

```console
$ docker pull mongo@sha256:a50b1a4bce88163e39b7f4071f4fc4742d380b842c45368d8c6d0665a894beb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `mongo:7-windowsservercore` - windows version 10.0.20348.2655; amd64

```console
$ docker pull mongo@sha256:09f7458917dfa6cb05f39ad6630fb8a1c7c9f3e1a8d3bd400e629db35adf9266
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2750562909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312a825e0fc0adc403a982ef1763ccc2fec51df69d2a46179ca61d180cdac5c3`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Tue, 13 Aug 2024 20:15:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 13 Aug 2024 20:15:02 GMT
ENV MONGO_VERSION=7.0.12
# Tue, 13 Aug 2024 20:15:03 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.12-signed.msi
# Tue, 13 Aug 2024 20:15:04 GMT
ENV MONGO_DOWNLOAD_SHA256=314f1b988490d46c9831cbf7ad7669a949507df17cc0674f7bdac47de74281b1
# Tue, 13 Aug 2024 20:16:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 13 Aug 2024 20:16:23 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 13 Aug 2024 20:16:24 GMT
EXPOSE 27017
# Tue, 13 Aug 2024 20:16:25 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304371999569501d22285076d583445ae9a71dbc9bbc8794422c2172c0f4c730`  
		Last Modified: Tue, 13 Aug 2024 20:16:28 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef456b8e36791a63aebfd02aa1457364b236b1e2d2ee28217313ef896cfe0fd`  
		Last Modified: Tue, 13 Aug 2024 20:16:28 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a1faaf446fba34c83978864b5b7d75a38c16fbfdd6843bb2b84eabdd57c842`  
		Last Modified: Tue, 13 Aug 2024 20:16:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a13aa819105bd796037c014ef879e4bcd9dd5c8d3824b8a2250c14dc5818a2`  
		Last Modified: Tue, 13 Aug 2024 20:16:27 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffee34de017a49064632da5d7e1030bfc31a5105652f49a2ee08474a7f5960f`  
		Last Modified: Tue, 13 Aug 2024 20:17:19 GMT  
		Size: 608.8 MB (608788900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ddbae91ab071def197c99a0c9b02d0b1e796e34cc04132d24c6d91d8b7cd3c0`  
		Last Modified: Tue, 13 Aug 2024 20:16:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42165731c8550589c978e9d836425f3d687ae47963aa87ce4541efa9d5d993b0`  
		Last Modified: Tue, 13 Aug 2024 20:16:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4299b8be79063f08fb975a723b9b4ec3315a2ea1ccd398081fbf8462cb5c816e`  
		Last Modified: Tue, 13 Aug 2024 20:16:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-windowsservercore` - windows version 10.0.17763.6189; amd64

```console
$ docker pull mongo@sha256:fc96eee784925b76ce9af670d74128c8ccff576ee3a3d27b9a64aa42c95e6c98
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2854123657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f451edc685259979df504d45c5b187af7161679a1db62ae1443dd069b198468`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 13 Aug 2024 20:16:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 13 Aug 2024 20:16:09 GMT
ENV MONGO_VERSION=7.0.12
# Tue, 13 Aug 2024 20:16:10 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.12-signed.msi
# Tue, 13 Aug 2024 20:16:10 GMT
ENV MONGO_DOWNLOAD_SHA256=314f1b988490d46c9831cbf7ad7669a949507df17cc0674f7bdac47de74281b1
# Tue, 13 Aug 2024 20:18:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 13 Aug 2024 20:18:13 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 13 Aug 2024 20:18:14 GMT
EXPOSE 27017
# Tue, 13 Aug 2024 20:18:15 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5fad384d45d89607211110ce60951115ac0f9fa8c606bffead989f6ecb382f`  
		Last Modified: Tue, 13 Aug 2024 20:18:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329a398fe85cf030807bf41b6720420793c696816ff23d58b45e5dc94e047664`  
		Last Modified: Tue, 13 Aug 2024 20:18:19 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ad1c05d571d3c52fbc4399b2bc09aeff40e8e66d6b73df1ab1f8b32a43bfa3`  
		Last Modified: Tue, 13 Aug 2024 20:18:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb14bd68fa1091de79c25fd53310d1a26b9af0620acaf272acab1545d098080f`  
		Last Modified: Tue, 13 Aug 2024 20:18:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f62e7b296004c7b66b7189017ec56ce147da7cf67c97b1abccbde13d38bb13`  
		Last Modified: Tue, 13 Aug 2024 20:19:08 GMT  
		Size: 608.9 MB (608911360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203cecf2f6ff03f104829de0b7eb36097193eb3d346f139226f6200e0138645d`  
		Last Modified: Tue, 13 Aug 2024 20:18:17 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e3863f3b50c73c620154f9e2c45a0940958ed3683e41aa3e8599bbc347b53b`  
		Last Modified: Tue, 13 Aug 2024 20:18:18 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda7a1fc8e14d4dde60bbece6f2c67d59cd77234a64f8fe82cb876f222e181fe`  
		Last Modified: Tue, 13 Aug 2024 20:18:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
