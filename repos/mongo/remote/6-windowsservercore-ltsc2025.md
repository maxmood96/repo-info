## `mongo:6-windowsservercore-ltsc2025`

```console
$ docker pull mongo@sha256:783e868edaae207760c6109a927d6378384ed1b19728793bf0d806b2104bed7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `mongo:6-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull mongo@sha256:5e7aec8c1b9e7c884f8e11fdfb12a5dcffa9db25b503c1a1eda3d67838b2e00c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2733458158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a8eb6ef51b46a5fed4381cbf9b0fda36eb0ae0df2a6bd91fc5c3feb58aa536`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Fri, 15 May 2026 16:50:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 15 May 2026 16:50:19 GMT
ENV MONGO_VERSION=6.0.28
# Fri, 15 May 2026 16:50:20 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.28-signed.msi
# Fri, 15 May 2026 16:50:21 GMT
ENV MONGO_DOWNLOAD_SHA256=49e24243affae70b9c80112d0552d14454f5db1219ed2f50abd02d9a81ce95f8
# Fri, 15 May 2026 16:53:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 15 May 2026 16:53:12 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 15 May 2026 16:53:13 GMT
EXPOSE 27017
# Fri, 15 May 2026 16:53:14 GMT
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
	-	`sha256:15fae92dfb55ac262de9960fc92689b61a6654c6adc652ca004e8f242a4ee3b6`  
		Last Modified: Fri, 15 May 2026 16:53:23 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1fa37648df37bbf3a5d4794b5bf8c421c47c4e5b7c83a711028a6d812d6d53`  
		Last Modified: Fri, 15 May 2026 16:53:23 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb99d0b314c6cec9051b7f3f4cab3d73bc22b0d36464ae34a5317db7daba3cec`  
		Last Modified: Fri, 15 May 2026 16:53:23 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac4495b95444b30911c89b524f1e020d88c77138bccb1383a84a9ec024271d4`  
		Last Modified: Fri, 15 May 2026 16:53:22 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f327d3f0c2cc41af422384c71a6c38e7343c0d8f3d741696c81cea21821b43`  
		Last Modified: Fri, 15 May 2026 16:54:15 GMT  
		Size: 527.5 MB (527507329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75ce3852287966b42a2eb08e28e291cadfaee024fbaf86894f95ed7daafa351`  
		Last Modified: Fri, 15 May 2026 16:53:22 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be1010fd83a06d0ab0bded0dcfeaa9624390ebf226c2e25ea940cff1f2a00889`  
		Last Modified: Fri, 15 May 2026 16:53:22 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61253fc6a9ae1474dd7ca703fe6951e8892b3ac9a6d70f6cf978cf6e4424a3b`  
		Last Modified: Fri, 15 May 2026 16:53:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
