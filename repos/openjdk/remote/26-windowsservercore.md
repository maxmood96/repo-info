## `openjdk:26-windowsservercore`

```console
$ docker pull openjdk@sha256:360d4a72ba218fdfd51a2d3964838965caf19fddaa644528d1b434bd7ca69d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `openjdk:26-windowsservercore` - windows version 10.0.26100.4946; amd64

```console
$ docker pull openjdk@sha256:cb3de8b0192c637700f4ee674b04f9c04aa3e5ffa59282473159be0b65746440
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3718547204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5802e0dba17a2bef41300e1fb7b72371ee2969438820262f99cc0f31586916ef`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 12 Aug 2025 20:33:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:34:05 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:34:06 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 12 Aug 2025 20:34:12 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:34:13 GMT
ENV JAVA_VERSION=26-ea+10
# Tue, 12 Aug 2025 20:34:13 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/10/GPL/openjdk-26-ea+10_windows-x64_bin.zip
# Tue, 12 Aug 2025 20:34:14 GMT
ENV JAVA_SHA256=da62aabe3ec673f91e3aafcc742d67304275407dff329118db9e2bcfbddaca5b
# Tue, 12 Aug 2025 20:34:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:34:31 GMT
CMD ["jshell"]
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
	-	`sha256:41a10cef8978ae5290ca7e18220c36d2928dcd71d266fde25547632fda46297f`  
		Last Modified: Tue, 12 Aug 2025 20:38:37 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9132b3afc45b96364af8e47a7f150cb8465174096316ad5e629f052d57dc133`  
		Last Modified: Tue, 12 Aug 2025 20:38:35 GMT  
		Size: 375.6 KB (375595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6882e0d97c94644f7699a23cb82dd0c92270b7a6f44d4cb1148ba0eec10a3d7c`  
		Last Modified: Tue, 12 Aug 2025 20:38:35 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5af1b40091e65f279501459bce9f39ead2d2d663e723e6b89f9c81914a4792`  
		Last Modified: Tue, 12 Aug 2025 20:38:35 GMT  
		Size: 357.5 KB (357504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07bf86809e91c72d4e72a1b9e423ff18d59bb9d1359ca14d2d68a0a3327d79e`  
		Last Modified: Tue, 12 Aug 2025 20:38:35 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d18cf2f1cb9e14f740e1a068b47a7ef1a814a94a4941178af0d4f5fb8fa57a7`  
		Last Modified: Tue, 12 Aug 2025 20:38:35 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ccdad26d9d16038e40d6088fef1d46d4d0fa20d851f381db1901332f1ca522`  
		Last Modified: Tue, 12 Aug 2025 20:38:35 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d49f5602fa91b48113b5ed11ceff803e700242eb43ca7acb2989e8be3d9520`  
		Last Modified: Tue, 12 Aug 2025 20:46:42 GMT  
		Size: 219.0 MB (218975610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8999220a5fb6d9ae624f0c494abb5bb833542b1ac3ff0d4cc8fa3ba6f9ac20a`  
		Last Modified: Tue, 12 Aug 2025 20:38:36 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull openjdk@sha256:9dcf7a78bafc7fa6267eeeefb728922c8a12354b66d90a78ae7b70c138ab19c2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2501325534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d7b817de4dfc900c62202e6219f09748183dca07166ca5d3e3f577bc3c2cb3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:33:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:33:55 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:33:56 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 12 Aug 2025 20:34:03 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:34:04 GMT
ENV JAVA_VERSION=26-ea+10
# Tue, 12 Aug 2025 20:34:05 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/10/GPL/openjdk-26-ea+10_windows-x64_bin.zip
# Tue, 12 Aug 2025 20:34:06 GMT
ENV JAVA_SHA256=da62aabe3ec673f91e3aafcc742d67304275407dff329118db9e2bcfbddaca5b
# Tue, 12 Aug 2025 20:34:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:34:28 GMT
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
	-	`sha256:cb44453f998ae873970ebb2cf9b7344ada6208d3ae918dce541baeee8c1c9e5f`  
		Last Modified: Tue, 12 Aug 2025 20:36:03 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51105a5697c7f6efd7db63b43b8c993512296bc774ff582d7a0e2358cb7c015`  
		Last Modified: Tue, 12 Aug 2025 20:36:02 GMT  
		Size: 343.2 KB (343173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97361a7aae0233b88c7dc8390dcc770147179e16250461d0081192b3ff11e2e9`  
		Last Modified: Tue, 12 Aug 2025 20:36:03 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b08e89ce9d068a79f518d0c4afdba46c035bd946a97e40a0246336cb5d49fa`  
		Last Modified: Tue, 12 Aug 2025 20:36:04 GMT  
		Size: 332.8 KB (332766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d08fe501ce613175f6fddad35a44d7a5b94835825fa9c6cbe12055fd0aee3f`  
		Last Modified: Tue, 12 Aug 2025 20:36:05 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd12050a61f8b6208a231be37f8bed489782e26a6214dd7b82ad8ff4cf1e6d5`  
		Last Modified: Tue, 12 Aug 2025 20:36:05 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a29f81b6a16a667683506a7076e956ea598d59531562ed3f6965bdf85514fb`  
		Last Modified: Tue, 12 Aug 2025 20:36:04 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2007a66b04ecaac5a23a7b367d7f8ced222d1a8a5fbe430c241165174affcad`  
		Last Modified: Tue, 12 Aug 2025 20:45:34 GMT  
		Size: 218.9 MB (218949928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6951832694311fa47b27a4fc8662b5ec77e8cb66b4d52a1465ead3f04d40b6`  
		Last Modified: Tue, 12 Aug 2025 20:36:05 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
