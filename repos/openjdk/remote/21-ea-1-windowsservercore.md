## `openjdk:21-ea-1-windowsservercore`

```console
$ docker pull openjdk@sha256:7d49c8c3e0459d67617f11320e42750553ac54034ce7a4886bb5c7fe0b05f47e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1366; amd64
	-	windows version 10.0.17763.3770; amd64

### `openjdk:21-ea-1-windowsservercore` - windows version 10.0.20348.1366; amd64

```console
$ docker pull openjdk@sha256:cf43fa33c70c4e4d609e8462bcfea74e3154a0d6169f2bbf69914a4d87f71c80
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2691164974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054d8c1a2f7c0a5ec0db165addffd8616c4ac38f96ec80261c61271a88fc59c6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 09 Dec 2022 09:36:47 GMT
RUN Install update 10.0.20348.1366
# Tue, 13 Dec 2022 22:45:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Dec 2022 02:49:23 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 14 Dec 2022 02:49:24 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 14 Dec 2022 02:49:56 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 14 Dec 2022 02:49:57 GMT
ENV JAVA_VERSION=21-ea+1
# Wed, 14 Dec 2022 02:49:58 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/1/GPL/openjdk-21-ea+1_windows-x64_bin.zip
# Wed, 14 Dec 2022 02:49:59 GMT
ENV JAVA_SHA256=5a7be14bb04a1ba61d85b34818d427f7bdaa736d9947bd828b5783e64533f636
# Wed, 14 Dec 2022 02:51:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 14 Dec 2022 02:51:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a4aee932fccc1ec8135f290aca03a7c93dcc2536fc84723813ef9b95f6fd13ea`  
		Last Modified: Wed, 18 May 2022 07:59:24 GMT  
		Size: 1.5 GB (1473997635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfa20ce142ecceb471dc070d9582fff942cef447b7c8ff22f2223ffe3737c99`  
		Last Modified: Tue, 13 Dec 2022 23:54:14 GMT  
		Size: 1.0 GB (1021665190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb8b9a4ec3ca516cfaa44f64e80b1e3aaecdbde870177411ff046f81f991dd2`  
		Last Modified: Tue, 13 Dec 2022 23:51:33 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc6d0e6b431095ccd3ac842154ae597a56b82834441570a9c95689f517a56ea`  
		Last Modified: Wed, 14 Dec 2022 08:45:36 GMT  
		Size: 576.9 KB (576869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc9ff5976ac61d4db52625b68997e78b00950928dbf9331ad574ee8a6325ffc`  
		Last Modified: Wed, 14 Dec 2022 08:45:35 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f94200dbf261bdba4d1be09e454ed78de2fd3de552ee8fe393fea2716d24d619`  
		Last Modified: Wed, 14 Dec 2022 08:45:35 GMT  
		Size: 512.8 KB (512838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28f629d4b88d3e9b860bc386b9879f73c7c383940f5b4b0bb4947be421a41eb`  
		Last Modified: Wed, 14 Dec 2022 08:45:33 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d2f38968afb6b6d79f62281be7f5e2f955fbc4cbbdf29f7ef50634d6ca3165`  
		Last Modified: Wed, 14 Dec 2022 08:45:33 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e30b71bed3fbe1b5d1da89a333b47be733126a998375699e7e3e92b773ff1b3`  
		Last Modified: Wed, 14 Dec 2022 08:45:33 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b2c9ff57be176b0b9baf3d79973c53d3de3e090a279a85aef4ac473c83268b`  
		Last Modified: Wed, 14 Dec 2022 08:46:00 GMT  
		Size: 194.4 MB (194403888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f815b0bfc24227a7321bd217cf978513d7533fb9b25f7a8223546d2645e251`  
		Last Modified: Wed, 14 Dec 2022 08:45:33 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-1-windowsservercore` - windows version 10.0.17763.3770; amd64

```console
$ docker pull openjdk@sha256:404b930b407f1502d2a5ce8455215357712062b9b3d15588f5cea56274df9658
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2975581354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:477372ea4e7f2202729768f5f54c98673dad3f35e87b5c978d9791c5b186f323`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sun, 11 Dec 2022 08:04:49 GMT
RUN Install update 10.0.17763.3770
# Tue, 13 Dec 2022 22:48:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Dec 2022 02:52:45 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 14 Dec 2022 02:52:46 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 14 Dec 2022 02:54:02 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 14 Dec 2022 02:54:03 GMT
ENV JAVA_VERSION=21-ea+1
# Wed, 14 Dec 2022 02:54:04 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/1/GPL/openjdk-21-ea+1_windows-x64_bin.zip
# Wed, 14 Dec 2022 02:54:05 GMT
ENV JAVA_SHA256=5a7be14bb04a1ba61d85b34818d427f7bdaa736d9947bd828b5783e64533f636
# Wed, 14 Dec 2022 02:56:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 14 Dec 2022 02:56:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3ad73ed772f80ab7923579a55dd12fb9b6e090d1d836408d16ffd9d3dee252`  
		Last Modified: Tue, 13 Dec 2022 23:56:47 GMT  
		Size: 856.4 MB (856427878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc9debb9503ac53c2f64685982eca56ac5110ea6baf7278b27af54ab8fbc409`  
		Last Modified: Tue, 13 Dec 2022 23:54:25 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e607bf43cbd414b2f7d5b6fdfc84e9eb56c2552fe9826cffa690a9d1fd381c`  
		Last Modified: Wed, 14 Dec 2022 08:46:21 GMT  
		Size: 348.4 KB (348396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7bf9dc65d10e90b70525df57c897036594bf31ca9f3291e807694c747e7c0d`  
		Last Modified: Wed, 14 Dec 2022 08:46:21 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3efbe2a37741e8df08f14ef4454b92bc8fbabf777e000dc58fd3642794a700`  
		Last Modified: Wed, 14 Dec 2022 08:46:21 GMT  
		Size: 309.8 KB (309816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a942958520da82291c1b7875cf82971d8c4ec6d76eff28d9741ed57389ec1ac`  
		Last Modified: Wed, 14 Dec 2022 08:46:19 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9702370c7508042a2c266f698991686f46bdc7d28879ed67ec3fa021bd734a21`  
		Last Modified: Wed, 14 Dec 2022 08:46:19 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a016035acddb68059b7da610adf46dea69b87628c99d51f26af64ec274284626`  
		Last Modified: Wed, 14 Dec 2022 08:46:19 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c1c522aa1649e4801e530d41178003f6d7318af1d3dfb9e22f88daac6ff00`  
		Last Modified: Wed, 14 Dec 2022 08:46:50 GMT  
		Size: 194.2 MB (194217391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd1aa8e013bbef01d89b595e971d62ac51a056cb302140b661af73935bb1eb6`  
		Last Modified: Wed, 14 Dec 2022 08:46:19 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
