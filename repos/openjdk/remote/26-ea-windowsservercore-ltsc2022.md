## `openjdk:26-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:5f1145d8c0fc9acd8ee5a7c8c949da59b424dd35988f692565a696860d62fd51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `openjdk:26-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

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
