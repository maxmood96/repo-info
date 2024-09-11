## `openjdk:23-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:b7942f83d59d53d2ad4e7f955d1214cc09b68f463ca20f3ce26514549b727001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `openjdk:23-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull openjdk@sha256:0772364b67dd24d5018201895bbc9e43128e8c1612ff57fb0e0d5ac6ae6ecbe4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1669306260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7e50a177b979b8095a402bff7800bbb89ad66399b91ff333c2cca4c536fc15`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 00:04:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:04:57 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:04:57 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 11 Sep 2024 00:05:03 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:05:04 GMT
ENV JAVA_VERSION=23
# Wed, 11 Sep 2024 00:05:04 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_windows-x64_bin.zip
# Wed, 11 Sep 2024 00:05:05 GMT
ENV JAVA_SHA256=cba5013874ba50cae543c86fe6423453816c77281e2751a8a9a633d966f1dc04
# Wed, 11 Sep 2024 00:05:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:05:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa27a9cd86d0dd4857f324be7a02a5d347b325381a1d3b8c74f574406d2c6a6`  
		Last Modified: Wed, 11 Sep 2024 00:05:44 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf664b689da9d59e0cfca284211e50c1589593555465fd54dc434e21dab6e332`  
		Last Modified: Wed, 11 Sep 2024 00:05:44 GMT  
		Size: 350.3 KB (350274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03020230e9f775f7894e3c6418d3e7596a2eaea4698ce4b1bfa5bd54435d0f7`  
		Last Modified: Wed, 11 Sep 2024 00:05:44 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b51aeedb56039e441b184c557d15a6623655ab9a18748f54a516592fe9c6d96`  
		Last Modified: Wed, 11 Sep 2024 00:05:44 GMT  
		Size: 334.5 KB (334511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e02584a59171fcdd4ddc7a9f9d6e2a30c215e754873c445173126e5c8e6b780`  
		Last Modified: Wed, 11 Sep 2024 00:05:42 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93562182dd6b80378030e7a6c83ecf1194a7e06a2d6b1957eacd41062f50cf73`  
		Last Modified: Wed, 11 Sep 2024 00:05:41 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4665a20dca2ed522818a0e94965ff11a7e51a6c806fc7de5a440ea729a5895`  
		Last Modified: Wed, 11 Sep 2024 00:05:42 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f27ee42a2be57648d92f6c070aa65d7895a49112d92878ce514ad34b303a5f`  
		Last Modified: Wed, 11 Sep 2024 00:05:53 GMT  
		Size: 206.4 MB (206421297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0769d2144598e1e5eaca278528e4456090df5d379b8f3740a83788c1c62732ff`  
		Last Modified: Wed, 11 Sep 2024 00:05:42 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
