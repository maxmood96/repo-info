## `mongo:7-windowsservercore-ltsc2025`

```console
$ docker pull mongo@sha256:03a7e39852ecef96a15feda7ad50ae28bef35674ab64af7944166039c5cf5c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `mongo:7-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull mongo@sha256:c30bf4495468147e7df0216e7b91847263154fe47df45bf3a872aa95f48b6f04
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2829821094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d19e13a67300f1467efb84b003315adb965582e9776d5a07c0730ba9b27a187`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:49:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 May 2026 23:49:35 GMT
ENV MONGO_VERSION=7.0.32
# Tue, 12 May 2026 23:49:35 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.32-signed.msi
# Tue, 12 May 2026 23:49:36 GMT
ENV MONGO_DOWNLOAD_SHA256=02bb67e1e490b4dc587d853b7ce30197f798c15faba5d48aadf4891bba695072
# Tue, 12 May 2026 23:51:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 12 May 2026 23:51:13 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 12 May 2026 23:51:13 GMT
EXPOSE 27017
# Tue, 12 May 2026 23:51:13 GMT
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
	-	`sha256:870809b3667e48a5c90ea691f7b9e892cbbe376cd6e3d0b94496b331dd20d1e5`  
		Last Modified: Tue, 12 May 2026 23:51:30 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c09cf714890d7fe28abf4aa990a1551cdb400e3ed1cd7ea5d369d9e116d149`  
		Last Modified: Tue, 12 May 2026 23:51:30 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe55590eef2ca0d5fb41f75096f5bc098e9167c7161786a08b28e6a5fde160a`  
		Last Modified: Tue, 12 May 2026 23:51:30 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02db701e796ffd51716b27750941205dbcab19c2d1f513aed712915cb74e3d79`  
		Last Modified: Tue, 12 May 2026 23:51:28 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6315a3b263291e129b270c04db1cd056064a73ef36a1d4b322ecfbac5ba8f48`  
		Last Modified: Tue, 12 May 2026 23:52:23 GMT  
		Size: 623.9 MB (623869871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede369bb2e32a21af388a904e6fcac612b7eb52829d8412393411fcd3a8cca98`  
		Last Modified: Tue, 12 May 2026 23:51:28 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88969b528e29afb72b7ed0ffd011bebc6b7c963f4b00eef15784dd6cde5b450`  
		Last Modified: Tue, 12 May 2026 23:51:28 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5259214b4df66b8276195da53348a688fea645e265e34b7aa0c3139338f52a`  
		Last Modified: Tue, 12 May 2026 23:51:28 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
