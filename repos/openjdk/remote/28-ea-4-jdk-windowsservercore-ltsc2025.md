## `openjdk:28-ea-4-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:17e526299037933e09881391fa8e7a73b0341ebd95ff2bf20baaf1aa71e78b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `openjdk:28-ea-4-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull openjdk@sha256:0b17e008ecd8cf67c4817fa90bc1deb2d695185c7330de77390bc33353d87664
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2504406076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5dfa3571b598e3029eeab9660054c23f8aa485020824e4c59f6d7d622698180`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Fri, 26 Jun 2026 22:42:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Jun 2026 22:43:25 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 26 Jun 2026 22:43:26 GMT
ENV JAVA_HOME=C:\openjdk-28
# Fri, 26 Jun 2026 22:43:32 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 26 Jun 2026 22:43:32 GMT
ENV JAVA_VERSION=28-ea+4
# Fri, 26 Jun 2026 22:43:33 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_windows-x64_bin.zip
# Fri, 26 Jun 2026 22:43:34 GMT
ENV JAVA_SHA256=b85f4b0c1313453fc760c198dec39f0c3a27e386671a184a123c19fcfb46c776
# Fri, 26 Jun 2026 22:44:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 26 Jun 2026 22:44:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8e4546b69fc08bed7bcc81486904a224e3a5e52d2a8c4dca141adca5ee5ce0`  
		Last Modified: Fri, 26 Jun 2026 22:44:07 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff609767754f9b924164651999bae6286a7bd48f87a9139fa1eb36a0a6bcd768`  
		Last Modified: Fri, 26 Jun 2026 22:44:07 GMT  
		Size: 402.6 KB (402571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ac0af4c28df97ed46f78c867f8ab2a0447ccf0fdb07fe6d3e26d8325d34144`  
		Last Modified: Fri, 26 Jun 2026 22:44:07 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ae7cb620fb920cd95bfea7f2a20fbf67082af59603aba342d7ce75cf50d4be`  
		Last Modified: Fri, 26 Jun 2026 22:44:07 GMT  
		Size: 390.1 KB (390092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c12e28cb48b30bc7ad092e94270c725615e04db0a8fbffeb1b2bec412dab5e0`  
		Last Modified: Fri, 26 Jun 2026 22:44:05 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d342bd7ab30f17d3e1815b1a3e603bd9d90c1cd960a60755f0c855d14e8fbc10`  
		Last Modified: Fri, 26 Jun 2026 22:44:05 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700ef82c47bc6ae276429173436bccfc7077070927b9be5628bcb3e03e3b896d`  
		Last Modified: Fri, 26 Jun 2026 22:44:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2b2c841cff667bb27278ef8709950bcf2b685c6567e0416a71e57055eeb54f`  
		Last Modified: Fri, 26 Jun 2026 22:44:21 GMT  
		Size: 224.5 MB (224462685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2b7c40675f1a3dc7dff1cbbf73c32eff9455e61e9132903d565e1d93c2953`  
		Last Modified: Fri, 26 Jun 2026 22:44:05 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
