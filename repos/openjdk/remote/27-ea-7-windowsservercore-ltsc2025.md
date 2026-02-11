## `openjdk:27-ea-7-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:9787d41eea7f941befedc42743e426f1bdc01879c841ca649d7d15e05ed5763d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `openjdk:27-ea-7-windowsservercore-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull openjdk@sha256:636c9113cc632da762cda19696f77fdef58e18046c9e34267bf9c03fad7f2cf5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190074053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93dd16422b3cf9cc29156d4aa1c3082b144d3c778d8eabef847571fbf96f99f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Tue, 10 Feb 2026 22:51:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 22:59:50 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 10 Feb 2026 22:59:50 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 10 Feb 2026 22:59:56 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 10 Feb 2026 22:59:57 GMT
ENV JAVA_VERSION=27-ea+7
# Tue, 10 Feb 2026 22:59:57 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_windows-x64_bin.zip
# Tue, 10 Feb 2026 22:59:58 GMT
ENV JAVA_SHA256=5940fbffa36c927e8b186d5bcdaa99e332aebc16b642bb272e05e5cce059d4a3
# Tue, 10 Feb 2026 23:00:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 10 Feb 2026 23:00:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f3641b48551abf691e707ba76f8b07a225d509249237749ad0c13cbcab89a6`  
		Last Modified: Tue, 10 Feb 2026 22:52:23 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e4124b1cce80532ad36119cdffa374f16bf9b0f7dd7b9ee443ca982f1e1dd6`  
		Last Modified: Tue, 10 Feb 2026 23:00:32 GMT  
		Size: 353.8 KB (353825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58949618ad1e3582ebd429e2864730c3b8255c470e90dcd4b1c3fb44b24da932`  
		Last Modified: Tue, 10 Feb 2026 23:00:31 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e36215dfca2b540a9963ae855a8763fd2d1b957d753ec37825daf537ffeb63`  
		Last Modified: Tue, 10 Feb 2026 23:00:30 GMT  
		Size: 340.9 KB (340876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a7df20cb6cbf5751d47a9563d854bdff0b6b68f6e7ba5f3e10ead3226a33657`  
		Last Modified: Tue, 10 Feb 2026 23:00:29 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd596adbd67f16e30d0c5d1a7780ace8c63783316c6a0a123980769b060e09f2`  
		Last Modified: Tue, 10 Feb 2026 23:00:28 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902bab5592ac59365b1010d31704d1ac559a20f66da62bfc64225c726958067f`  
		Last Modified: Tue, 10 Feb 2026 23:00:27 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb9cdaa65c7351505fc6629435fb20a48cd8f2d3cb88b48ff633ec692910d70`  
		Last Modified: Tue, 10 Feb 2026 23:00:44 GMT  
		Size: 224.6 MB (224611492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819c331cff668e8a975c5fbcf20d7709b6b8f12c4514b23e6e8b1746bc55272e`  
		Last Modified: Tue, 10 Feb 2026 23:00:28 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
