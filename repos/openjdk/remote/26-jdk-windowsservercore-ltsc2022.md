## `openjdk:26-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:1214ab24db5bee0347fdc3e19b090282f4158135d7731afbdeab2275f9b88795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `openjdk:26-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull openjdk@sha256:cf37655ca15e0c90512151de60138661dc4b2583782fa1555cea27986f10cebc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2499767663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9137607f5288a090a351c42ad032cbb1e6e95564a256bf5836b6abf07aed67`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Mon, 30 Jun 2025 17:28:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 30 Jun 2025 17:29:32 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 30 Jun 2025 17:29:33 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 30 Jun 2025 17:29:42 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 30 Jun 2025 17:29:43 GMT
ENV JAVA_VERSION=26-ea+4
# Mon, 30 Jun 2025 17:29:45 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/4/GPL/openjdk-26-ea+4_windows-x64_bin.zip
# Mon, 30 Jun 2025 17:29:46 GMT
ENV JAVA_SHA256=bb9270496ac199b05ed1ccbf5c3caa75f278f93900fac9444931bbbc76524588
# Mon, 30 Jun 2025 17:30:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 30 Jun 2025 17:30:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9d76659e003ff2762e8a4eaa24d1823759224eede4ef2b6ce3db492361996d`  
		Last Modified: Mon, 30 Jun 2025 17:30:54 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7ed86f2b1bb665a38717978b3f6fe4ae4a8033e4617d10d897b948c01f831c`  
		Last Modified: Mon, 30 Jun 2025 17:30:54 GMT  
		Size: 358.6 KB (358605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ea2df61d045ca3b0c83e154f277765c86aa387566120fc45a3d35b4e1bb1d6`  
		Last Modified: Mon, 30 Jun 2025 17:30:54 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb72953859389098e3d61f74eb464a8258cfb16c7de3827b9d87b16f9dc7b464`  
		Last Modified: Mon, 30 Jun 2025 17:30:54 GMT  
		Size: 346.9 KB (346906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fea0c668c5cccfb85c484505035e92ba66c90f02847c690871abd92e843c935`  
		Last Modified: Mon, 30 Jun 2025 17:30:54 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6cab9af6ec87cdc8726a0ed96773f28a014ae84f208d8978b2508868d798fb8`  
		Last Modified: Mon, 30 Jun 2025 17:30:54 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da9b54cef8db895b4ee149983cd3863952e2010ef29003808b98cf9582620bb`  
		Last Modified: Mon, 30 Jun 2025 17:30:54 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a008e956f27299f160f0e26491a95e8c39e3c865484bfeaaa2a9e5b3262e86`  
		Last Modified: Mon, 30 Jun 2025 17:36:56 GMT  
		Size: 218.8 MB (218802836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298c6db96ebd60b3d2fc5025aaf7427d698a09dc0c159457f66a603571c73c81`  
		Last Modified: Mon, 30 Jun 2025 17:30:54 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
