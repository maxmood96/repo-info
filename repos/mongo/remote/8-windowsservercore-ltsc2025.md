## `mongo:8-windowsservercore-ltsc2025`

```console
$ docker pull mongo@sha256:b2ef0faf3aa47ec6cd809dffd60713dbe205329fd182a1739652efb2c0075b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `mongo:8-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull mongo@sha256:170c20dd31da2ca1500fa43a2a74b35e69622969707f6c715907b3a1694190cb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2311327496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c17c13fe5ec3fd6ae1d8af677bf51c2e760ff334440ca5712d2e12a56bdec7c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 10 Feb 2026 20:08:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Feb 2026 20:08:02 GMT
ENV MONGO_VERSION=8.2.5
# Tue, 10 Feb 2026 20:08:03 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.5-signed.msi
# Tue, 10 Feb 2026 20:08:04 GMT
ENV MONGO_DOWNLOAD_SHA256=02d42062a64b88b68b385dbd723fc2110ef2d43a83642324d94f2f2a6268befb
# Tue, 10 Feb 2026 20:11:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 10 Feb 2026 20:11:01 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 10 Feb 2026 20:11:02 GMT
EXPOSE 27017
# Tue, 10 Feb 2026 20:11:03 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a5aa8e1fa5bfac31a0104db90a5921227d523903954a1cec1b0751def99fb5`  
		Last Modified: Tue, 10 Feb 2026 20:11:09 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69163faf7e48c29688b0944c7e1f746e5f0058a9289a07017244d2cd9cca3f80`  
		Last Modified: Tue, 10 Feb 2026 20:11:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db06eaf9c846c38f7978021dbde25c2a0ed233878f460c05200c90a4c2698c69`  
		Last Modified: Tue, 10 Feb 2026 20:11:09 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1079daf0f10af02ebd51b79285e91a703ab781503a58ee458645b5c7b127652c`  
		Last Modified: Tue, 10 Feb 2026 20:11:07 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7243f82d7a8018f15862f50ea18d814e4133c36986c0f103437fc23031fe7201`  
		Last Modified: Tue, 10 Feb 2026 20:12:19 GMT  
		Size: 815.6 MB (815558023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404b04dce76f2cc2f2a0eb01976bde1cee8b0c123638067551788ebdf334dafb`  
		Last Modified: Tue, 10 Feb 2026 20:11:07 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8f89c6f82137af6cf42b3ffdc7b7929246605574f5afa22ea57fd5f03d9d1f`  
		Last Modified: Tue, 10 Feb 2026 20:11:07 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7bfa7240b3acb6d1e1ce50e1136075cd480c5fba0f01d64ab9cfd27200e02c`  
		Last Modified: Tue, 10 Feb 2026 20:11:07 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
