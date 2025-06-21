## `openjdk:25-ea-windowsservercore`

```console
$ docker pull openjdk@sha256:ff0e9f2fe1d9aba70934c5dfaf1216418704cf37cafc0a756c32d941c49912a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `openjdk:25-ea-windowsservercore` - windows version 10.0.26100.4349; amd64

```console
$ docker pull openjdk@sha256:fdff7485f3be6a85b74575fe453e10bccf29cc025fe7ea03874d9c4d7280f288
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3695826780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44c463dec56ef5785b955522326b5e01754c756aecfcf18fb2340a6d4b117a9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Sat, 21 Jun 2025 00:33:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 21 Jun 2025 00:33:11 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 21 Jun 2025 00:33:12 GMT
ENV JAVA_HOME=C:\openjdk-25
# Sat, 21 Jun 2025 00:33:19 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 21 Jun 2025 00:33:19 GMT
ENV JAVA_VERSION=25-ea+28
# Sat, 21 Jun 2025 00:33:20 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/28/GPL/openjdk-25-ea+28_windows-x64_bin.zip
# Sat, 21 Jun 2025 00:33:21 GMT
ENV JAVA_SHA256=4e1f6ee8523006f5f4e9c5e78283bec3011ecacaac80de81b4e8f75647efc1cc
# Sat, 21 Jun 2025 00:33:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 21 Jun 2025 00:33:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f4a0bf9272137e6cf08d4071c7512e920869365c2f79571d873200b43080256`  
		Last Modified: Sat, 21 Jun 2025 00:50:58 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d34d4ff6383d2f62ac21966200466358a98aa833a337c6e15d583802bde6e5`  
		Last Modified: Sat, 21 Jun 2025 00:51:02 GMT  
		Size: 396.3 KB (396314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a188b5398e4aad8a85ac58695a468e7784accf3c1c217ed53a8d6cd62e8e968`  
		Last Modified: Sat, 21 Jun 2025 00:51:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023dd2881a668d20b9a3e4c384c97a1e7b9b00f4ae6a142b0ed2c4448168fe6d`  
		Last Modified: Sat, 21 Jun 2025 00:51:17 GMT  
		Size: 381.2 KB (381230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df5bfbe86c3953a10af010bbcae765085565d4feaa0fbfe1fde4b088793f7de`  
		Last Modified: Sat, 21 Jun 2025 00:51:27 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59dcbebb688a373a8cb940b0a66b52b0d9670a84228955aa3dc5304cadef3814`  
		Last Modified: Sat, 21 Jun 2025 00:51:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e23c077a9abda0a0a8d4ce5ba22279006ddf3755706530bf67101b66536059`  
		Last Modified: Sat, 21 Jun 2025 00:51:33 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69dcecc462c84e33868731f5e1fbafe120d27a6d8cf7972d4e5fd1ba28324b5d`  
		Last Modified: Sat, 21 Jun 2025 01:08:05 GMT  
		Size: 218.9 MB (218867376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4033b606c7805159d73aa850126d7362c1b29f95c21b500cce920c382b205a0b`  
		Last Modified: Sat, 21 Jun 2025 00:51:36 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-windowsservercore` - windows version 10.0.20348.3807; amd64

```console
$ docker pull openjdk@sha256:860df8a554e1356c0797e78b5873dc15ad111978ecb43151301dfa073caebb6a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2499793514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b297fa48354319ac24f01fc002defc1b8d1f1a8c00070750d47eacfa90b533c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Sat, 21 Jun 2025 00:28:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 21 Jun 2025 00:28:25 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 21 Jun 2025 00:28:25 GMT
ENV JAVA_HOME=C:\openjdk-25
# Sat, 21 Jun 2025 00:28:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 21 Jun 2025 00:28:34 GMT
ENV JAVA_VERSION=25-ea+28
# Sat, 21 Jun 2025 00:28:34 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/28/GPL/openjdk-25-ea+28_windows-x64_bin.zip
# Sat, 21 Jun 2025 00:28:35 GMT
ENV JAVA_SHA256=4e1f6ee8523006f5f4e9c5e78283bec3011ecacaac80de81b4e8f75647efc1cc
# Sat, 21 Jun 2025 00:28:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 21 Jun 2025 00:28:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b790e4076f3273d9da88ae8b790e3c86b598981e20bb6b720b49ff0059f9eeff`  
		Last Modified: Sat, 21 Jun 2025 01:07:48 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3468d94d4e83dc63887eae927f28031a88c1eeb497a1cb384e0c8de090f0e1a6`  
		Last Modified: Sat, 21 Jun 2025 01:07:48 GMT  
		Size: 357.8 KB (357784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fedfd2a6b43aaaf68b7a4cba5b13cfd1d7362c53f37c91cbcc7a29ed59a048e6`  
		Last Modified: Sat, 21 Jun 2025 01:07:48 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6dd8e9cb6e61436df4351ecebea6c6db91f42ea2a80bb7374d3d526c6dbd4a`  
		Last Modified: Sat, 21 Jun 2025 01:07:48 GMT  
		Size: 347.0 KB (346952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b809b37c618490ce75f0e5457f90cb2f4b6354619f3b62e91025616af1c2dcca`  
		Last Modified: Sat, 21 Jun 2025 01:07:48 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88f1738bc60fa0f396719db8fab97f223d27039fda55f170a1f57908f0d0ed6`  
		Last Modified: Sat, 21 Jun 2025 01:07:48 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4f456142f3df756eff4e456e83d01b785726af5220560b4722170f47fddaae`  
		Last Modified: Sat, 21 Jun 2025 01:07:49 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa1290fe761aebf6020d89c1f1d34f19b12344eabec793511f43f20ab375681`  
		Last Modified: Sat, 21 Jun 2025 01:08:06 GMT  
		Size: 218.8 MB (218829442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d1332858a239584aca9854f908a935907f2cc022796289b4f40c15da105535`  
		Last Modified: Sat, 21 Jun 2025 01:07:49 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
