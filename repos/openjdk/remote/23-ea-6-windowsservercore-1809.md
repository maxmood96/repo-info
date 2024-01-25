## `openjdk:23-ea-6-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:0eea27024d846498f6d1419e8b58ec042daf29c383f3d52010fe62b53250a52d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `openjdk:23-ea-6-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull openjdk@sha256:327f80367265d29b250e53d6cb70bac461c90e489223db928e1a62dfbea8499e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2268404914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf1f20efd8000a494ce8f044d591aa3efff0fe75752d8cc12e87a402da74a9a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 24 Jan 2024 20:49:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Jan 2024 20:52:09 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 24 Jan 2024 20:52:10 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 24 Jan 2024 20:52:32 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 24 Jan 2024 20:52:32 GMT
ENV JAVA_VERSION=23-ea+6
# Wed, 24 Jan 2024 20:52:33 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/6/GPL/openjdk-23-ea+6_windows-x64_bin.zip
# Wed, 24 Jan 2024 20:52:33 GMT
ENV JAVA_SHA256=7a0ae9736e1fa5d2e341e863dc04057af1ce6525eb3ca98932584a2fb4058837
# Wed, 24 Jan 2024 20:53:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 24 Jan 2024 20:53:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c7d66208680345c6c4ca1a507d40e48a14d7f8d0891b7c7d3a67197760935`  
		Last Modified: Wed, 24 Jan 2024 20:53:29 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0128e04e330b39ab8310cb82ae598acf3ea5d879bb046a03dd77fc4150523dc3`  
		Last Modified: Wed, 24 Jan 2024 20:53:30 GMT  
		Size: 495.8 KB (495776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6790756ef4953e3e763a580f0a1cd0bc0ca4903981f18f21516fc3ec5377875a`  
		Last Modified: Wed, 24 Jan 2024 20:53:29 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a77c5a052f5c5299336afab206ccea104481bcc2f643b05b3487de79a0b6b2`  
		Last Modified: Wed, 24 Jan 2024 20:53:29 GMT  
		Size: 342.9 KB (342931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d8ee20a5fca357826c851cc731094b73901b68179f95ad4b8386b023b3a051`  
		Last Modified: Wed, 24 Jan 2024 20:53:27 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e196d81eeb31a9691a66028b21861b66bd715715a41cf1dc8db930fc10913d24`  
		Last Modified: Wed, 24 Jan 2024 20:53:27 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817920aaa6fab4583c5e90ac211e6d732d54854a93435e945aa2ed8e9bbcfff5`  
		Last Modified: Wed, 24 Jan 2024 20:53:27 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6431f6a8893d182576a88426872d97dabe0bf48c4debbc5ae1eb243b389c61bd`  
		Last Modified: Wed, 24 Jan 2024 20:53:38 GMT  
		Size: 197.8 MB (197835921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad96668ba6bc59a1d859bdcd424cf0d28b8a294e3bd8e284ce6ecd8e940f2083`  
		Last Modified: Wed, 24 Jan 2024 20:53:27 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
