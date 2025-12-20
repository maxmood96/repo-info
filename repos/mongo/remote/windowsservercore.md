## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:3eda210a39b18ea7e86acdbb19eb32d39ace7ef09055413aafc553ee5a379ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `mongo:windowsservercore` - windows version 10.0.26100.7462; amd64

```console
$ docker pull mongo@sha256:b3d8db113bcc8c83f11bdea50f1c4decbfaacad651a6ee20bd13cc78f5702162
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 GB (4068430407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878ebeea3c8642dc2396ba43e1a4e21836f5b0d9406a39efa765f2e072151d61`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Fri, 19 Dec 2025 18:57:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 19 Dec 2025 18:57:29 GMT
ENV MONGO_VERSION=8.2.3
# Fri, 19 Dec 2025 18:57:29 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.3-signed.msi
# Fri, 19 Dec 2025 18:57:30 GMT
ENV MONGO_DOWNLOAD_SHA256=dbad91532fd5f5bb5b42818ce7a644dd603a388926303b306e23ef29a640e849
# Fri, 19 Dec 2025 19:00:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 19 Dec 2025 19:00:12 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 19 Dec 2025 19:00:12 GMT
EXPOSE 27017
# Fri, 19 Dec 2025 19:00:13 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e2689c4421ccfad4aaaa0fb2f657a994702ff1dae1abfd08e2ba16cbd69ccd`  
		Last Modified: Fri, 19 Dec 2025 19:13:21 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1a58d85723c0ffe6b3fd7147dc87bdb505223f596206f7fcb1ad95b11e92d8`  
		Last Modified: Fri, 19 Dec 2025 19:13:21 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560cf7eb2e69a085774c3b505b9710a65cb25ed326589256531b15b80e767485`  
		Last Modified: Fri, 19 Dec 2025 19:13:21 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac307f575d00b10de59235d9b1bf58e0ba794390a8ee86cea2592d25a2b1c20a`  
		Last Modified: Fri, 19 Dec 2025 19:13:21 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22149fda106fdafc717f8fba2c557210fbea2e121810cc07b728190df2615ed`  
		Last Modified: Fri, 19 Dec 2025 19:15:27 GMT  
		Size: 815.3 MB (815300775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f22ddf844beff3b2ab406d83c1a93403b5cb87878d0b64140b8392f5910a652`  
		Last Modified: Fri, 19 Dec 2025 19:13:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4cb09a4853e4311d530f446706e28809474007e6dbded7fbdc74644a15887c`  
		Last Modified: Fri, 19 Dec 2025 19:13:21 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb5e7aec4f3b78eada1a85e8d7d0c3c80d85a13155ca62c3819af68a6f0c6de`  
		Last Modified: Fri, 19 Dec 2025 19:13:21 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:windowsservercore` - windows version 10.0.20348.4529; amd64

```console
$ docker pull mongo@sha256:37d7e7765629c560cf5c2a0a9edde1539befbd2170e61262d9ac8bb0feb0594f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2595306935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5058fa9e20fe992e5c6962844b8833c5b26abc606d170cd6fd01e99b705ddd5f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Fri, 19 Dec 2025 18:56:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 19 Dec 2025 18:56:33 GMT
ENV MONGO_VERSION=8.2.3
# Fri, 19 Dec 2025 18:56:34 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.3-signed.msi
# Fri, 19 Dec 2025 18:56:35 GMT
ENV MONGO_DOWNLOAD_SHA256=dbad91532fd5f5bb5b42818ce7a644dd603a388926303b306e23ef29a640e849
# Fri, 19 Dec 2025 19:02:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 19 Dec 2025 19:02:53 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 19 Dec 2025 19:02:54 GMT
EXPOSE 27017
# Fri, 19 Dec 2025 19:02:54 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdee0875f00689056b27d4f960b96394d14df8ba637ca7b976b9242bf8629e1c`  
		Last Modified: Fri, 19 Dec 2025 19:11:29 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304f364b2e547815b2614b43368652979437daba5e2fb3974699825661415817`  
		Last Modified: Fri, 19 Dec 2025 19:11:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f012aeaa4248e718b744dc415b6eb416d1a575944171c0a1853ff4e45138b0e2`  
		Last Modified: Fri, 19 Dec 2025 19:11:29 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac7ba93c72d0fb8c4540eb2583ea436c648ce7c6182955960197a5b9fab00e6`  
		Last Modified: Fri, 19 Dec 2025 19:11:29 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a5575209bb9aa44b199cbdd921aeb2ad0727b35ccd4d0fb29534adf2db0ef8`  
		Last Modified: Fri, 19 Dec 2025 19:11:38 GMT  
		Size: 815.4 MB (815418599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc258206738985f7dacebda8f04dcf62cae38371d516dff46c8ef2e90809ba88`  
		Last Modified: Fri, 19 Dec 2025 19:11:29 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1b523be68eb1c08701c5c4ab189e00f4725552b61410e609e1e65a46bf1fdd`  
		Last Modified: Fri, 19 Dec 2025 19:11:29 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb2547f256153dec13e55bf1115129c773e70ba978bcf72528cd9affe10fbed`  
		Last Modified: Fri, 19 Dec 2025 19:11:29 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
