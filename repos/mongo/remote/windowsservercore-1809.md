## `mongo:windowsservercore-1809`

```console
$ docker pull mongo@sha256:d12c4c27ba30793d57d80a8a100c015229bcc6fb597723d3b4170039f997fa46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `mongo:windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull mongo@sha256:18b25a0b2737a702df9c4112167345770ff79291df0decdc578d3baa783394a0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2669586613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55f492a889de5738c121710bb16328d5273c3e15bdd98eda2507d255adfbf493`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 03:20:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 29 Nov 2023 01:18:39 GMT
ENV MONGO_VERSION=7.0.4
# Wed, 29 Nov 2023 01:18:40 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.4-signed.msi
# Wed, 29 Nov 2023 01:18:40 GMT
ENV MONGO_DOWNLOAD_SHA256=86a9ce6ce62c9b6a3fee8739572419b59040fa25c7e07a4d1ce28894670e2a2b
# Wed, 29 Nov 2023 01:22:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 29 Nov 2023 01:22:32 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 29 Nov 2023 01:22:33 GMT
EXPOSE 27017
# Wed, 29 Nov 2023 01:22:34 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e4111e1324ff2110def2382c3796071edd92a76a262efa6c0657d549b64496`  
		Last Modified: Thu, 16 Nov 2023 04:21:07 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4978ca8262cbdc8e63abcfaed0f23a7c4df7aef868a4c332e0ccfacdfacff370`  
		Last Modified: Wed, 29 Nov 2023 01:49:49 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40efc97f2b231e5ddf8e46d8ed14a06888d92bd043aa477b600f81aacab9e8f`  
		Last Modified: Wed, 29 Nov 2023 01:49:49 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48540d9bc0e8b12c96e43c0dfa0978acffee2b5e1b122d39f7e0a29d6ea610d`  
		Last Modified: Wed, 29 Nov 2023 01:49:47 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d4139522aaf0ec8fb16a5dcfd93e12fcd1db95cb08b1630b167e6cdb94ee19`  
		Last Modified: Wed, 29 Nov 2023 01:51:21 GMT  
		Size: 612.1 MB (612145151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146a588d30b5e8f2d9371800460372793871abec7fbbbd7f2ce971cafe1f262a`  
		Last Modified: Wed, 29 Nov 2023 01:49:47 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8805d648cb16861f3c1ffcbab0617f563c3940b2eee35baf10fe832726e68b1e`  
		Last Modified: Wed, 29 Nov 2023 01:49:47 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66b7fff7824061ffe85d175aeb63bec161a489b4eadf0a0f40f77dd813336b2`  
		Last Modified: Wed, 29 Nov 2023 01:49:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
