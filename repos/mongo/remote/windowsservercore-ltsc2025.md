## `mongo:windowsservercore-ltsc2025`

```console
$ docker pull mongo@sha256:25737e6a842c643194154025ee99807516bd1b15a2f2e12fb0b54dea78e83941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `mongo:windowsservercore-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull mongo@sha256:00f8f358ef314ce2be6e32928c6554bc54a8ec4dbd893a50a118b4ef894bb8b3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 GB (4168665778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f16d10c0d1b205b99a5a55702806d21618f0fe8162261962f95abe15c01f41`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Thu, 01 May 2025 22:34:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 01 May 2025 22:34:03 GMT
ENV MONGO_VERSION=8.0.9
# Thu, 01 May 2025 22:34:04 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.9-signed.msi
# Thu, 01 May 2025 22:34:07 GMT
ENV MONGO_DOWNLOAD_SHA256=4acf24592a7658cc58b4293cbf0a3f42133c9c1d4f2234f1a249f74aa1c7d22a
# Thu, 01 May 2025 22:35:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 01 May 2025 22:35:43 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 01 May 2025 22:35:44 GMT
EXPOSE 27017
# Thu, 01 May 2025 22:35:45 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Thu, 08 May 2025 17:36:06 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cccd48a0c5377d8718cc8996cd030fd9c44f81f01d9504598f5ee454927c2cd8`  
		Last Modified: Thu, 08 May 2025 17:20:11 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a826a7710cded399ef84aab5bb14bc01889de49303b80d7071bbe9aba000896`  
		Last Modified: Thu, 08 May 2025 17:20:11 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a925c6773379e2dae97ed38f536d853c3a23162201fa809806cbfddd3620d4b0`  
		Last Modified: Thu, 08 May 2025 17:20:11 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8fff0c45fe72daf506ad5856321d9be8b230b23eb061168f1020fd1b51f35a`  
		Last Modified: Thu, 08 May 2025 17:20:12 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94408351b87f6142e2ebd794494d39694722c5c97d1d61ad723ed8e34cb7eaae`  
		Last Modified: Thu, 08 May 2025 17:42:26 GMT  
		Size: 773.5 MB (773495107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bec2fdd4f099de9a2221e4b099fb05296882765309313a8107735d19ef58951`  
		Last Modified: Thu, 08 May 2025 17:20:12 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c42448f181bc1c424769ef68c122d219ca70d9078f5962198ae2e8438605685f`  
		Last Modified: Thu, 08 May 2025 17:20:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7db15666cfcc8ab8d39680f9ee967f342e0f19263efc4d3e1232ab46f73e87a`  
		Last Modified: Thu, 08 May 2025 17:20:13 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
