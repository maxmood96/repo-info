## `openjdk:24-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:0ec49f514e34930b5aac1117db7c0ae3e3bd945af4cb4ada31f2f9cacd473a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `openjdk:24-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull openjdk@sha256:cd3d5886ad4611172aaef4602b08bf4279c12faf79beb4d32a86f4c01a47ac6d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2008560496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30d96bb9dabdad300667036763f86216f01c3b8be19887bf1e0db6d97b30a9b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Fri, 11 Oct 2024 19:07:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 11 Oct 2024 19:07:52 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 11 Oct 2024 19:07:52 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 11 Oct 2024 19:07:58 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 11 Oct 2024 19:07:59 GMT
ENV JAVA_VERSION=24-ea+19
# Fri, 11 Oct 2024 19:07:59 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/19/GPL/openjdk-24-ea+19_windows-x64_bin.zip
# Fri, 11 Oct 2024 19:08:00 GMT
ENV JAVA_SHA256=c90e6e8d5c865f3712dc302b6bec4f6c9f66d372764d0dbef55391fb52198a08
# Fri, 11 Oct 2024 19:08:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 11 Oct 2024 19:08:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99ebd1f9ca9a8c162a12c86b6fd7fd2174e0f6b6d2419da9c346820241d5365`  
		Last Modified: Fri, 11 Oct 2024 19:08:29 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0be229b6561339a2a7358ab37bcbc220cc2387fef4d7428f4f68569c498440`  
		Last Modified: Fri, 11 Oct 2024 19:08:29 GMT  
		Size: 483.0 KB (483047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a9ec6e4707075350412b93649b286fa45abf4dd40b5b7a468c0ff572db5258`  
		Last Modified: Fri, 11 Oct 2024 19:08:29 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5933a8cb3b75b0f3c34c124a85e8f8c5b8f152a1345b894b129b471e6acd1ec`  
		Last Modified: Fri, 11 Oct 2024 19:08:29 GMT  
		Size: 336.3 KB (336270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762b0061a28b09a6f4b04444cf2d45939c99dfb2ceef8494bb16440ea9243018`  
		Last Modified: Fri, 11 Oct 2024 19:08:28 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787b53e9dd2c704364d6f8a6c8343ec265de05595f7c6defe913d5cacd19f8be`  
		Last Modified: Fri, 11 Oct 2024 19:08:28 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e398914931112f49835c8a14fffcda458e9c06a9f3fd207e1de9e6b9e9945fcf`  
		Last Modified: Fri, 11 Oct 2024 19:08:28 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a37cb7c41efa324f04b88f2dd4f774382b0fd99e7176322db84a3cec477f25`  
		Last Modified: Fri, 11 Oct 2024 19:08:40 GMT  
		Size: 208.4 MB (208391702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc156d337ccb48e87d4672e29e865a208209c720c0a685518a0012333f7d5fa`  
		Last Modified: Fri, 11 Oct 2024 19:08:28 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
