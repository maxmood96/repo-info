## `openjdk:25-ea-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:2d6d5ad0a0f94d6e718b242cc91f8dbd0f3c3206b3069fede895cfd1e72fe65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `openjdk:25-ea-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull openjdk@sha256:9180feb2a5a3a91f4845d874aa654f5e9fa4a0daa0c2dbc1642e48a9de348972
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3603763931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd371fc75b9e9c6d4ecf91ce01e7ce5e1f714afc796b20e15e727d7906005faf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Wed, 09 Apr 2025 00:49:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:49:43 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:49:44 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 09 Apr 2025 00:49:51 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:49:54 GMT
ENV JAVA_VERSION=25-ea+17
# Wed, 09 Apr 2025 00:49:55 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_windows-x64_bin.zip
# Wed, 09 Apr 2025 00:49:57 GMT
ENV JAVA_SHA256=46c47281310039b4e8d7e583a1629bfb2ca08a102794c3a68d1f2051101e9f5b
# Wed, 09 Apr 2025 00:50:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:50:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4421324a5d82f1532ca4f4f8c3f3a46ea089f697096c41559aa63e8c88d9feb1`  
		Last Modified: Wed, 09 Apr 2025 00:50:24 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8999c0d868c51f88dbf27c4a0dc8aefdda18ea0356df7d3b1e34b724005b5080`  
		Last Modified: Wed, 09 Apr 2025 00:50:24 GMT  
		Size: 367.9 KB (367911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc012495130e3a0ae9399601254a6897b2d8df4f57fa6652f81f322b8b00635`  
		Last Modified: Wed, 09 Apr 2025 00:50:24 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5927f63ef491059db77b52528a506d430a2aec5116a570a6d7e8297c9aacbeef`  
		Last Modified: Wed, 09 Apr 2025 00:50:24 GMT  
		Size: 354.7 KB (354709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8011b0d24d2f2482d6e56731e1f6304cd71918afd80b989ef6d3a099afdb4114`  
		Last Modified: Wed, 09 Apr 2025 00:50:23 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cf5a60a550cb3ca7c38007a46b2487c0fb34728fb47e518a256cd2cdfaca7e`  
		Last Modified: Wed, 09 Apr 2025 00:50:23 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8269bfbec0d9583badb286a551789fd4e2ae40ca896c88adfd889a15ff935c5`  
		Last Modified: Wed, 09 Apr 2025 00:50:23 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:985d3ab8c70214ed52d5c08e86428092dc1bd752730d25141f4a132231b3ea60`  
		Last Modified: Wed, 09 Apr 2025 00:50:37 GMT  
		Size: 208.4 MB (208354054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352880e1f5682a7be7e7b95465f692e5435848797c12ebb618719a0b1d67f9fe`  
		Last Modified: Wed, 09 Apr 2025 00:50:23 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
