## `openjdk:26-ea-27-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:484aaac67d3939483b6afe3d3379c8d8a06f111006d2ae8c13f35812e5c85d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7462; amd64

### `openjdk:26-ea-27-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.7462; amd64

```console
$ docker pull openjdk@sha256:3c94a3bf2bb75a1495d64cca2d1c6e11260359ff7dbcf65c5625d7283cabed9c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3479333263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c15eaadf32571cd3e3e703283ca51b40edd821ebc2e2df36ea7859595f0a37`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Tue, 09 Dec 2025 20:35:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:48:02 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:48:03 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 09 Dec 2025 20:48:08 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:48:09 GMT
ENV JAVA_VERSION=26-ea+27
# Tue, 09 Dec 2025 20:48:10 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_windows-x64_bin.zip
# Tue, 09 Dec 2025 20:48:11 GMT
ENV JAVA_SHA256=5fc8523fafe0bbe81e010d1bd57b12836c42cdd1f017e4492f67d56bde06f86a
# Tue, 09 Dec 2025 20:48:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:48:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62c64c7dc565d03eb3e9f39894e67ad9fe74d54f61e84975b3f57b9f2972a79`  
		Last Modified: Tue, 09 Dec 2025 20:45:08 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c71974a87b51cf6f3c1173d0dd549c9cd811ec8f94105839f73f41a7cbb278`  
		Last Modified: Tue, 09 Dec 2025 20:49:04 GMT  
		Size: 335.9 KB (335946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75dccdc57442bae9305519da51c85a0826dc042a40e1b069945e5871ebbcdf11`  
		Last Modified: Tue, 09 Dec 2025 20:49:04 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e64e9b7db1833188529973db2194fe400603af3bd237e0819a5513eed16bb55`  
		Last Modified: Tue, 09 Dec 2025 20:49:04 GMT  
		Size: 326.3 KB (326266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07cc06412dd9f9e6b77373717b849b33caf82ed9ce913f7c0c4b5b45e550eb4a`  
		Last Modified: Tue, 09 Dec 2025 20:49:04 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8582bfcef2f8c5a6823cd3a4e7c8c92dba150854b9e76ea7e4274f25aaca3428`  
		Last Modified: Tue, 09 Dec 2025 20:49:04 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b2e564c314fec71ac31165c3426f30f79c50a8df6f19fa448c4c90ceeb44e8`  
		Last Modified: Tue, 09 Dec 2025 20:49:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e74e314b5e1d28fe97cb517f237c65faa363da469a338106b60ec1079c9348a6`  
		Last Modified: Tue, 09 Dec 2025 20:49:15 GMT  
		Size: 225.5 MB (225542755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e66f7ecd3696ec6ed90f5e9d316b4355d40f1834ccb10726f6d106da364e01`  
		Last Modified: Tue, 09 Dec 2025 20:49:04 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
