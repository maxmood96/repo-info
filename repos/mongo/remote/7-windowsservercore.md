## `mongo:7-windowsservercore`

```console
$ docker pull mongo@sha256:3c086207c346a0e767c68b891f66cb72c459a461c166e60e8a49e0f3de94506c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `mongo:7-windowsservercore` - windows version 10.0.26100.32995; amd64

```console
$ docker pull mongo@sha256:2a2ab6dd46a8eebb2895da89a0a6dba6e5132c2420eda555b33226e09d2766fd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2902994151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c833fc4a2ffe5c15fa1441191efbda806bc08579b0a341298ccfc949e387768`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Fri, 12 Jun 2026 19:14:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 12 Jun 2026 19:14:33 GMT
ENV MONGO_VERSION=7.0.37
# Fri, 12 Jun 2026 19:14:35 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.37-signed.msi
# Fri, 12 Jun 2026 19:14:36 GMT
ENV MONGO_DOWNLOAD_SHA256=110a4774e93dd3dd253725f18bc87b77468521875d7448ca5f79fb1d5045cedc
# Fri, 12 Jun 2026 19:16:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 12 Jun 2026 19:17:00 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 12 Jun 2026 19:17:01 GMT
EXPOSE 27017
# Fri, 12 Jun 2026 19:17:02 GMT
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
	-	`sha256:aebbdfcf85d8f881db133bd5455f1a7e0332c4f35d9eded01268ed34d9c8393a`  
		Last Modified: Fri, 12 Jun 2026 19:17:08 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d0013d156d83b3d20d42f3db0f68c7c003037ee96457602e409fc760fa0721`  
		Last Modified: Fri, 12 Jun 2026 19:17:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e06e0ee86ec37503073a9fbd12d32eacc908c3c11e1d5ad49f9938ed50deb2e`  
		Last Modified: Fri, 12 Jun 2026 19:17:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0093f9b7695ebedc27123f0b235ed3f5b63d46a6dec785e96539a649dac02562`  
		Last Modified: Fri, 12 Jun 2026 19:17:06 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ce48c312ba0bce59e76d997616e69be954527c444159c080d7ed037e41ff2f`  
		Last Modified: Fri, 12 Jun 2026 19:18:02 GMT  
		Size: 623.8 MB (623842059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea2a143fa3def0432fb11d53e74033d6e3c5b67ee9519e6b83e76f54ec54adf`  
		Last Modified: Fri, 12 Jun 2026 19:17:06 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e1ddad0f55447ffb460e0fd19e7111d65907ab23e50eda42b076915cb07113`  
		Last Modified: Fri, 12 Jun 2026 19:17:06 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31dc0337ed531ad7a46b9d83177c1886270f8c502041ffc5beb3b886d1e56047`  
		Last Modified: Fri, 12 Jun 2026 19:17:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-windowsservercore` - windows version 10.0.20348.5256; amd64

```console
$ docker pull mongo@sha256:3f5c56013fb978f56849376b2d777a7d84bad4b04572e2e4f1d2c0aa5f9e1a59
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2756082467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25151158c272adc2a0b3bb3a6cebb132f3a28b75bdefc837b51b9adc2b7c64e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Fri, 12 Jun 2026 19:23:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 12 Jun 2026 19:23:28 GMT
ENV MONGO_VERSION=7.0.37
# Fri, 12 Jun 2026 19:23:29 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.37-signed.msi
# Fri, 12 Jun 2026 19:23:30 GMT
ENV MONGO_DOWNLOAD_SHA256=110a4774e93dd3dd253725f18bc87b77468521875d7448ca5f79fb1d5045cedc
# Fri, 12 Jun 2026 19:25:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 12 Jun 2026 19:25:42 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 12 Jun 2026 19:25:43 GMT
EXPOSE 27017
# Fri, 12 Jun 2026 19:25:43 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d07a1b9de415ccd0f36e42cd7c6cd82307c4d8279074f01838b9af4a89bf635`  
		Last Modified: Fri, 12 Jun 2026 19:25:59 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7bb95fea82afd2ee058d362c1c1b5012f4d7f3d85cc98ea4b149f095f9f965`  
		Last Modified: Fri, 12 Jun 2026 19:25:59 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1ab4d34fba95f0ca4d719f1a9ab1e246634ecd8764eb542ac806c1aeb2b456`  
		Last Modified: Fri, 12 Jun 2026 19:25:59 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41355ebd13141bedf709b5a43f1334870effa4c0ea8fb02c6e73b36458dca3a3`  
		Last Modified: Fri, 12 Jun 2026 19:25:57 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80269167abc9f73a3dc8576c12bd844fcfe41daa80788e8b6215d5fc5950b5e`  
		Last Modified: Fri, 12 Jun 2026 19:27:00 GMT  
		Size: 623.9 MB (623947729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9721defbd8b97a5008d6d163030c6b8a22c3d039888abd021007df84557beb`  
		Last Modified: Fri, 12 Jun 2026 19:25:57 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c658dd84e395f13313e656db73d22f5d06a09c91c26670440248c2d4945ca18`  
		Last Modified: Fri, 12 Jun 2026 19:25:57 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f33e29c4d4c1775ab97ef01dd4e1c2a4c9029117f86428ead2e38a707d7b699`  
		Last Modified: Fri, 12 Jun 2026 19:25:57 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
