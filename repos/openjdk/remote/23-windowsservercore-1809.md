## `openjdk:23-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:884a33e7704c65ce3e4792e88b7bbda422f3d5a59429a44df214d29c639e8cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `openjdk:23-windowsservercore-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull openjdk@sha256:5924ed5f907b8d3f828db662a8414a59738896bef6bb8cef46113113266535c3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2445724389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90319424db6042c11f03d8d0bc8a02125b474885fc4b69a1594caf3bc29d341a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Mon, 22 Jul 2024 20:59:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 22 Jul 2024 21:02:07 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 22 Jul 2024 21:02:07 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 22 Jul 2024 21:02:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 22 Jul 2024 21:02:34 GMT
ENV JAVA_VERSION=23-ea+33
# Mon, 22 Jul 2024 21:02:34 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/33/GPL/openjdk-23-ea+33_windows-x64_bin.zip
# Mon, 22 Jul 2024 21:02:35 GMT
ENV JAVA_SHA256=b187293e4a2d22e9975c77c2a9fa5ac548e60fa92ac6f5a7185f697ab295d04f
# Mon, 22 Jul 2024 21:03:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 22 Jul 2024 21:03:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4492dbbb683465899fe47f991ab8bc2cd18a531a1b14ec578052b07941231b`  
		Last Modified: Mon, 22 Jul 2024 21:03:32 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0378b5b9361e1091fd3bdbc9ff9c378f6f3a1b81b8008f689dcf9afeed331196`  
		Last Modified: Mon, 22 Jul 2024 21:03:32 GMT  
		Size: 500.5 KB (500497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de3de2537607174ee5a0108307c7d0c2d4bcf6a0531ddacfc9c6635fcc752ef`  
		Last Modified: Mon, 22 Jul 2024 21:03:32 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed79ac91669a0f33a6fc74482d34e06131b3c09222018e01528678ec0d00d6fe`  
		Last Modified: Mon, 22 Jul 2024 21:03:32 GMT  
		Size: 344.4 KB (344398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779a0e43611bb7ed1193fe22fcf0d6a7c8fc0ccbee755268d8d1e73d2d355b77`  
		Last Modified: Mon, 22 Jul 2024 21:03:31 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1723be0c21485f2fa099a6d4f5413badf5540851a351fe6b0b2e802e0ccfce07`  
		Last Modified: Mon, 22 Jul 2024 21:03:31 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:decd092d07e5a2d6b72133a3cebd801af5a09d80a1d17fd61f91d3cea3e47f30`  
		Last Modified: Mon, 22 Jul 2024 21:03:31 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba141e4cf2e5dd3382645778894d2c11746b25fdba9d1f5a02143a7f180c384`  
		Last Modified: Mon, 22 Jul 2024 21:03:41 GMT  
		Size: 206.4 MB (206442212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6738b5184765ce4589392d0d0e4634861521d513f099b720e154b198a1d064`  
		Last Modified: Mon, 22 Jul 2024 21:03:31 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
