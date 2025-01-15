## `mongo:6-windowsservercore`

```console
$ docker pull mongo@sha256:c3e51615d5415914c6a5b4238b708bc6a96f508a235c255fc6f1f6203558d68e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `mongo:6-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull mongo@sha256:2daa13bba956f57015de1527d6d5b06406d827d9f82e3aaca46826ccd7348a14
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2789118877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7954e0a852e57c0546cc9ed0668437d866fbf3be815db540e7bb6208d006a8ed`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:37:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Jan 2025 23:37:25 GMT
ENV MONGO_VERSION=6.0.19
# Tue, 14 Jan 2025 23:37:25 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.19-signed.msi
# Tue, 14 Jan 2025 23:37:26 GMT
ENV MONGO_DOWNLOAD_SHA256=2d9f5555d820c1b6a3f3177f0a73a4f9e9b3a7f1275d2aa3122a2ecc3a1b31a2
# Tue, 14 Jan 2025 23:38:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:38:12 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 14 Jan 2025 23:38:16 GMT
EXPOSE 27017
# Tue, 14 Jan 2025 23:38:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c5bcb8e5abc163bcb6c5ea67d4ec02279969779d538d79a774b44473b0298a`  
		Last Modified: Tue, 14 Jan 2025 23:38:25 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936ab1385c4b1477032511a6afcceebd7c3b2ca423ff529f0270a65f88f5bcf3`  
		Last Modified: Tue, 14 Jan 2025 23:38:25 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf008e7ee228745deca03d4909c5762e2bd99c643c1af892b48318f35da77319`  
		Last Modified: Tue, 14 Jan 2025 23:38:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f177ce968f6e7855a5076adb8359dbe8dbf10f4973f6a6b92cf1d2548a88b8c0`  
		Last Modified: Tue, 14 Jan 2025 23:38:23 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef50aea2dbd7bee4d554127f4e611b5305ded53dbe69984bf786d5491a0e4b94`  
		Last Modified: Tue, 14 Jan 2025 23:39:07 GMT  
		Size: 526.7 MB (526724647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9323867771d2375e7cff011bbf7823bdea25b207631e8c11abdc2277ef6f2fa5`  
		Last Modified: Tue, 14 Jan 2025 23:38:23 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c528395fa8adc68e9836939bf6c2bff3e8f5f914ace13ae8138d81db47177e2a`  
		Last Modified: Tue, 14 Jan 2025 23:38:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c053b41ed3e64ca31f693d645ccefa0f943afcb0e436ec68f2e4f2c880a3bffd`  
		Last Modified: Tue, 14 Jan 2025 23:38:23 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull mongo@sha256:5e341ddc8a3472b8a8473b2858ecd11b7597fafe4896af40775dfc1418fe5ea0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2648964557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdbf9fd872b1c7a209b102f3f8afa8ebbc45f2e44d9a90deb33c79325c8ea188`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:38:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Jan 2025 23:38:47 GMT
ENV MONGO_VERSION=6.0.19
# Tue, 14 Jan 2025 23:38:48 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.19-signed.msi
# Tue, 14 Jan 2025 23:38:48 GMT
ENV MONGO_DOWNLOAD_SHA256=2d9f5555d820c1b6a3f3177f0a73a4f9e9b3a7f1275d2aa3122a2ecc3a1b31a2
# Tue, 14 Jan 2025 23:40:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:40:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 14 Jan 2025 23:40:25 GMT
EXPOSE 27017
# Tue, 14 Jan 2025 23:40:26 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9be94f029167381344fd6e2aa7c6031ea427bb0f0be44bd35e5e74c6e051fd1`  
		Last Modified: Tue, 14 Jan 2025 23:40:29 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a076fe47f57bae71da5b3d46296337e2052314c1cfe2d7f4ac7fd45d1e35d08`  
		Last Modified: Tue, 14 Jan 2025 23:40:29 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd270d739d0fa179f7b79e460b4887c0e6aba5dc0a95c9df70574159660d8cd7`  
		Last Modified: Tue, 14 Jan 2025 23:40:29 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cb4c02a02f76cd058f63e066e01fd223bfa4db863ab6b5709cba628dafb016`  
		Last Modified: Tue, 14 Jan 2025 23:40:28 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b1bfe03d0e543b18962c5b252a99475c599cbc27a57c45d41aac070dda4261`  
		Last Modified: Tue, 14 Jan 2025 23:41:12 GMT  
		Size: 526.7 MB (526743267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72202b3ba33384ab641a90e4a3088773ba280f42a89b44082d2250c73f6b201b`  
		Last Modified: Tue, 14 Jan 2025 23:40:28 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d65b7a299e16a787aeb00aa05e80fe7fea969a465129454e949d17fccdc390`  
		Last Modified: Tue, 14 Jan 2025 23:40:28 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f2052b08c8427ad02b8a771c92e280b4803cbcd6c84fbe95c7e639c31188ad`  
		Last Modified: Tue, 14 Jan 2025 23:40:28 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
