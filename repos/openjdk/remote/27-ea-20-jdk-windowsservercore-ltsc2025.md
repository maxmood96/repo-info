## `openjdk:27-ea-20-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:ec8bddf32561e1083c0ead30beed3ec9682049ff1fbc95144e115718aa5114b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `openjdk:27-ea-20-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull openjdk@sha256:2ac8a82b75b0cc92073499a1fae982f917dec978b8df8c5657886c676d76d479
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2355726950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d74b3f0882f7a711b627a00ff60021b8ce3efc1412b34b4b5651fe8b26aedbb8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 05 May 2026 22:59:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 May 2026 23:00:56 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 05 May 2026 23:00:57 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 05 May 2026 23:01:03 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 05 May 2026 23:01:04 GMT
ENV JAVA_VERSION=27-ea+20
# Tue, 05 May 2026 23:01:05 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_windows-x64_bin.zip
# Tue, 05 May 2026 23:01:06 GMT
ENV JAVA_SHA256=5499df903e0ea0fb9652da36292197a89324f03f18fc670d4af55d54c5a75687
# Tue, 05 May 2026 23:01:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 05 May 2026 23:01:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba25f10142e04eaa4f1a4b100591667fb5223281f472a85ba0715fa43973b42c`  
		Last Modified: Tue, 05 May 2026 23:01:49 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2c391f78a3c64fcd513c117a4524f93e9f8f6b808f8a5a5ff84c7acdc85082`  
		Last Modified: Tue, 05 May 2026 23:01:49 GMT  
		Size: 370.7 KB (370693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce38463a8d0ab9af10e93337a3361fe18969f4eaa8d96a0f3c0777eeb054544`  
		Last Modified: Tue, 05 May 2026 23:01:49 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2bcfac10a308f61ecab150b4b3f64a0c902f5591c5c7a5d3232e9334e5e3a44`  
		Last Modified: Tue, 05 May 2026 23:01:49 GMT  
		Size: 371.3 KB (371338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b1221112cc13a8c99673908638c51f4f674d2d057962f65646f349187dbdc35`  
		Last Modified: Tue, 05 May 2026 23:01:47 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b23fd73c144b7808bc6ddbae8c365ef4a2a7ca89f84d9ffbc3fc6922d0c946`  
		Last Modified: Tue, 05 May 2026 23:01:47 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae7b0e63c608559d8b65a8414e09503e6d6b346f43169a6dc472eb12d097bfb`  
		Last Modified: Tue, 05 May 2026 23:01:47 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03792966c2c3fb38e7f27aca5544b55503316d3a4dc16d8db6fb190d96c8c1b6`  
		Last Modified: Tue, 05 May 2026 23:02:03 GMT  
		Size: 225.0 MB (224991023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9091292491ea459e809847a9d1bee1760f8d23966b57a5175f112ea7dfb0fea4`  
		Last Modified: Tue, 05 May 2026 23:01:47 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
