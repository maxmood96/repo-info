## `openjdk:25-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:3d100e3ea944b8d1b92f2483caf8c3cb9246a675f67d05d56bea7bd888901545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `openjdk:25-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:1fea92a8ecd0a149cecebce5f00335d38107f7e29b5b9556ef8715715acb8453
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2470904786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8d28d754bdf77e87205f59b3968977948e0c91b6cab673bd24dda8c3ba5357e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 11 Feb 2025 00:27:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Feb 2025 00:28:35 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:28:36 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 11 Feb 2025 00:28:49 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:28:50 GMT
ENV JAVA_VERSION=25-ea+9
# Tue, 11 Feb 2025 00:28:50 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_windows-x64_bin.zip
# Tue, 11 Feb 2025 00:28:51 GMT
ENV JAVA_SHA256=422ffa84afebca61d5ff96e0459231633ad47f082eb11fbecdb64c76e37b35ea
# Tue, 11 Feb 2025 00:29:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:29:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20b4d605e705d3f47072b7d2766df33099177a0b668693003d19bdf3c6a9340`  
		Last Modified: Tue, 11 Feb 2025 00:29:23 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc94b17f055ae5d776d17833337cdb19f892b69e078438574804239ee3ea3bb`  
		Last Modified: Tue, 11 Feb 2025 00:29:23 GMT  
		Size: 365.0 KB (365034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99216bb37b1d08e1e59de495a3808e5f400e470cb619f68dbcf10f143ab2c714`  
		Last Modified: Tue, 11 Feb 2025 00:29:23 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8885f460c82d88e3fbc71353191e82c3f11d2a5a5f3f69268a62645771f400dc`  
		Last Modified: Tue, 11 Feb 2025 00:29:23 GMT  
		Size: 312.4 KB (312424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f6b9653fe28ad47ebbd26d417ab788c68f684fdf834da41b0f6672e04df365`  
		Last Modified: Tue, 11 Feb 2025 00:29:22 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f671062518fe644d4999c69ddc0b72f5ff59f4ff90fb26d4ff88beee1e87dea8`  
		Last Modified: Tue, 11 Feb 2025 00:29:22 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddecbdb2d2e8c88371cf678d724b8f18bc26f58257cb49d9a76c0c313765c7ed`  
		Last Modified: Tue, 11 Feb 2025 00:29:22 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8dabbc2b2320f85a5094a57d80cc2e3a116a500cbf6773a5f0276b91a940ec`  
		Last Modified: Tue, 11 Feb 2025 00:29:33 GMT  
		Size: 207.8 MB (207834366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146db06c36f6b9da5d3f925c3bc657440df28e0ab03f8a59292dff5fc21cc19a`  
		Last Modified: Tue, 11 Feb 2025 00:29:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
