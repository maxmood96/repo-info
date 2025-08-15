## `mongo:7-windowsservercore-ltsc2025`

```console
$ docker pull mongo@sha256:19564c5d621e3643fc1815250b1b9528a4e1b4d6f945429b5ca8e810f06f49c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `mongo:7-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull mongo@sha256:68fde503f903b69119f3587757eabb1e4769377ba6fb7a63fa24c6de583b3ec7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 GB (4116634191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9ae4efd9358797b830820bbb9b316c9d45e9d75b9968a4e2c792c7cb33caf70`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Thu, 14 Aug 2025 22:52:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 14 Aug 2025 22:52:46 GMT
ENV MONGO_VERSION=7.0.23
# Thu, 14 Aug 2025 22:52:47 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.23-signed.msi
# Thu, 14 Aug 2025 22:52:47 GMT
ENV MONGO_DOWNLOAD_SHA256=930756f059e218a427192156655066a1c900b9493d7c107077ed89aca6fc950a
# Thu, 14 Aug 2025 22:53:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 14 Aug 2025 22:53:37 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 14 Aug 2025 22:53:37 GMT
EXPOSE 27017
# Thu, 14 Aug 2025 22:53:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f8f31e83a1926c85618d38ed20456531ccfce73fb4b76ef501e624b888cd44`  
		Last Modified: Thu, 14 Aug 2025 22:57:27 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa867156522169e6bafa069270a9889a67a17c1709aeb24afd4b015971262c0b`  
		Last Modified: Thu, 14 Aug 2025 22:57:27 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2643116bd2ed312183c30fc98b9d65bafe6f00989f2d3cc44d9e37166bb176`  
		Last Modified: Thu, 14 Aug 2025 22:57:27 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de2b8d2a2bb176b155aab51ee1178c875101c38150711c2b69a3ea90b6ce915`  
		Last Modified: Thu, 14 Aug 2025 22:57:27 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34dc3c7a06def8fddf5ae4b46e7a81c8b14d77574aea1e908048080610a413fa`  
		Last Modified: Fri, 15 Aug 2025 01:08:36 GMT  
		Size: 617.8 MB (617794429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a27ba27034dc7e127a8f94b360b8b48949427826b3fcf4aa5153db8b24b91a1`  
		Last Modified: Thu, 14 Aug 2025 22:57:27 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b86c82b3c71bae63a9f0fb63bb7cbe781afa8477182038039b361befdc9b50`  
		Last Modified: Thu, 14 Aug 2025 22:57:27 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291e7f5f3d4ad2914ef11190a36df77b8c9956ac14e23e096b6fdcf56f71a6ce`  
		Last Modified: Thu, 14 Aug 2025 22:57:27 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
