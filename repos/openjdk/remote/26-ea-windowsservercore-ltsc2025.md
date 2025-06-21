## `openjdk:26-ea-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:b83e93643e69f7be60beb99eabfd09e1a12fe5ad58a3ebfce9f09b9851ea2c0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `openjdk:26-ea-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull openjdk@sha256:d357623e8379912de939e7e000b7143d3a3424b29bfceba7f4a02e21197653eb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3695831032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c82bdaae0f6e1d81e1c211010fa665875597d16059e345a090d35aa3220c495`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Sat, 21 Jun 2025 00:33:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 21 Jun 2025 00:33:30 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 21 Jun 2025 00:33:30 GMT
ENV JAVA_HOME=C:\openjdk-26
# Sat, 21 Jun 2025 00:33:37 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 21 Jun 2025 00:33:38 GMT
ENV JAVA_VERSION=26-ea+3
# Sat, 21 Jun 2025 00:33:39 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/3/GPL/openjdk-26-ea+3_windows-x64_bin.zip
# Sat, 21 Jun 2025 00:33:40 GMT
ENV JAVA_SHA256=b5728414606c8b9c7d53d32794dcd985c83d5aad7e57dec16cd8286ccdcb1aab
# Sat, 21 Jun 2025 00:34:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 21 Jun 2025 00:34:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296ca119ddbf56626b38338481409ea64f27cc5785490a313410bf7b54d844b5`  
		Last Modified: Sat, 21 Jun 2025 00:37:53 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c646a9cf7842e8f5e798c2b45c102b4f937fa2a39befa7764bdd5ddd9c3016`  
		Last Modified: Sat, 21 Jun 2025 00:37:54 GMT  
		Size: 411.6 KB (411603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae352aae3d5c7908b4cc64ff6fe4dde0350eaf0516937832afd16ac399fdf6ed`  
		Last Modified: Sat, 21 Jun 2025 00:37:54 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2daef46d64d8b835597b09cb7e2a33f46953645e048aced2797738c536a5157`  
		Last Modified: Sat, 21 Jun 2025 00:37:55 GMT  
		Size: 392.4 KB (392422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc1b3f447d2792e28a0bc25dcb5b2357011b82f3bd8cbaafdd9cfc74bbacb59`  
		Last Modified: Sat, 21 Jun 2025 00:37:55 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075dd3d16d4356c6a438f1465acf43152d0f2a4ea6fac4b180bd349eebfb9f5c`  
		Last Modified: Sat, 21 Jun 2025 00:37:55 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e625fbad7f6b0b95372893a83198785643d8aeb5b9d6ff41292f0c9a08dddd`  
		Last Modified: Sat, 21 Jun 2025 00:37:55 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250d9f29ea770b4524227e16268107a876b435c8056479c55da88816e92e101a`  
		Last Modified: Sat, 21 Jun 2025 01:08:24 GMT  
		Size: 218.8 MB (218845066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb54360876ea6776db8beb14d73eab1b6222813ce78440d87a38fc37e8e3ff1`  
		Last Modified: Sat, 21 Jun 2025 00:37:55 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
