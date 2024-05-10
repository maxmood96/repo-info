## `openjdk:23-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:83756d1f621eb15f7ea9ec9b78ed46bd54934498d15b2ebb39c8b3ab437981c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `openjdk:23-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull openjdk@sha256:ebfc074de73d0bfec1142b598cfad0bc07df285f713aabc0f299c947d73f5c82
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2370081929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18942407845b9dfab552f2ea7e04d79950be4d3d3ebb3f0dc2b7fb84e6ec7dfe`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Fri, 10 May 2024 00:51:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 10 May 2024 00:53:55 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 10 May 2024 00:53:56 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 10 May 2024 00:54:21 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 10 May 2024 00:54:22 GMT
ENV JAVA_VERSION=23-ea+22
# Fri, 10 May 2024 00:54:22 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/22/GPL/openjdk-23-ea+22_windows-x64_bin.zip
# Fri, 10 May 2024 00:54:23 GMT
ENV JAVA_SHA256=a849b0c4f58cb28b02e6c43660886859ce8678d18224b4038ad69c1e3ead6249
# Fri, 10 May 2024 00:55:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 10 May 2024 00:55:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0446aa553e9377dd0f788c399d92e48231bb3e17aea06be5705f5ba1edaac31`  
		Last Modified: Fri, 10 May 2024 00:55:20 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83fac9d0a3c668b46ac3a5055fc4a902bce37bd90f3d3fe944ebba88a4d335b`  
		Last Modified: Fri, 10 May 2024 00:55:20 GMT  
		Size: 503.7 KB (503703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff81dc76ccf3b2fbff999c2b21ff47447a0a4f3075c67729869117e84c810b93`  
		Last Modified: Fri, 10 May 2024 00:55:20 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da86b1bec0f90129a69f7d189fc632168e95041ecde73dad9f9ada7a54eb6f1`  
		Last Modified: Fri, 10 May 2024 00:55:20 GMT  
		Size: 350.5 KB (350460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a3edc5d02851bef2b7eae8c114cda4333f2e911b207fff2903aad542961f0f`  
		Last Modified: Fri, 10 May 2024 00:55:19 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab74a84f996afcb8979a7d62ea97e8c708989a9c59235699a25b9cb82e88d169`  
		Last Modified: Fri, 10 May 2024 00:55:19 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6315b9cf8192869861bbb649d5a8d9bb00118dd90be54361463733cceb71e55`  
		Last Modified: Fri, 10 May 2024 00:55:18 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cd21058285287336065c071aec50047fd75eef48fc28a7b85eb012847679c1`  
		Last Modified: Fri, 10 May 2024 00:55:29 GMT  
		Size: 204.8 MB (204792062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc207b91966e0ab95ca9d96223fd69c3c70971e63c83c012a550f04cff3ab20`  
		Last Modified: Fri, 10 May 2024 00:55:18 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
