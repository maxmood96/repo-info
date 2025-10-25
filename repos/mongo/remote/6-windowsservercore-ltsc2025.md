## `mongo:6-windowsservercore-ltsc2025`

```console
$ docker pull mongo@sha256:c56cc3a267bfe991426a4ccebc6f9e7bd4129cf490fffaf27f2e8e5e169dfcaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `mongo:6-windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull mongo@sha256:aa6058f6e188abfd3d55778a2048568983a9604d9fd1cecee29fd9f83744a461
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3747379199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a880ee44a48d7b805fbbc3085918d2c2e3a71f4a6c6bf33fa640a23b43bb17e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 24 Oct 2025 18:24:48 GMT
ENV MONGO_VERSION=6.0.26
# Fri, 24 Oct 2025 18:24:49 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.26-signed.msi
# Fri, 24 Oct 2025 18:24:50 GMT
ENV MONGO_DOWNLOAD_SHA256=b32578a8d982810c6a9a0b2f962bd45053701d97415f901030b796ec93dea75a
# Fri, 24 Oct 2025 18:26:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 24 Oct 2025 18:26:22 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 24 Oct 2025 18:26:23 GMT
EXPOSE 27017
# Fri, 24 Oct 2025 18:26:23 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28fc55a62bc5ce80a72a387a0f00371aaa400898ee85680d6a902d16d067ec41`  
		Last Modified: Fri, 24 Oct 2025 18:27:31 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a213291317e87a12a34efe8151a6e2308db9f61df40b26abde19183473157e`  
		Last Modified: Fri, 24 Oct 2025 18:27:31 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff107be2eb1f4fdb3373e6284c2823bf8d3b1bb9df9f96642ee4b2d1d70edf81`  
		Last Modified: Fri, 24 Oct 2025 18:27:31 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b593922960afb5996e2bd3cf551ec17db7e8f667a74da69b061dbcc41a95a2`  
		Last Modified: Fri, 24 Oct 2025 18:27:31 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78e3eb3159c9348e58ce7551866e41f4c2a648fc9179f5ba5d2139a2bc27aa3`  
		Last Modified: Fri, 24 Oct 2025 22:08:13 GMT  
		Size: 527.0 MB (527022961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a7b3b79755d99dbf5066ed296fcdc4c90589c240fb6592ce5334012b6bf855`  
		Last Modified: Fri, 24 Oct 2025 18:27:31 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854a8e1bd6b152efe999661ad43f645d8508849a609b44d737613ccccd5c7e78`  
		Last Modified: Fri, 24 Oct 2025 18:27:31 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab552171df0d8dfc7030b2ca91e29088f90930058dd7de818cdf732301cf73b3`  
		Last Modified: Fri, 24 Oct 2025 18:27:31 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
