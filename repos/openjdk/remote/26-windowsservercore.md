## `openjdk:26-windowsservercore`

```console
$ docker pull openjdk@sha256:873613e6dd38cd722f886233e8102e05c92c3d88989e0dac58684e0860aef5c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `openjdk:26-windowsservercore` - windows version 10.0.26100.4349; amd64

```console
$ docker pull openjdk@sha256:1922cb46cf8becd498f0acef25e82b4825a62eee37b2d0bf61c722c0c4e39420
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3695805475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e3fafdd4ad784e959aaafe678a32288787b015996897dc3ca0cf17f11fcc27`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Mon, 30 Jun 2025 17:34:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 30 Jun 2025 17:34:41 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 30 Jun 2025 17:34:44 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 30 Jun 2025 17:34:57 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 30 Jun 2025 17:34:59 GMT
ENV JAVA_VERSION=26-ea+4
# Mon, 30 Jun 2025 17:35:04 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/4/GPL/openjdk-26-ea+4_windows-x64_bin.zip
# Mon, 30 Jun 2025 17:35:06 GMT
ENV JAVA_SHA256=bb9270496ac199b05ed1ccbf5c3caa75f278f93900fac9444931bbbc76524588
# Mon, 30 Jun 2025 17:36:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 30 Jun 2025 17:36:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341c918446e3dde2759dba1159661b8abc690af2c7c07ee9fb229f09767d319f`  
		Last Modified: Mon, 30 Jun 2025 17:39:33 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc85c3ceee5134ae13594ea065c2fda143b4d8501b5cd8f073b78f604eb1f480`  
		Last Modified: Mon, 30 Jun 2025 17:39:34 GMT  
		Size: 397.1 KB (397059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3eb76743d37c0a1d2f199f7c1134c271794ea7dfc3859f3b5f166a8facc5176`  
		Last Modified: Mon, 30 Jun 2025 17:39:34 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f26a26fb4260a8d8ea2bfb28bc5ed9e6ccd46a8d3584be12d663d8e56edb34`  
		Last Modified: Mon, 30 Jun 2025 17:39:34 GMT  
		Size: 382.3 KB (382328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41620ba50e80908c7bfff6eb9e9cc29488d030b2fe7cef70cf5aa80cbaa6b8f`  
		Last Modified: Mon, 30 Jun 2025 17:39:34 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb04c66236e735dbbc39be0869fda42ad1d3fa09bc29ed96fe683ef747ea3d9`  
		Last Modified: Mon, 30 Jun 2025 17:39:33 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27140cd831239c112827350ed62853f801107ff043208c2203c276d46eefeb7`  
		Last Modified: Mon, 30 Jun 2025 17:39:34 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1920e3769b35b3ec37fe13aa2d3fbcc95048e18157a67dc9792e383adda1e9e8`  
		Last Modified: Mon, 30 Jun 2025 18:09:53 GMT  
		Size: 218.8 MB (218844233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2047eba5c9198d0f9973e54324993efc51adc2e6eac33d77b0840dea7ac904c0`  
		Last Modified: Mon, 30 Jun 2025 17:39:34 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-windowsservercore` - windows version 10.0.20348.3807; amd64

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
