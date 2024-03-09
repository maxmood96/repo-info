## `openjdk:23-ea-13-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:71df6ceac9dc37ec47d2ae6272a71ebe69411bf0157866ba5ba8c8aae89f0b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `openjdk:23-ea-13-jdk-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull openjdk@sha256:ea4803912b3357d5e869214394fb6214964bb17627937e1a06228a9c3a19da51
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2278854803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89fcc7d1e554cf1fa080da455ea8fa12468a36a20761555be020a55b21dc2c62`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Sat, 09 Mar 2024 01:48:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 09 Mar 2024 01:50:12 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 09 Mar 2024 01:50:13 GMT
ENV JAVA_HOME=C:\openjdk-23
# Sat, 09 Mar 2024 01:50:39 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 09 Mar 2024 01:50:40 GMT
ENV JAVA_VERSION=23-ea+13
# Sat, 09 Mar 2024 01:50:40 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/13/GPL/openjdk-23-ea+13_windows-x64_bin.zip
# Sat, 09 Mar 2024 01:50:41 GMT
ENV JAVA_SHA256=f8ee056a7c33a543e7562d171b9f032a45db3be0f5fc2ecc6d5b4eb70aaeed87
# Sat, 09 Mar 2024 01:51:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 09 Mar 2024 01:51:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0fb1c4ab3b5f4018aec84a419d625d9bb00e65291a4794a73b0b2302141fb8`  
		Last Modified: Sat, 09 Mar 2024 01:51:42 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13b3989138456a941d9731cedabe91c3fe3b8699fd095069d460872318be8040`  
		Last Modified: Sat, 09 Mar 2024 01:51:42 GMT  
		Size: 498.3 KB (498259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5e0b0ddf4893787c203d04e8424a892ae829c6244b013c7bf6070565a338f3`  
		Last Modified: Sat, 09 Mar 2024 01:51:42 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:547a339d3d9b984d376c4ebe8f5c13809023195bfe3e720ebcd4ed863715bfee`  
		Last Modified: Sat, 09 Mar 2024 01:51:42 GMT  
		Size: 352.8 KB (352751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0e90489c9281b8f1bfcdb68e91425dcb4f6302fda6e7a4b03f6223e332df00`  
		Last Modified: Sat, 09 Mar 2024 01:51:40 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ada31a7969543ed583da5b18bfa16bfff0c5dd35102e8a955efda73e2abfe5c`  
		Last Modified: Sat, 09 Mar 2024 01:51:40 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43545d2e297022472ad69d13c0d6da6e1defecc6e4887c0a309cb527972fbae`  
		Last Modified: Sat, 09 Mar 2024 01:51:40 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05a67c61a4a1e9f133d1066eaf04eda2f4d1b638df286c19f5962c4cc1dbee7`  
		Last Modified: Sat, 09 Mar 2024 01:51:51 GMT  
		Size: 197.5 MB (197547140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49ba7f4c04a2c3022fba0304cc0337a7c392aa1907b94020a10850acce9d515`  
		Last Modified: Sat, 09 Mar 2024 01:51:40 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
