## `openjdk:24-ea-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:f7f5843f152f4d60c2c63c25a057ce21af23adb9ac68ddbc713804377d5073aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `openjdk:24-ea-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:630e9f76dc1f26d4a93c615df19cecf72b3c62cfaed379a5df87a147e71c5c38
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2709990799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c0bb491739b61b59778220cea3d906433d65d98229f616e4ff3c7125bbbb1d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Fri, 31 Jan 2025 22:29:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 22:29:31 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:29:31 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 31 Jan 2025 22:29:37 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:29:38 GMT
ENV JAVA_VERSION=24-ea+34
# Fri, 31 Jan 2025 22:29:39 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/34/GPL/openjdk-24-ea+34_windows-x64_bin.zip
# Fri, 31 Jan 2025 22:29:39 GMT
ENV JAVA_SHA256=190d1d3c9dc679675ebbe68fc9936e9f17471cd4c161f9f7a3fefc1750bd74d7
# Fri, 31 Jan 2025 22:29:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:29:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0771ac81081ef90c3a9c07b205e3d5c2d57ab0e18f947196bab1251da098b2b9`  
		Last Modified: Fri, 31 Jan 2025 22:30:02 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3627ae475615e49d8d18cab82c9e8a8f7cb866f7b33857bcee8fef6878a182da`  
		Last Modified: Fri, 31 Jan 2025 22:30:01 GMT  
		Size: 385.6 KB (385600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb71d371d6b7e5eef4ff2b8e07f8560d0480391d9aca53433bebbade5289ea71`  
		Last Modified: Fri, 31 Jan 2025 22:30:01 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb0557d6717e22757bb3a3e2d0904b4b2515fe1a77ea0bdcbc14f41f71af55a`  
		Last Modified: Fri, 31 Jan 2025 22:30:01 GMT  
		Size: 373.8 KB (373810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb8298348de28330c9e14ea4171ad8e1a89b87cb577ca21fec611ea06413841`  
		Last Modified: Fri, 31 Jan 2025 22:30:00 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339cb8ca9a68e1070ca3f96422ad302c5d869ab936faed41b268be1b84bcc800`  
		Last Modified: Fri, 31 Jan 2025 22:30:00 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8768f16777ebf2a32a886bb9a41f85598c4b7e9461f719a91eb5bda552f23638`  
		Last Modified: Fri, 31 Jan 2025 22:30:00 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d85b73e92287f547d208c387396050797de5200579da2a1b13e62f7c6f0d49e9`  
		Last Modified: Fri, 31 Jan 2025 22:30:13 GMT  
		Size: 208.9 MB (208946003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d985f7304e5e9657a4b1784b0de2100313cebde65206cb5a31656010514c1895`  
		Last Modified: Fri, 31 Jan 2025 22:30:00 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
