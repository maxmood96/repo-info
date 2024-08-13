## `mongo:windowsservercore-1809`

```console
$ docker pull mongo@sha256:d24a504e9bde5f58fa11c51d7696795a3766962038ef7563224fa38eb0ed976a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `mongo:windowsservercore-1809` - windows version 10.0.17763.6189; amd64

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
