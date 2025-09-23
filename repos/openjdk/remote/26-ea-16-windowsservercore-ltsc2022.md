## `openjdk:26-ea-16-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:4cfe65f96d57f9e23dba4f2f81df29d1aab5cdfc618a22f60a66cf07c5e31f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `openjdk:26-ea-16-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull openjdk@sha256:313c0fe15cac74a9b5eb6845bf5143421933c50c8a7183fddbc6731541313d58
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2502157890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd59aaf95316e2cf2e29e74f77793fe66eeab11a911116277147c1acae2c96a8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Mon, 22 Sep 2025 22:12:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 22 Sep 2025 22:13:33 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 22 Sep 2025 22:13:34 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 22 Sep 2025 22:13:39 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 22 Sep 2025 22:13:40 GMT
ENV JAVA_VERSION=26-ea+16
# Mon, 22 Sep 2025 22:13:41 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/16/GPL/openjdk-26-ea+16_windows-x64_bin.zip
# Mon, 22 Sep 2025 22:13:42 GMT
ENV JAVA_SHA256=f867e655606913a0bda0dd383b0d783722ba5b64b9fa63a7a684afb3ed9c5e0c
# Mon, 22 Sep 2025 22:14:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 22 Sep 2025 22:14:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de025308e6c7fe95a48bc6f309e52c61c6253ccc5de132c2aced7c9a7058b86b`  
		Last Modified: Mon, 22 Sep 2025 22:23:15 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5216245c9193fc358d863a8f44293e53a062dcb1c724ef678f419a210ed761f5`  
		Last Modified: Mon, 22 Sep 2025 22:23:15 GMT  
		Size: 368.6 KB (368557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75f0b8d10371251a59a3a791ac6be3410edab216115cc890aa0a32041b58e92`  
		Last Modified: Mon, 22 Sep 2025 22:23:15 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7aaf5173994af62dbef4170b7f952df9b78788b02d14bc397b5d20b65fe3cc9`  
		Last Modified: Mon, 22 Sep 2025 22:23:15 GMT  
		Size: 350.8 KB (350830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f868b4d4eb664a1bb8c1d13f8a3f9fd89733a5983853146efd876c6d32d30a0`  
		Last Modified: Mon, 22 Sep 2025 22:23:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655796da91fe53de706718440cd806bc63f6077b81bdc1369b4afa8770d13380`  
		Last Modified: Mon, 22 Sep 2025 22:23:15 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee43e87b2e1c325cb20eed8880f2f98209fa530f07d71f933a6b0a760e47c436`  
		Last Modified: Mon, 22 Sep 2025 22:23:15 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33acb1e77cac2822d14e3fcd8b138a61b5d1a69b400efd9e320b372990a66d6`  
		Last Modified: Mon, 22 Sep 2025 23:16:01 GMT  
		Size: 219.3 MB (219285692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6744fac708ad5d889cffd9f57c64e23e0e5994e4f88636e0da50421ef954da7c`  
		Last Modified: Mon, 22 Sep 2025 22:23:15 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
