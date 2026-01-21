## `openjdk:26-ea-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:a3f00c7717dcaa341995b7ef06061293d54013aca00f7c2c82e6a12903a6ee7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `openjdk:26-ea-jdk-windowsservercore` - windows version 10.0.26100.32230; amd64

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
		Last Modified: Tue, 13 Jan 2026 18:56:33 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea386d3f231cd51d65f90cee89c9ac8d16f1a31939e14e985fa6a726457dbcd`  
		Last Modified: Tue, 20 Jan 2026 19:01:31 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5adc18c3e4b56bd0ce5625ed042a3a8dffa7980ecf1d809ad3df6db462a708b6`  
		Last Modified: Tue, 20 Jan 2026 18:51:14 GMT  
		Size: 501.6 KB (501566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de92f5a3063c5cb293480b09697bd0db435fe1a8a57e70bf20681dde91b30268`  
		Last Modified: Tue, 20 Jan 2026 19:01:00 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265c9bc1893bac919700fd36e2701bdc138c6fd1dbf0da3430984aba4ae0a860`  
		Last Modified: Tue, 20 Jan 2026 18:51:14 GMT  
		Size: 398.2 KB (398203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e614afd727846af505bc9b3ae096e915de2e6cb07ec2040372e6fe9cf9ea82b`  
		Last Modified: Tue, 20 Jan 2026 19:01:05 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a9c630391b95637698a76a0b179ddcbd3c8b3e0d4f07eea2a4fbd0eae38e26`  
		Last Modified: Tue, 20 Jan 2026 19:01:01 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b82e1c4e22f87360371b81ed6d8df3bcf2830d95cf30a1d00ace75b15291bab`  
		Last Modified: Tue, 20 Jan 2026 18:51:12 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e4b73034748bd1ec1c33aeb210f02d6a6fd166a26376e53740c9d55c5ad55d`  
		Last Modified: Tue, 20 Jan 2026 19:24:30 GMT  
		Size: 224.3 MB (224288154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f664962111eaea8530176b74ff3457b3a8e7b8579c1c3b50cad64a8a6a8b54`  
		Last Modified: Tue, 20 Jan 2026 19:01:43 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-jdk-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull openjdk@sha256:68e712fe9d9f255d840a39517a333e20f21be786957b0ad891cba0264c033627
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2060728152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e660f6e6eef38aa391ea8c727cb06a84bc179406f51f0819c2bc69f642e1f918`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 20 Jan 2026 18:49:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 20 Jan 2026 18:50:44 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 20 Jan 2026 18:50:45 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 20 Jan 2026 18:50:52 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 20 Jan 2026 18:50:53 GMT
ENV JAVA_VERSION=26-ea+31
# Tue, 20 Jan 2026 18:50:53 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/31/GPL/openjdk-26-ea+31_windows-x64_bin.zip
# Tue, 20 Jan 2026 18:50:55 GMT
ENV JAVA_SHA256=729237a33f3f431285ea2d0a8ec5668440acc285e6f484be1c7c17b26ccec761
# Tue, 20 Jan 2026 18:51:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 20 Jan 2026 18:51:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:28:58 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3380b620c58c596f1609e5dfd5ce2eb7bb472a207cd9fee48adb79d268f61ebb`  
		Last Modified: Tue, 20 Jan 2026 19:00:33 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdd76be044f19871712460cce44c0a30841d6d82ba5daff63fcf776456fa047`  
		Last Modified: Tue, 20 Jan 2026 19:00:33 GMT  
		Size: 491.1 KB (491115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c3ceaf24cc236921faa6f5f624de38ca2c792fc9cc91fbc99d78f24051df1c2`  
		Last Modified: Tue, 20 Jan 2026 19:24:23 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27683916210a6564d9ee9481fa88cbe40087242053fec9887a44f9dabb59ac74`  
		Last Modified: Tue, 20 Jan 2026 18:52:00 GMT  
		Size: 335.8 KB (335782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce40c409d8822ddf320b4553138be4933ffe1adef0db4c71eb81520130cf76e4`  
		Last Modified: Tue, 20 Jan 2026 18:51:58 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f7ed04891cc3f7c9563502232568866c4ab0b71587f558b9e74f4871b9c98d`  
		Last Modified: Tue, 20 Jan 2026 19:24:15 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8e2805cd215b737f6ef76acab716ef23c2686524b91ae92387442b6959494c`  
		Last Modified: Tue, 20 Jan 2026 19:00:36 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447bc5c2b8767cf475adeb8d6fcf1ff33f62366c247acfc66821bb242133b249`  
		Last Modified: Tue, 20 Jan 2026 19:09:30 GMT  
		Size: 224.2 MB (224234205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03abc903f6224acfca3d797e41a69bb7406c077299b9ee31cf4f24ed0c6b1391`  
		Last Modified: Tue, 20 Jan 2026 19:00:33 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
