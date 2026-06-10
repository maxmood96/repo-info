## `mongo:windowsservercore-ltsc2025`

```console
$ docker pull mongo@sha256:5d03b47682db71ae758e31227226c49af3fbb0f277a2a367a2ffa25c7be5fb86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `mongo:windowsservercore-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull mongo@sha256:86718051c7e0baca05081fbbd7b5c4acfe9a6ec0cf5e5f7b5e1d85318b6393cd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3096538757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c49a43a4caea531a5451c2e556f9e159f2ffdd0a6fe915df1e30ddad04428033`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Tue, 09 Jun 2026 22:23:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Jun 2026 22:23:21 GMT
ENV MONGO_VERSION=8.2.9
# Tue, 09 Jun 2026 22:23:21 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.9-signed.msi
# Tue, 09 Jun 2026 22:23:22 GMT
ENV MONGO_DOWNLOAD_SHA256=a23b5865415ab2d507823e64163e5f3b09a4118bd8ede539938673137faab690
# Tue, 09 Jun 2026 22:25:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:25:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 09 Jun 2026 22:25:16 GMT
EXPOSE 27017
# Tue, 09 Jun 2026 22:25:17 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc873abe7a2ef03fddddafc75c76f7b370d017c4e0de3b1f22e62f199af56cf`  
		Last Modified: Tue, 09 Jun 2026 22:25:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f688ed439107b0c087a79424e831cfb8ce55d0f7c85366b99bebe643a0f621`  
		Last Modified: Tue, 09 Jun 2026 22:25:32 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1190f55c90da53c2001a91ff8c71d6da31922a6b4fe572f77624585202ee2bfb`  
		Last Modified: Tue, 09 Jun 2026 22:25:32 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6a84726b4c49621f9c3cff8097af64c72499005bb23cc8cc25b33cbef88b7f`  
		Last Modified: Tue, 09 Jun 2026 22:25:30 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fcda3dcd63bb45d28276d3d417ff58078e405fc0022f635733d0e0b2c26007`  
		Last Modified: Tue, 09 Jun 2026 22:26:48 GMT  
		Size: 817.4 MB (817386799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62634aa040c81bda1896fd4f6f5dfe2b938cb75f47c1004ee60daceb3011f0e`  
		Last Modified: Tue, 09 Jun 2026 22:25:30 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2167b93b43714f8a9969bc8bed44545c95c0b69545452ab9383bf69db03b80d`  
		Last Modified: Tue, 09 Jun 2026 22:25:30 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f84a6374887edc318e552ae4d099f3c1ccfc9edefa4c21366b529b847e9fc9bc`  
		Last Modified: Tue, 09 Jun 2026 22:25:30 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
