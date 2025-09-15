## `openjdk:26-ea-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:3be396ef6188ce6038c553476962ef52e538c301f899ab8c07473fe41532b7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `openjdk:26-ea-jdk-windowsservercore` - windows version 10.0.26100.6584; amd64

```console
$ docker pull openjdk@sha256:d564a18d94a13fdb9836ba330eb53fbc13c23a5eb74dc3d17183a213d258f439
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3791403877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb715334491dd22c44327ce9b9b9003dbca5a8bb71dc498438e5fd7fb6dc7fc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Mon, 15 Sep 2025 17:04:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 15 Sep 2025 17:04:58 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 15 Sep 2025 17:04:59 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 15 Sep 2025 17:05:05 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 15 Sep 2025 17:05:05 GMT
ENV JAVA_VERSION=26-ea+15
# Mon, 15 Sep 2025 17:05:06 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/15/GPL/openjdk-26-ea+15_windows-x64_bin.zip
# Mon, 15 Sep 2025 17:05:07 GMT
ENV JAVA_SHA256=8620c77a818f584769ebda95d4cb9d48d02f8340a9b16467de74590ec46c730c
# Mon, 15 Sep 2025 17:06:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 15 Sep 2025 17:06:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0861dde30c6849e0475df82b1911098b91a571b937e143589b1fa4292613bfbe`  
		Last Modified: Mon, 15 Sep 2025 17:20:45 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c474329c9cc5d1ccd0c4ec5cbd53e1cb2135929dbe4e1dfd236894ff3ed014c8`  
		Last Modified: Mon, 15 Sep 2025 17:20:46 GMT  
		Size: 364.7 KB (364671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c43d97d08aaaa5ad05f4079e49b66252ed50a68644c9f310719bff37113e14`  
		Last Modified: Mon, 15 Sep 2025 17:20:46 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e91df1a61ac000617b6afba5d588b93d31e57c39faad4eabbc3c2192e45051`  
		Last Modified: Mon, 15 Sep 2025 17:20:46 GMT  
		Size: 339.5 KB (339535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ebc35c30e50895f833057a6e45ae69dfdf47ffe20c38e0e0efdef0ebd93f7c4`  
		Last Modified: Mon, 15 Sep 2025 17:20:46 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10139e7c54f656bf9f7ee9550045ea3c94c2e9a0b3596efd8a08fba5ed91643b`  
		Last Modified: Mon, 15 Sep 2025 17:20:46 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20582e5a6292c8bbaeff48e34d7690b589fc5d683111b962b482a3a03c57c5ec`  
		Last Modified: Mon, 15 Sep 2025 17:20:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a486f9442a913632aa0ae10ab1275fc1590eee71482eb3e02123c3589c11f6`  
		Last Modified: Mon, 15 Sep 2025 18:03:53 GMT  
		Size: 219.3 MB (219252132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744aba06fd809aa6bc621b07efd2cf375af59ab0766160257b3840b0e330e8e6`  
		Last Modified: Mon, 15 Sep 2025 17:20:46 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-jdk-windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull openjdk@sha256:15a7aef11154b87560db5a79626b5d29b11e5fd76e6dc995349b70f8e3f4975e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2502168548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92080218e327a9b0bfb3fb8794e201bef8d3912cc03909bee8c20f009c92cab`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Mon, 15 Sep 2025 16:58:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 15 Sep 2025 16:59:21 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 15 Sep 2025 16:59:22 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 15 Sep 2025 16:59:29 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 15 Sep 2025 16:59:29 GMT
ENV JAVA_VERSION=26-ea+15
# Mon, 15 Sep 2025 16:59:30 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/15/GPL/openjdk-26-ea+15_windows-x64_bin.zip
# Mon, 15 Sep 2025 16:59:32 GMT
ENV JAVA_SHA256=8620c77a818f584769ebda95d4cb9d48d02f8340a9b16467de74590ec46c730c
# Mon, 15 Sep 2025 16:59:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 15 Sep 2025 16:59:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebdce8c236e588a48abb72ba4f4cfbb4707871e712f18537c070ee45f227099`  
		Last Modified: Mon, 15 Sep 2025 17:18:41 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c343394d662c7529c736bec3dd6f525ce2b61d0630dba2dac7c1fbcf35e921f`  
		Last Modified: Mon, 15 Sep 2025 17:18:45 GMT  
		Size: 378.7 KB (378743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325b5b433722ebc365a55e957ed08aebbae704c1e350059aef8f969d7b1eeb3c`  
		Last Modified: Mon, 15 Sep 2025 17:18:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecce369025075ec85e56ae819ffda37700567f05c5089eab5888feeec16792a`  
		Last Modified: Mon, 15 Sep 2025 17:18:55 GMT  
		Size: 360.4 KB (360397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74dabb6bc550ca72be5291337621b97b2bb372bff44e3efe06dcd6aea823e58`  
		Last Modified: Mon, 15 Sep 2025 17:19:00 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5407430b9f2621d06b6eb9ea4c34f62f8d9abaf537f02aacd82f7e96a88b0b`  
		Last Modified: Mon, 15 Sep 2025 17:19:05 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4621e780c6196dd1b7badd8ed0d3ee79f6cb2e4cbb1f0f99d5c925b24f4585`  
		Last Modified: Mon, 15 Sep 2025 17:19:09 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87cd30e7b307ec07d89a4693c56247aa25e02c346b1cbbe286d92df1916b979`  
		Last Modified: Mon, 15 Sep 2025 18:02:42 GMT  
		Size: 219.3 MB (219276588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:294597be4a1fc35b0369fb73c6f27518dddf699b4fbee1fed75ed2c07d0887fe`  
		Last Modified: Mon, 15 Sep 2025 17:19:13 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
