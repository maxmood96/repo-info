## `openjdk:27-ea-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:d9efb0edf8821e4dfa43675d6753226c3fed4ffec6fb3d5414bf131d12ae2fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7462; amd64

### `openjdk:27-ea-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.7462; amd64

```console
$ docker pull openjdk@sha256:5a8bb76de191c98e99d767fc10a71c6b58ae564626b9b6b37f4a62a5cd773284
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3478209619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a8c055570902eb8754590237b349f665fc4415796dd595adda8aaf6d8aa80ee`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Tue, 16 Dec 2025 00:18:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Dec 2025 00:19:01 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 16 Dec 2025 00:19:01 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 16 Dec 2025 00:19:07 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 16 Dec 2025 00:19:08 GMT
ENV JAVA_VERSION=27-ea+2
# Tue, 16 Dec 2025 00:19:08 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/2/GPL/openjdk-27-ea+2_windows-x64_bin.zip
# Tue, 16 Dec 2025 00:19:10 GMT
ENV JAVA_SHA256=486eb3681d48770501631da706141ae22a0bc408cb4899e2370656479dd8ebfd
# Tue, 16 Dec 2025 00:19:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 16 Dec 2025 00:19:32 GMT
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
	-	`sha256:2d046c790b9cc12e8864e25e14576fe17199d8345da2e286637151050025d41f`  
		Last Modified: Tue, 16 Dec 2025 00:36:58 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a601a6f0e927b213e1b9aaf378f190afe9cc50e89a142f6270f5c44957a4df69`  
		Last Modified: Tue, 16 Dec 2025 00:36:58 GMT  
		Size: 401.2 KB (401215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767a55327600cbb242fbf770846eff66b8cf57d2c135d237753e4345f615857b`  
		Last Modified: Tue, 16 Dec 2025 00:36:58 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a810c35701a0e65c01816224df9bdf353b0af9a331fee8709ba563c6f68b6cf`  
		Last Modified: Tue, 16 Dec 2025 00:36:58 GMT  
		Size: 384.8 KB (384818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:763e67627c5e30698bc80d63134d7935d33fcd8af37af0df6cbacf6f7e3e8f70`  
		Last Modified: Tue, 16 Dec 2025 00:36:58 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d38c27d3fff8f3c07b56b754da6224ab25672dffa5b6b53f122d61a1e99aa7a`  
		Last Modified: Tue, 16 Dec 2025 00:36:58 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68518b6718f1e27ba94238ef5748fca75e66e3a725a6e69e55d6ac28a266bd09`  
		Last Modified: Tue, 16 Dec 2025 00:36:58 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff02e8934e9d035da10f423d921ed9ff9762f83c870b06c8f34586c396b1f048`  
		Last Modified: Tue, 16 Dec 2025 00:39:29 GMT  
		Size: 224.3 MB (224295317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6b3bacc83cc0c0c0bea70e58c5d933beb95a9adb4aa490890f2bfa3ad4205a`  
		Last Modified: Tue, 16 Dec 2025 00:36:58 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
