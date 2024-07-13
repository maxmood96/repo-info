## `openjdk:23-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:f81d993d56f57e47309ac3851babe92a6ce94c86bee062032d7c1ab70db4d0ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `openjdk:23-windowsservercore-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull openjdk@sha256:3610b7fea5f423b9172d83a8ca638462d58e5f1d72e0662ca95c601ddca33b00
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2445733678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:323f9a364646f0f49617668117e43a9444200f938b18526177ac02263b9a87f7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Fri, 12 Jul 2024 22:07:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Jul 2024 22:08:23 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 12 Jul 2024 22:08:24 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 12 Jul 2024 22:08:44 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 12 Jul 2024 22:08:45 GMT
ENV JAVA_VERSION=23-ea+31
# Fri, 12 Jul 2024 22:08:46 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/31/GPL/openjdk-23-ea+31_windows-x64_bin.zip
# Fri, 12 Jul 2024 22:08:46 GMT
ENV JAVA_SHA256=7894a87e50c30dfa4be1f1432dfb289c4de40e1c0fd447b8f4b5fce3141e6615
# Fri, 12 Jul 2024 22:09:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 12 Jul 2024 22:09:25 GMT
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
	-	`sha256:64e038a148c7feb7f6010c1a044eab9010d7366ab1fb7354bf3b1c47a5a899c5`  
		Last Modified: Fri, 12 Jul 2024 22:09:32 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a09613aba4fe06f7a33a4835642da64c9046a3ba825deaf232d6ff53ebd87f`  
		Last Modified: Fri, 12 Jul 2024 22:09:33 GMT  
		Size: 499.5 KB (499451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c636eb003f485953497b0c84c27688c71b18f764c6609c1546aabeff7347395`  
		Last Modified: Fri, 12 Jul 2024 22:09:32 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181510fa1de9a60c846800436a088f4d2cb5934c9175973eaa381e31122d28c8`  
		Last Modified: Fri, 12 Jul 2024 22:09:32 GMT  
		Size: 351.3 KB (351272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423b6a3d8d9b45b5894ac877a42feccabc49fbf7ed8ce3bab9864501e9a182e0`  
		Last Modified: Fri, 12 Jul 2024 22:09:30 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44444c0cd7387445289886fb4133a979f4cd09dd206dc4b2b7af4ff966ed64c`  
		Last Modified: Fri, 12 Jul 2024 22:09:30 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2291c13bd05a63826b47b0ee530a041dccf8f00fc1bbbcf3f077a45b83e5c37a`  
		Last Modified: Fri, 12 Jul 2024 22:09:30 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71d5824591b9663c45a15dc762c052a8e43d1fe7365b96439431495da924a9f`  
		Last Modified: Fri, 12 Jul 2024 22:09:41 GMT  
		Size: 206.4 MB (206445751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35fd2491ff21be1bde2b47a997dcbde2488df01ebea2aaa7771668517d82b08c`  
		Last Modified: Fri, 12 Jul 2024 22:09:30 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
