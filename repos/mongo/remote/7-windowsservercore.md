## `mongo:7-windowsservercore`

```console
$ docker pull mongo@sha256:4e0e01718b867a3da8bfc2f4e0d14c8106711babe9e66c9b0d691f94cd5ffbd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64

### `mongo:7-windowsservercore` - windows version 10.0.26100.4061; amd64

```console
$ docker pull mongo@sha256:ff30102c03427d39c26cac5a929224ebdeb8522c6800bca9e74859b733eecea2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 GB (4046734577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f7e4ad16c5d36341d1fe37cbd7c7802abf952bcdb3920610639becb110335b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Tue, 03 Jun 2025 22:53:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 03 Jun 2025 22:53:34 GMT
ENV MONGO_VERSION=7.0.21
# Tue, 03 Jun 2025 22:53:35 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.21-signed.msi
# Tue, 03 Jun 2025 22:53:36 GMT
ENV MONGO_DOWNLOAD_SHA256=35baeddf28f20f63a50d6a65bdb19492afdea42005bfb8621a8ec433ec9c748b
# Tue, 03 Jun 2025 22:55:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 03 Jun 2025 22:55:12 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 03 Jun 2025 22:55:13 GMT
EXPOSE 27017
# Tue, 03 Jun 2025 22:55:14 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Thu, 15 May 2025 19:25:03 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c039c6b198b97eae9c1a0a3457a007de784c617e233b4eb5a95b21a9798994b6`  
		Last Modified: Tue, 03 Jun 2025 23:13:05 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aae8d21e052ed762be0f4217bfc70627379eced7b5eb92b617e9ade36ad1cdd`  
		Last Modified: Tue, 03 Jun 2025 23:13:10 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a451db8148d02032d6a16c929595427e41ce2afd51f32babc07910eace6613`  
		Last Modified: Tue, 03 Jun 2025 23:13:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cad132f4f46b52475aaae5603eb22cdbba4d26c8edc0df1ff04e8d4b7ef822b`  
		Last Modified: Tue, 03 Jun 2025 23:13:18 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbe1316d134abe19308d4c8173b748c9aa6db19c7d7e2898dc81b668c54ac5f`  
		Last Modified: Wed, 04 Jun 2025 01:08:38 GMT  
		Size: 616.0 MB (615959634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a25c0b1edfe38e93a73bedca37a7aa09bbce15ccd1317e417921a1400c9849c`  
		Last Modified: Tue, 03 Jun 2025 23:13:23 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145fd6d866f90390a417e379afc67470972a566dcd8a17a44a847808540f5572`  
		Last Modified: Tue, 03 Jun 2025 23:13:25 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f847c8cfab596067b3f6fef9af864a109ce42d060faa930bcae8a53291d19b9`  
		Last Modified: Tue, 03 Jun 2025 23:13:29 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-windowsservercore` - windows version 10.0.20348.3692; amd64

```console
$ docker pull mongo@sha256:713a5475f24387b51cf1e4284c3dcb65978d42d2767887dca5f983b331b1ba9d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2889604746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d1afc1760cfbdfd998228588cd0565e063fbc1686f8674a45b73d9a2b57897`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 03 Jun 2025 22:48:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 03 Jun 2025 22:48:49 GMT
ENV MONGO_VERSION=7.0.21
# Tue, 03 Jun 2025 22:48:50 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.21-signed.msi
# Tue, 03 Jun 2025 22:48:51 GMT
ENV MONGO_DOWNLOAD_SHA256=35baeddf28f20f63a50d6a65bdb19492afdea42005bfb8621a8ec433ec9c748b
# Tue, 03 Jun 2025 22:51:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 03 Jun 2025 22:51:39 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 03 Jun 2025 22:51:40 GMT
EXPOSE 27017
# Tue, 03 Jun 2025 22:51:41 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f0e025dc84bc2922b78ded22dfe370ab8db63716ed99bf66474837fa786f067`  
		Last Modified: Tue, 03 Jun 2025 22:52:58 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e9d97fea1b752ea3d1241153929b83302ac58aed2d6886ee831ede1292a724`  
		Last Modified: Tue, 03 Jun 2025 23:00:09 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f593273d495a21b0994bde707fa5776fc5408a4bb8a7e8902a4813cf55a530`  
		Last Modified: Tue, 03 Jun 2025 23:00:14 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3592e4314869f3e86bd8d4c793683fb11fa608b592e7ca6340fff617758437`  
		Last Modified: Tue, 03 Jun 2025 23:00:16 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53ae107a18264e898f6bfefee096d4309f94854890fd561dba4be2753e8b372`  
		Last Modified: Tue, 03 Jun 2025 23:05:02 GMT  
		Size: 616.0 MB (615967594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c217c2a9ba079e72e02f85d87f87805487a71e5228f9d3c4e58e1c23c06aee7`  
		Last Modified: Tue, 03 Jun 2025 23:00:19 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3349522297f2c005ae6f5ad4a8d35ff0cfb5665e21ba888b9cd6825a4002742a`  
		Last Modified: Tue, 03 Jun 2025 23:00:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63307c1b46464e8473168b472986211398f8012de17506874b999a464f12fae6`  
		Last Modified: Tue, 03 Jun 2025 23:00:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
