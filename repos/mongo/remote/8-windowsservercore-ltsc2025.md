## `mongo:8-windowsservercore-ltsc2025`

```console
$ docker pull mongo@sha256:3b7349d4c2b3fcba1692fab501eccbc8b8575bffa139b48cd9ddce6afe13d8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `mongo:8-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull mongo@sha256:4bad175b6628d7d971ba57a39de2ae72cf13f3110957efcc62beb5aae1073955
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3023760798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb526fc5eb113dfbe94ead2baeb2e9cb5acfbe79aace1d07202574b7d82e9f2a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:47:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 May 2026 23:47:36 GMT
ENV MONGO_VERSION=8.2.7
# Tue, 12 May 2026 23:47:36 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.7-signed.msi
# Tue, 12 May 2026 23:47:37 GMT
ENV MONGO_DOWNLOAD_SHA256=6a326fa3ea7f2013ef28247ea4e68faddaeffc5f19cabed1059e23488986379b
# Tue, 12 May 2026 23:49:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 12 May 2026 23:49:29 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 12 May 2026 23:49:30 GMT
EXPOSE 27017
# Tue, 12 May 2026 23:49:30 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3327124ae5f82925d8db4bceee3d364b3dd15ebd6a6497040d42609eba7d5f4`  
		Last Modified: Tue, 12 May 2026 23:49:46 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a527a2ed1d0c7982d0b8f1d278cc768ee1b1dbb296f71fa12fc7f0ccefa91811`  
		Last Modified: Tue, 12 May 2026 23:49:46 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dfa018d44dfd55082f3ea9babf07d03b8a8ad3ff7ee3ab3c8ff10cfa6c7cea7`  
		Last Modified: Tue, 12 May 2026 23:49:46 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32766009d65d1bb9e0dbea69738ac3dccb30ccefc09fd5a2cfa25a5780375511`  
		Last Modified: Tue, 12 May 2026 23:49:44 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb0fc990c1b9eb908a0432956b6e13c1cb6367f0852492853453502eb69fcc3`  
		Last Modified: Tue, 12 May 2026 23:50:59 GMT  
		Size: 817.8 MB (817809660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f630125491498de9874d3787fb6a0b16ca125412dee72beeb6b3db0b15e9f6`  
		Last Modified: Tue, 12 May 2026 23:49:44 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02336520acddf2a5f0ecb3543195c8efa422d80d590b633043b35df83d1914b4`  
		Last Modified: Tue, 12 May 2026 23:49:44 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bfd0ea8210adb2b6cc32bf03454c7af9e4c8b16654545e218eeedbd160bfde0`  
		Last Modified: Tue, 12 May 2026 23:49:44 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
