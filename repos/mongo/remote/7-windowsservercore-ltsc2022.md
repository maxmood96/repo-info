## `mongo:7-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:6282e7b02e84e7dd777bebae25494c97d90b1b1585ba15becfb4eb88cf0b98f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `mongo:7-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull mongo@sha256:0a06636db63392a31809908bdd03bc03125fc2dc5bcd973c406d0de085138dad
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2897905001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034c958d7fbbf5bfadcd92cafed7ea70ea17ccca19cdcecda08989d3843e031c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:31:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 Aug 2025 20:31:52 GMT
ENV MONGO_VERSION=7.0.22
# Tue, 12 Aug 2025 20:31:52 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.22-signed.msi
# Tue, 12 Aug 2025 20:31:53 GMT
ENV MONGO_DOWNLOAD_SHA256=c3b3cab89a024970ee1971c6ead4ede2c5e8be2e302616f5aa45e409cba30167
# Tue, 12 Aug 2025 20:32:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:32:42 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 12 Aug 2025 20:32:43 GMT
EXPOSE 27017
# Tue, 12 Aug 2025 20:32:44 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483fd4a728beb05662fad6527a0107e16afd9eca8b65f16a6758f073fcf0a41f`  
		Last Modified: Tue, 12 Aug 2025 20:45:27 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5ff4141bc1914934701c7e26d43a8b4d94d388db7053896e5c3b21719a2c12`  
		Last Modified: Tue, 12 Aug 2025 20:45:27 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fca31b18ee8383379d89718174046bc82c52f3615f92c385ebdab212cfa3818`  
		Last Modified: Tue, 12 Aug 2025 20:45:28 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7c3b0bdd219e3937302e4c75e4250798611eaaee8373e1deaf69d48ac9a1ef`  
		Last Modified: Tue, 12 Aug 2025 20:45:28 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe08a16c371927c2187b30624d89f81384533f6fa02735b324a95b243909b4e`  
		Last Modified: Tue, 12 Aug 2025 20:46:03 GMT  
		Size: 616.2 MB (616204035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c7c978453ff187f812cd98f0f52472dd55aba9b3640a74044a48c27af44655`  
		Last Modified: Tue, 12 Aug 2025 20:45:30 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502a80809d2830faae025f434fc47bc99323d7e96019deec6597c8b121746b26`  
		Last Modified: Tue, 12 Aug 2025 20:45:31 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e7da68920b15a85de3538d07068b44a2dcecb9610657d90c640d500060a1bf`  
		Last Modified: Tue, 12 Aug 2025 20:45:33 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
