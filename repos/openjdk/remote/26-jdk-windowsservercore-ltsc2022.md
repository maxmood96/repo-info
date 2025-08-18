## `openjdk:26-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:1d28cbeefe84d8fc27801524e95c6a86e9cc100163ea8a600511ff6f39245497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `openjdk:26-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull openjdk@sha256:eac04ad88f82a3b16e8eb1ae5925f03f135fa3f68bb9ca881c03be865e6bac11
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2501431475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71e7eb3de20f4e3ebafdb034c1bfb2f48e2b8296304486bea6f82b2de38e18e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Mon, 18 Aug 2025 18:20:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 18 Aug 2025 18:21:03 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 18 Aug 2025 18:21:04 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 18 Aug 2025 18:21:10 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 18 Aug 2025 18:21:12 GMT
ENV JAVA_VERSION=26-ea+11
# Mon, 18 Aug 2025 18:21:13 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_windows-x64_bin.zip
# Mon, 18 Aug 2025 18:21:14 GMT
ENV JAVA_SHA256=64e5c9fa2194c4b3cd3b424b1688dd4a30f7cb8e9b1b837030e835cfa5d8d866
# Mon, 18 Aug 2025 18:21:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 18 Aug 2025 18:21:37 GMT
CMD ["jshell"]
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
	-	`sha256:bf18e579a122a435885182d9bd1f24492aab4a0e6cb928cc513eb5b31c9fdfab`  
		Last Modified: Mon, 18 Aug 2025 18:23:11 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d46ee15c9913026207c0d5b7cf81b2bfbab7ec22ca932861e60cb8d6f197f5e4`  
		Last Modified: Mon, 18 Aug 2025 18:23:11 GMT  
		Size: 369.0 KB (369013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617f4514256c4c6027de5bc9f6761dffde218a281a0a4625592b418a2f8fd757`  
		Last Modified: Mon, 18 Aug 2025 18:23:11 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5841b3837c0860a3aa78cc9df6b755dbf675ab5e9799ddd8dedaed2e6319e58`  
		Last Modified: Mon, 18 Aug 2025 18:23:11 GMT  
		Size: 354.0 KB (354046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34988ed2608ee026f7d61e27f1ad8e7d8608fb1651dbcf13d3d1394532881683`  
		Last Modified: Mon, 18 Aug 2025 18:23:11 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac0069d36a50a53bd7b0b0fa5f46192e98648ec5f32d181a81862abbfa6e4f5`  
		Last Modified: Mon, 18 Aug 2025 18:23:12 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee37fa5cbfa84b3fcf15ca6d6747a539cc7e3ef30615070093a8f9146335838`  
		Last Modified: Mon, 18 Aug 2025 18:23:12 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aeb723cfa9291f9ba9705f9844996ec6edd59c6f47cd65dd5da0010efcb3224`  
		Last Modified: Mon, 18 Aug 2025 19:09:28 GMT  
		Size: 219.0 MB (219008714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aaa8d5343ddf43bb29c514db44d8980996b7fce5533656ea381603d85d6b12d`  
		Last Modified: Mon, 18 Aug 2025 18:23:12 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
