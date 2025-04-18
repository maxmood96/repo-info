## `mongo:windowsservercore-ltsc2025`

```console
$ docker pull mongo@sha256:258851636d3617f16df3f5e0ef3bce14894baa980a59443c7ea33699c132a7cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `mongo:windowsservercore-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull mongo@sha256:ff06eb44cf6a11f6a5e6f5add2283480aa9e6d0274d4f4167a5caf8a63765dd9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 GB (4165469554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b03eb4a4de5001e6e4a956170cb68b7638a513357e6abc05d56c3c8777ba1e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Fri, 18 Apr 2025 03:15:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 18 Apr 2025 03:15:40 GMT
ENV MONGO_VERSION=8.0.8
# Fri, 18 Apr 2025 03:15:41 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.8-signed.msi
# Fri, 18 Apr 2025 03:15:42 GMT
ENV MONGO_DOWNLOAD_SHA256=4bf700912876c337697fa02bf4c38db0baed89604033b138e5e27d4e3eb743ee
# Fri, 18 Apr 2025 03:17:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:17:19 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 18 Apr 2025 03:17:19 GMT
EXPOSE 27017
# Fri, 18 Apr 2025 03:17:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ba2336fb9edc233889dd58d0a99ab12f5b5acf04de49d7ee3aa450cd7e8cec`  
		Last Modified: Fri, 18 Apr 2025 03:17:24 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553011d5ffaa7f6953c13c78daad8464ae82332eb12dbb6b9bce5056eecaa344`  
		Last Modified: Fri, 18 Apr 2025 03:17:24 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2791125331c75ddd43318abfeda2e1792876441b4620a1e72da55488046eb47c`  
		Last Modified: Fri, 18 Apr 2025 03:17:24 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d846f19fea476a630d970cf569774e963b960da6688019fc9dcda8d8e855db7`  
		Last Modified: Fri, 18 Apr 2025 03:17:23 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16dfbf7e9002fe593df2c6e3aa07cca48072d6148c871610746cd4646a6435a5`  
		Last Modified: Fri, 18 Apr 2025 03:18:36 GMT  
		Size: 770.3 MB (770298942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f15d00179ee682aea38643c863135d9c46d1fe4c78c3c171d3edf2e97a4ff57`  
		Last Modified: Fri, 18 Apr 2025 03:17:23 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ebc27c8de7fcbfa381ec8a19ec0a5981ea01c4eab3a38dcf9eb578366ada8af`  
		Last Modified: Fri, 18 Apr 2025 03:17:23 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102bc816db28bb4d9308aff47e5d34d11943265a480eaa0b1c76caec0fc77019`  
		Last Modified: Fri, 18 Apr 2025 03:17:23 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
