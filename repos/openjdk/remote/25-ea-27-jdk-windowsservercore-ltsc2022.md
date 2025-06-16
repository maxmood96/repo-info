## `openjdk:25-ea-27-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:1c281ac8c31118550f6f8fb6c65a27d7002374034cdc90d1abf23d79415e7d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `openjdk:25-ea-27-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull openjdk@sha256:673b83d78c5618077113504c32b1cc9c8988e76fc323b52442c84d7ec9df397c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2499778942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502ff5f3e3484b72818bba55ae0e80c935fbe39f9ba39360f07017363b20b33e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Mon, 16 Jun 2025 17:54:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 16 Jun 2025 17:54:26 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 16 Jun 2025 17:54:27 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 16 Jun 2025 17:54:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 16 Jun 2025 17:54:34 GMT
ENV JAVA_VERSION=25-ea+27
# Mon, 16 Jun 2025 17:54:35 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/27/GPL/openjdk-25-ea+27_windows-x64_bin.zip
# Mon, 16 Jun 2025 17:54:36 GMT
ENV JAVA_SHA256=c29b512a7b967525b3286a6451ba478530d950d8d4981c8ce5d681ff715a5c22
# Mon, 16 Jun 2025 17:54:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 16 Jun 2025 17:55:00 GMT
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
	-	`sha256:e52d8e2771faa6bf03122e8a088ead3d0d133d898e97202fd54f59586d3290b7`  
		Last Modified: Mon, 16 Jun 2025 17:56:33 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22caf26579711b3b4d672f08266b383c714ed0b20fbd6cac20ccc1788a90520`  
		Last Modified: Mon, 16 Jun 2025 17:56:33 GMT  
		Size: 357.6 KB (357598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5f73cafe8e470cd078b7506ce89bc4dfcc2040c26bdd4ab3c310eaf67f143a`  
		Last Modified: Mon, 16 Jun 2025 17:56:33 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebaf78da7d05ec9bf5b0fce1db9feb2eab63b4e71083e6a7924f397af725ab45`  
		Last Modified: Mon, 16 Jun 2025 17:56:33 GMT  
		Size: 346.2 KB (346207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97aa9de85d10673a5db71da59d26e340598b14737378e8ef121f425a462846b`  
		Last Modified: Mon, 16 Jun 2025 17:56:33 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9bdab477f4018735a24ce52a2f805a62e868a43329e4f7642bab792d88ae5e`  
		Last Modified: Mon, 16 Jun 2025 17:56:33 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c652090baf3de091e523aab727f25b6a448c035146d56a3018192f3cabecc122`  
		Last Modified: Mon, 16 Jun 2025 17:56:34 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84f4204dd629da2838aed62d52b357d261ae8d771742a4adeb274dd08c11966`  
		Last Modified: Mon, 16 Jun 2025 18:08:37 GMT  
		Size: 218.8 MB (218815846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a110126960289f578c57f7403ba91062fd37ec236ead20480c681ff9094a81f6`  
		Last Modified: Mon, 16 Jun 2025 17:56:34 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
