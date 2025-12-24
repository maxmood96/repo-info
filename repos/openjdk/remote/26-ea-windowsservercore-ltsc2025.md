## `openjdk:26-ea-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:547d29cb9d87f8571e2413477e123bbf0c826f62bf77cf604c208df323449838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7462; amd64

### `openjdk:26-ea-windowsservercore-ltsc2025` - windows version 10.0.26100.7462; amd64

```console
$ docker pull openjdk@sha256:86083ccc915a5136eeaa49625bcdb6b799b2757a1e4bd789c0957af220cc4265
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3478205670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0cd22d1e381e913d96c3381d742ceff25c743ba8457b69142c2025a643efb56`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Wed, 24 Dec 2025 05:15:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Dec 2025 05:16:54 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 24 Dec 2025 05:16:55 GMT
ENV JAVA_HOME=C:\openjdk-26
# Wed, 24 Dec 2025 05:17:00 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 24 Dec 2025 05:17:00 GMT
ENV JAVA_VERSION=26-ea+29
# Wed, 24 Dec 2025 05:17:01 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_windows-x64_bin.zip
# Wed, 24 Dec 2025 05:17:02 GMT
ENV JAVA_SHA256=901386b7c2b8f4a23a6158eddfca969dabb4acec8359c9861f538ea3873cf53d
# Wed, 24 Dec 2025 05:17:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 24 Dec 2025 05:17:31 GMT
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
	-	`sha256:f0dc8f2b08258837002d7692fa1e460a207e837b1bd69e7717399b8b4f1a272b`  
		Last Modified: Wed, 24 Dec 2025 05:35:05 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4683a72ac86c6950ef5dbd13374ab49c0dc2f4f796a7890c390ffb8348f9c4ca`  
		Last Modified: Wed, 24 Dec 2025 05:35:08 GMT  
		Size: 413.1 KB (413061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2756407d710233d501b014538add3c82b4fe283aca3ea4e535644f09fcc35cc3`  
		Last Modified: Wed, 24 Dec 2025 05:35:05 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4683e47f54aff9dad045e8581d4c6c1604e416aec9f89cb3d502b677b759d49`  
		Last Modified: Wed, 24 Dec 2025 05:35:05 GMT  
		Size: 393.6 KB (393618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8644a2ca6a5c3e3f394c1a35206dcf2c0f6f3c1b3d6f4f8d33f34eb11a69f49b`  
		Last Modified: Wed, 24 Dec 2025 05:35:05 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425b3ee4384b175bc62a59ee2c208fa53efb354318f416d26a754dacaff2dc43`  
		Last Modified: Wed, 24 Dec 2025 05:35:05 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b222d19899124e8b1d7df2db9771e8f2743047ff468248fbc028c422afe3f45d`  
		Last Modified: Wed, 24 Dec 2025 05:35:05 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce52c9540f472249fcfc14f7d766b8a226b648a5f8b877de2e65f52ca30e773`  
		Last Modified: Wed, 24 Dec 2025 05:35:28 GMT  
		Size: 224.3 MB (224270674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6428464b7fd1c585954568d95e59c4da27015ab489a5925e81607458ad015f69`  
		Last Modified: Wed, 24 Dec 2025 05:35:06 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
