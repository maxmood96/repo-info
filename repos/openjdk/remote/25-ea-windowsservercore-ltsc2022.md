## `openjdk:25-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:827c5581d517d3d5e816e50043007b134a6a131a3fb85c83194a21c510c87908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `openjdk:25-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull openjdk@sha256:7926e68393a0a88ed64275f9619f19dd5d894ed86167702e0068b9fdae3ca8d5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2482417283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0281a2ce8bf29fdd475cb4eb78f105c852316bc6d686f0039c5718d25125aed0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Fri, 25 Apr 2025 21:54:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 25 Apr 2025 21:54:24 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 25 Apr 2025 21:54:25 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 25 Apr 2025 21:54:31 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 25 Apr 2025 21:54:31 GMT
ENV JAVA_VERSION=25-ea+20
# Fri, 25 Apr 2025 21:54:32 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/20/GPL/openjdk-25-ea+20_windows-x64_bin.zip
# Fri, 25 Apr 2025 21:54:33 GMT
ENV JAVA_SHA256=189b22f424bd7f7ef01de23f6e41fd183bc3b28da7db090dacba784054fe1f43
# Fri, 25 Apr 2025 21:54:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 25 Apr 2025 21:54:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78ca831e6fd2c4d3273ce91d60d3fcce010e154a3d4895e5fdacb5c3736c55e`  
		Last Modified: Fri, 25 Apr 2025 21:54:56 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6669f0f6bb1e83a15b05ece8feedcc5c3a9f93741c3e2462717f24739bbd99f`  
		Last Modified: Fri, 25 Apr 2025 21:54:56 GMT  
		Size: 373.1 KB (373107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b6f07b768aff9f2088e560a3fccb74b07f59c6321c9678f720b0e44a940166`  
		Last Modified: Fri, 25 Apr 2025 21:54:56 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f124f3b5f9b5948dae4a149f09c244567b108cc233541238bc9a72199e1ca5`  
		Last Modified: Fri, 25 Apr 2025 21:54:56 GMT  
		Size: 359.6 KB (359623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f95b25d0022835734f770cff22c4a522e9a6cacadf0b96d3ad4fb4d81bb58b`  
		Last Modified: Fri, 25 Apr 2025 21:54:55 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53d4bf7d9bade25ff02cc9f6a740aae65b3c4de25c9183a04fe482e3d741386`  
		Last Modified: Fri, 25 Apr 2025 21:54:55 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289816406037b43f59be21f45023fc6f5a18d84a00c17ce49c50ae53743fd011`  
		Last Modified: Fri, 25 Apr 2025 21:54:55 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8fe7f28ac1e3dc4125430cc7091eaf7478a28fbc069d9f86d1dd8bda77662e2`  
		Last Modified: Fri, 25 Apr 2025 21:55:06 GMT  
		Size: 208.1 MB (208094291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b21a81b08aafb65c68783286df7238a7a8c70e30d9e2686faf36465af11e4ae`  
		Last Modified: Fri, 25 Apr 2025 21:54:55 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
