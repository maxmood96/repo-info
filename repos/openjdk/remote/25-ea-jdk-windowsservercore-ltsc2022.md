## `openjdk:25-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:5c9c5975fe55941c9334a06cdf46d7048e4901484b32a4bd7ddea63559664892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `openjdk:25-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull openjdk@sha256:9ed1333f2739e58ea04afb499c712535331f5dd11221ad2d7e88b9c93fd30bb0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2483666221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63944e66ccd7f3610aa8912b80832274655663f8302e8a84c98a44f047c4ae70`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Fri, 16 May 2025 21:04:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 May 2025 21:04:24 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 16 May 2025 21:04:25 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 16 May 2025 21:04:31 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 16 May 2025 21:04:32 GMT
ENV JAVA_VERSION=25-ea+23
# Fri, 16 May 2025 21:04:32 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_windows-x64_bin.zip
# Fri, 16 May 2025 21:04:33 GMT
ENV JAVA_SHA256=903e77b6d79a2c808e32a4111a54802e149b11e39d15629d7a04ccfb97e4c79b
# Fri, 16 May 2025 21:04:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 16 May 2025 21:04:52 GMT
CMD ["jshell"]
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
	-	`sha256:5bb77149bb250a6a718022280db2075b45e6d815772aa1f3393fd87602fbd8be`  
		Last Modified: Fri, 16 May 2025 21:06:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a194cd0150b1cebd8ce8477b6680eb08f936eda8d9fc28c4676c4653240c465`  
		Last Modified: Fri, 16 May 2025 21:06:26 GMT  
		Size: 373.6 KB (373615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6109808ec595500f9243b380fe804cccc8d71ead6cedff824347ed463c73603d`  
		Last Modified: Fri, 16 May 2025 21:06:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac4a491f9c96211defff838b8ebd8839411cb77f801715c2ec9078fb4039853`  
		Last Modified: Fri, 16 May 2025 21:06:28 GMT  
		Size: 361.1 KB (361120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:407f9d80a44d667a68966a54f8b5ce16c58d3ab9e89237050193e400d37532a8`  
		Last Modified: Fri, 16 May 2025 21:06:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99811b8a85c2d2cdfbc85488728290e617f0a6b5efba8cdd8a5bc71341f4944a`  
		Last Modified: Fri, 16 May 2025 21:06:28 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9e8ec9046dbd4a9c1e72ff6d45089472ea23de0fdf4566230684b957eaf2d6`  
		Last Modified: Fri, 16 May 2025 21:06:29 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173b58d3b42c3a3079caeef797937322909559f0fd7040ab00c6caf0ef799308`  
		Last Modified: Fri, 16 May 2025 21:08:18 GMT  
		Size: 209.3 MB (209295654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9947447cac5190ad87c1f2fa0f92870775e91bb2ed20c69375639671aac1a158`  
		Last Modified: Fri, 16 May 2025 21:06:28 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
