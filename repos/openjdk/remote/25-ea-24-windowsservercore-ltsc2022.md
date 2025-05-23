## `openjdk:25-ea-24-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:855f94ad03888f0d335985de58d4381f79895ad0f64d7c5e2af63ef4fe154073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `openjdk:25-ea-24-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull openjdk@sha256:fcf190c415f8041fb35b4a5d8d1828874682cd86d245f908350b8e587fd58027
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2484049371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357604f9091509899cb2b7d05f936a2abb7047fad5675c371c0e0badda562b47`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Fri, 23 May 2025 20:11:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 23 May 2025 20:11:28 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 23 May 2025 20:11:28 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 23 May 2025 20:11:34 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 23 May 2025 20:11:35 GMT
ENV JAVA_VERSION=25-ea+24
# Fri, 23 May 2025 20:11:36 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_windows-x64_bin.zip
# Fri, 23 May 2025 20:11:37 GMT
ENV JAVA_SHA256=2a8b2ea51b3b0b3751867a3117e7fde1235189e6d7601f5ffdb9b9160b270bf2
# Fri, 23 May 2025 20:11:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 23 May 2025 20:11:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Tue, 13 May 2025 18:47:51 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f67237879c096267e1200856bf037f3f29aa56b28033a80f0932dd27895f082`  
		Last Modified: Fri, 23 May 2025 20:12:04 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28834b2922b677c8fd3b8da93b8710de1c2e15e7fb95e4277fdd08b2f1bf5b5e`  
		Last Modified: Fri, 23 May 2025 20:12:03 GMT  
		Size: 357.8 KB (357825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0477140b8639c611b5f6419232a874a96116bde038349af232aa52c43f761a`  
		Last Modified: Fri, 23 May 2025 20:12:03 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7610db4ab5004086ee0062d9a4dcaa3fa58be6b2d94adbd1da78dc3d0d8f72e`  
		Last Modified: Fri, 23 May 2025 20:12:03 GMT  
		Size: 345.8 KB (345787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487672f1881a7ed5cbabf7c0e710dc179fa8611168e4b83cc3bf06e5920cf4fd`  
		Last Modified: Fri, 23 May 2025 20:12:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f9e6cad41ac51225d604c82ae062af0c0857808f49372f51558b4c6cd72154`  
		Last Modified: Fri, 23 May 2025 20:12:02 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de805c3c8194da08542d957c906f5606d24570fb482796003010792a178963c`  
		Last Modified: Fri, 23 May 2025 20:12:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c638d3864bd87ed514894184ed4789df81eeaa7024f0fd79192326d2a7423c`  
		Last Modified: Fri, 23 May 2025 20:12:15 GMT  
		Size: 209.7 MB (209709936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062e5b3fc45b5eadba5bd34a424cb019549939d0bbf6c37263969021140bb156`  
		Last Modified: Fri, 23 May 2025 20:12:02 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
