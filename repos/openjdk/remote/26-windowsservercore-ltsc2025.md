## `openjdk:26-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:3d432c2a6b30ece743ff374ad8987c5dc636e45f4710697ae09a58e6d6a41751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `openjdk:26-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

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
