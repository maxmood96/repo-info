## `openjdk:26-ea-31-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:985317a53e1aa13929e3b65436703c471ec5e748d7e01f0e0c96ed7f8c4542fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `openjdk:26-ea-31-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull openjdk@sha256:ce0b827ebd44a5b026ddf80b7a7cfd9a77fd19355167e7f21e7ade1f94d4a606
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1720956095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65204a8b19e20457d1ddee04404073cb692931d100e60d5e084678dc23e1b26e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 20 Jan 2026 18:49:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 20 Jan 2026 18:50:30 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 20 Jan 2026 18:50:31 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 20 Jan 2026 18:50:37 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 20 Jan 2026 18:50:38 GMT
ENV JAVA_VERSION=26-ea+31
# Tue, 20 Jan 2026 18:50:38 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/31/GPL/openjdk-26-ea+31_windows-x64_bin.zip
# Tue, 20 Jan 2026 18:50:40 GMT
ENV JAVA_SHA256=729237a33f3f431285ea2d0a8ec5668440acc285e6f484be1c7c17b26ccec761
# Tue, 20 Jan 2026 18:51:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 20 Jan 2026 18:51:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea386d3f231cd51d65f90cee89c9ac8d16f1a31939e14e985fa6a726457dbcd`  
		Last Modified: Tue, 20 Jan 2026 19:01:31 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5adc18c3e4b56bd0ce5625ed042a3a8dffa7980ecf1d809ad3df6db462a708b6`  
		Last Modified: Tue, 20 Jan 2026 19:01:00 GMT  
		Size: 501.6 KB (501566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de92f5a3063c5cb293480b09697bd0db435fe1a8a57e70bf20681dde91b30268`  
		Last Modified: Tue, 20 Jan 2026 19:01:00 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265c9bc1893bac919700fd36e2701bdc138c6fd1dbf0da3430984aba4ae0a860`  
		Last Modified: Tue, 20 Jan 2026 19:01:00 GMT  
		Size: 398.2 KB (398203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e614afd727846af505bc9b3ae096e915de2e6cb07ec2040372e6fe9cf9ea82b`  
		Last Modified: Tue, 20 Jan 2026 18:51:12 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a9c630391b95637698a76a0b179ddcbd3c8b3e0d4f07eea2a4fbd0eae38e26`  
		Last Modified: Tue, 20 Jan 2026 19:01:01 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b82e1c4e22f87360371b81ed6d8df3bcf2830d95cf30a1d00ace75b15291bab`  
		Last Modified: Tue, 20 Jan 2026 21:02:28 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e4b73034748bd1ec1c33aeb210f02d6a6fd166a26376e53740c9d55c5ad55d`  
		Last Modified: Tue, 20 Jan 2026 18:51:28 GMT  
		Size: 224.3 MB (224288154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f664962111eaea8530176b74ff3457b3a8e7b8579c1c3b50cad64a8a6a8b54`  
		Last Modified: Tue, 20 Jan 2026 19:01:43 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
