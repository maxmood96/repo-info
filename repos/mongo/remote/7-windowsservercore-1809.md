## `mongo:7-windowsservercore-1809`

```console
$ docker pull mongo@sha256:9f1b4a01745b69c938acc941c5356c14dc94bb700df75f7834e679afdf942c1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5206; amd64

### `mongo:7-windowsservercore-1809` - windows version 10.0.17763.5206; amd64

```console
$ docker pull mongo@sha256:2d40afb90d17b3848063bfe1b5208d0c6361e0beb787d7c52c585d7879ca2c73
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2672614843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b83ce9f87aba8f057f636cf051c8b0d227ab6f3522a5d9a5912fd9358b18214`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Tue, 09 Jan 2024 00:54:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Jan 2024 00:54:11 GMT
ENV MONGO_VERSION=7.0.5
# Tue, 09 Jan 2024 00:54:12 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.5-signed.msi
# Tue, 09 Jan 2024 00:54:13 GMT
ENV MONGO_DOWNLOAD_SHA256=96441addde451b9d81dfaa10aca9678ada35d17d02a9a07481c6137d3df55e2b
# Tue, 09 Jan 2024 00:57:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 09 Jan 2024 00:57:38 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 09 Jan 2024 00:57:39 GMT
EXPOSE 27017
# Tue, 09 Jan 2024 00:57:40 GMT
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
	-	`sha256:a421642312d96e45fe9bc10bb32446fe94cbab7c3c5acf883e9d842f9aa8fa5d`  
		Last Modified: Tue, 09 Jan 2024 00:57:46 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5676dbb955451a4b3a31d423086d6e07d46b953bf7a1c5ee8f22ac6e366c49f2`  
		Last Modified: Tue, 09 Jan 2024 00:57:46 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d65ec156309c6418689d33cb41c514b2f51fdbc6a137b274e1249ef4ca3a4ec`  
		Last Modified: Tue, 09 Jan 2024 00:57:46 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea637db99ef736272b9d26f8b626df21473564a6e5ba531fdc61576192011e8f`  
		Last Modified: Tue, 09 Jan 2024 00:57:45 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8569d6b6a66b1c05121655d68ab745d1314c7d5689afc6b97ae2344f8220a7a5`  
		Last Modified: Tue, 09 Jan 2024 00:58:32 GMT  
		Size: 612.9 MB (612896766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afb741b97f6d04437a428628dfd02463edcb418f8d8218170d4d67ce822528f`  
		Last Modified: Tue, 09 Jan 2024 00:57:44 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6ab4c629309211176c678bfa6219fd1049eba0e3efe4b7ef7a267c85ff76c2`  
		Last Modified: Tue, 09 Jan 2024 00:57:45 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f114970c712afd3dbb31b0a14458340c59abd53d4418b429daf6f09a7b918d`  
		Last Modified: Tue, 09 Jan 2024 00:57:44 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
