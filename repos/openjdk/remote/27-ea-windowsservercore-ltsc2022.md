## `openjdk:27-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:02697950624d9d0a0e0a372f4c83edf41eba56347a22e429d769d1f4d9ebe49b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `openjdk:27-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull openjdk@sha256:4c7c1047999b86628d817a1d0a72acc4a887e378581d20f8703b16615daeafd9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2006334704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152a656b4e6a7f13e76e6649f7664bb8528130d51e0640cc1541d7768b887055`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 09 Dec 2025 20:29:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:45:16 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:45:17 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 09 Dec 2025 20:45:22 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:45:23 GMT
ENV JAVA_VERSION=27-ea+1
# Tue, 09 Dec 2025 20:45:24 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_windows-x64_bin.zip
# Tue, 09 Dec 2025 20:45:25 GMT
ENV JAVA_SHA256=77d566459162b6597396e779186334a870aeee1837fe453aac80662b023659c1
# Tue, 09 Dec 2025 20:46:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:46:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dac22ca67391bc67ae059bdc6b4fe7cfa91d0dd9f198a7a4a48d1208814e923`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a2f008183168bde68b91f19059fb5a2932ffca93f573665a863038e54852e67`  
		Last Modified: Tue, 09 Dec 2025 20:46:34 GMT  
		Size: 491.1 KB (491114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678e16c0488e2e52183c36eea1b736af3f24966b5a4804461c92f1f18f0a94a5`  
		Last Modified: Tue, 09 Dec 2025 20:46:34 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a6fabcf69c668a047b14dc04852d4490787bd762850c1f1ddf578c4b08d6f1`  
		Last Modified: Tue, 09 Dec 2025 20:46:34 GMT  
		Size: 338.1 KB (338079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34d0088da8340135518f8acebfcebdee6b3d4f0667bb82c73681d8e1e40176c`  
		Last Modified: Tue, 09 Dec 2025 20:46:34 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03653331c81498eb8bbba739b80a7a84e502c00923c6271a4a7882501b427bd4`  
		Last Modified: Tue, 09 Dec 2025 20:46:42 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ef99eddcb3c99d6d41e25abf972704ef051d7edc7405c3cb4ddd718853d2b8`  
		Last Modified: Tue, 09 Dec 2025 20:46:34 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2966b453b83ec37aefef177b8cffa39307388910e528b23dd27a4d90394f5dd6`  
		Last Modified: Tue, 09 Dec 2025 20:46:47 GMT  
		Size: 225.6 MB (225618324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c205b61bcdd9988b3c4925dc62efca88838c55a234cc2ac8e972718fd423ff`  
		Last Modified: Tue, 09 Dec 2025 20:46:34 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
