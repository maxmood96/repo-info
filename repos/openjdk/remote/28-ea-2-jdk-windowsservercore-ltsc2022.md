## `openjdk:28-ea-2-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:ab761fb193500564a84bcfe11f0a593c3d9092c6284757cf540445ad3e6f46f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `openjdk:28-ea-2-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull openjdk@sha256:ff59f80eb5416cf46033891b49726625aac19b2ae206d2a877a437874eef6f73
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2356923873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f120e7dceb6b0de1dcae31f834f29e4a9199cc9b25a41314f83c9bc04c5aeab`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 16 Jun 2026 23:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Jun 2026 23:39:13 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 16 Jun 2026 23:39:14 GMT
ENV JAVA_HOME=C:\openjdk-28
# Tue, 16 Jun 2026 23:39:21 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 16 Jun 2026 23:39:22 GMT
ENV JAVA_VERSION=28-ea+2
# Tue, 16 Jun 2026 23:39:23 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk28/2/GPL/openjdk-28-ea+2_windows-x64_bin.zip
# Tue, 16 Jun 2026 23:39:24 GMT
ENV JAVA_SHA256=6e0811bf75540123fa28845352ebc400893f45c2b1ad8bedcf7837395fce7e5e
# Tue, 16 Jun 2026 23:39:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 16 Jun 2026 23:39:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2bd52046d8de3425deb30c353fd410e1f7e2f30ab0079e8a5a1e5da69227c3`  
		Last Modified: Tue, 16 Jun 2026 23:39:59 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320f8fbe718f637b6dfbb24e5a6b6a11f17cdcd75cd4e795447909dc6f436814`  
		Last Modified: Tue, 16 Jun 2026 23:40:00 GMT  
		Size: 503.0 KB (503046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f46c3a74f1519223a1dd7e69709acdb809643ed60eabf9051dfeb9c3315954`  
		Last Modified: Tue, 16 Jun 2026 23:39:59 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccce64e30b0b795abb8456e9f4b2e764135161ad1ef4b2c766e9d59d3d9de9e`  
		Last Modified: Tue, 16 Jun 2026 23:39:59 GMT  
		Size: 352.2 KB (352234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89971b99667cb450c91422376a831a740e26eb0675b620ac3abc988d9dc1b8f1`  
		Last Modified: Tue, 16 Jun 2026 23:39:57 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58e3f24cba59a91e25078d5cf65f974683b35c3bd99675b3096abafe001dd37`  
		Last Modified: Tue, 16 Jun 2026 23:39:58 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f221e07f2778a05cf0ea6bfac2624a7a91902141924209218204a6f4d376a2`  
		Last Modified: Tue, 16 Jun 2026 23:39:57 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5177dad8097483c5e6c8b26c1003de199205e047821800b96f7a8a452029ecb0`  
		Last Modified: Tue, 16 Jun 2026 23:40:14 GMT  
		Size: 223.9 MB (223935170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e2b8512b52b2583ade435eb3b75d25231e10082a73fdc812d728241669bbf2`  
		Last Modified: Tue, 16 Jun 2026 23:39:57 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
