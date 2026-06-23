## `openjdk:28-ea-3-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:6ab5c5a9a12d67b90750df90a1f4f1221e6cc786a90235d0936e75b44f1adb21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `openjdk:28-ea-3-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull openjdk@sha256:3e6b42f6d5dd7a4c5bcd05a477e2dfe8d9f4a9c5bc01e7bb7fa3f6f2c3186537
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2504376329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234016c8b9352367def9d18c7a2e11f71c87068fb321ff9087e38563882dee1c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Mon, 22 Jun 2026 22:45:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 22 Jun 2026 22:46:37 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 22 Jun 2026 22:46:38 GMT
ENV JAVA_HOME=C:\openjdk-28
# Mon, 22 Jun 2026 22:46:43 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 22 Jun 2026 22:46:44 GMT
ENV JAVA_VERSION=28-ea+3
# Mon, 22 Jun 2026 22:46:44 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_windows-x64_bin.zip
# Mon, 22 Jun 2026 22:46:45 GMT
ENV JAVA_SHA256=ea552c7a26368ac534c4cae4c56666b9efdf9ad421575f4281dfbb81c4185fa3
# Mon, 22 Jun 2026 22:47:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 22 Jun 2026 22:47:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e21b3ffd131aebaf9a247c168c7a4bae55db9b2cb6a9637cb191de044c9b48`  
		Last Modified: Mon, 22 Jun 2026 22:47:29 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d154b2fb13125248b6824ca5bbac20dbc72569fd24c3f39923c8b94c5c5518`  
		Last Modified: Mon, 22 Jun 2026 22:47:29 GMT  
		Size: 396.7 KB (396668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60214b62b23eda3dbdee4f30fc526bebffc8f7343d75d1d93207073070a12e7`  
		Last Modified: Mon, 22 Jun 2026 22:47:29 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed00fbb477dcb144f294f11ae189535d11af4c8d6f4d32fb0a5b1820838f45a`  
		Last Modified: Mon, 22 Jun 2026 22:47:29 GMT  
		Size: 385.6 KB (385571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45ba46607ef44d128ef809801d331513843bc2d6b5a606062a7b2e43aea23d0`  
		Last Modified: Mon, 22 Jun 2026 22:47:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa1a7a973552e88dcc2b8732ccf61261f545d9cedfa7c3aaf598e24cb2937a7`  
		Last Modified: Mon, 22 Jun 2026 22:47:27 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1923fbbb22e56bf8f4658f996c2d5d08dabecb94facfdda3d94fa5a1f21cf7e2`  
		Last Modified: Mon, 22 Jun 2026 22:47:27 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85818f15434e77788ecc94972719517ea56a3cb9cc54a32c0312238679fba307`  
		Last Modified: Mon, 22 Jun 2026 22:47:42 GMT  
		Size: 224.4 MB (224443363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37b047fc093b605d1589f468c2a558047e034a137685b0fda9337e9696cb199`  
		Last Modified: Mon, 22 Jun 2026 22:47:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
