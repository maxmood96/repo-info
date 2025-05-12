## `openjdk:25-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:fa4683f907741bdc838c97e840575045ffc9f443518dfc9fd07c74fda5be30bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `openjdk:25-windowsservercore-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull openjdk@sha256:f985fb9513b2f53e0699de535eb41be19a2ecb727739de5d4eccdc740b6620e8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2483048931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a06aa272a2307d0efb819371d9dca53ae1106c7dad5af73ac53722ec57f999`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Mon, 12 May 2025 19:12:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 12 May 2025 19:13:12 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 12 May 2025 19:13:13 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 12 May 2025 19:13:21 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 12 May 2025 19:13:22 GMT
ENV JAVA_VERSION=25-ea+22
# Mon, 12 May 2025 19:13:22 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/22/GPL/openjdk-25-ea+22_windows-x64_bin.zip
# Mon, 12 May 2025 19:13:23 GMT
ENV JAVA_SHA256=8b16ab02467967b98cf7d8743da9c9688d3ff39b4a693b66b6d9fe84cc0bb55a
# Mon, 12 May 2025 19:13:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 12 May 2025 19:13:54 GMT
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
	-	`sha256:433714f2b2a088420493a789e574820330dd8710627164079ec8bf8a3aef1c76`  
		Last Modified: Mon, 12 May 2025 19:13:58 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cece69bee8a0a0e47eb547ddf89d3b2947a9baed369ec1facbdc886446227479`  
		Last Modified: Mon, 12 May 2025 19:13:58 GMT  
		Size: 359.4 KB (359431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abef151c372192997b6c377e5b7a4a7f1a072a6e8946b15f704da541d8e67b4b`  
		Last Modified: Mon, 12 May 2025 19:13:58 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57eccdbd8f45c74af1c5d7fc064c5ac4270db6bffb1412df592e4c9da1865f95`  
		Last Modified: Mon, 12 May 2025 19:13:58 GMT  
		Size: 347.6 KB (347581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76c63a5ca06c688be6120435732193c652b79ecf9b6b63bae12ee7e1eee8be6`  
		Last Modified: Mon, 12 May 2025 19:13:57 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e800c1a671a0121b5ec8d4cb7a63be77fed25e740bd545d8a38e56e643e514e`  
		Last Modified: Mon, 12 May 2025 19:13:57 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee77e7ee35de69e1aee07a8055fbcb84ae9ea2740ec0aa9e958aa8e693a312a`  
		Last Modified: Mon, 12 May 2025 19:13:57 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43b3ff9014e05d57f0fb40ac5de2e72546fcfdb7ccd5b772bccc7da781cf15e`  
		Last Modified: Mon, 12 May 2025 19:14:08 GMT  
		Size: 208.8 MB (208751664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331fbb8e7089c4d7f3aea062c678bed44d6f067ced05e3bfba48d9152307865b`  
		Last Modified: Mon, 12 May 2025 19:13:57 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
