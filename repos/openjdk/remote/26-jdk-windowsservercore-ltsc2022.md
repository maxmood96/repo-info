## `openjdk:26-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:cb986763eea7cdf297c872e52bbd94463d59306db27d3d8e475bde6aee43ac8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `openjdk:26-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull openjdk@sha256:97343f988df496cd0efe696bdd7a1efaa075669764447ea4b61870244268337e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2504453667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a5738284ed6d6b75ea7bbdd1f7c866ca99c40956edf687112f8a6c7ff7d911`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Mon, 13 Oct 2025 18:21:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 13 Oct 2025 18:22:26 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 13 Oct 2025 18:22:27 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 13 Oct 2025 18:22:34 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 13 Oct 2025 18:22:35 GMT
ENV JAVA_VERSION=26-ea+19
# Mon, 13 Oct 2025 18:22:36 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_windows-x64_bin.zip
# Mon, 13 Oct 2025 18:22:37 GMT
ENV JAVA_SHA256=b31dc1d0afdaba4c6b7a399e0a932fb1a4f5a61e7624aaad8ca40b85400f966a
# Mon, 13 Oct 2025 18:23:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 13 Oct 2025 18:23:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Thu, 09 Oct 2025 10:32:05 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bb7dfcb21f637059e920895867272f6b5844269335225d912fd2c1c1f672f2`  
		Last Modified: Mon, 13 Oct 2025 18:34:23 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b602b2ce8095b05453a05481e04cee3f1320a02e300e093bae790d5abb11c62`  
		Last Modified: Mon, 13 Oct 2025 18:34:23 GMT  
		Size: 369.3 KB (369252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e36f72e2357a8545af99a74fa42b99190d692e240780234c476b7f9119f6cb`  
		Last Modified: Mon, 13 Oct 2025 18:34:23 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88770b40d9bfe1cc8d660c447d682003eaebbdf9dd7e06a9a1d10081bb0e4bec`  
		Last Modified: Mon, 13 Oct 2025 18:34:23 GMT  
		Size: 344.6 KB (344626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb606e0f0e306a112a7ae303c544c7c823c07ef6578f33d8a05554d38cc87560`  
		Last Modified: Mon, 13 Oct 2025 18:34:23 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3521842abf0442cb29c50df890d8cbee7eea5c1db9607ad2fde440e49e915f00`  
		Last Modified: Mon, 13 Oct 2025 18:34:23 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f868c3df2262bc1d2b6da516738171320a0c5e33aab40e7aee720df6942bf9ee`  
		Last Modified: Mon, 13 Oct 2025 18:34:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2818a4bbd44a88c3d895fc3fb6d2a27eb79548c70a0e09d040e3b757fa29015`  
		Last Modified: Mon, 13 Oct 2025 20:18:21 GMT  
		Size: 221.6 MB (221586912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ac1aee8213cc281f1bc814ebe3df548df4545336d38822dc56e6ae3e60bbfe`  
		Last Modified: Mon, 13 Oct 2025 18:34:23 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
