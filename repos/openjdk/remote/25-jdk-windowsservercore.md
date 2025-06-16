## `openjdk:25-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:4b40d5cde8b11ccf56a147212add1224c9fb41bb372f06d8fdbe311157fb1a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `openjdk:25-jdk-windowsservercore` - windows version 10.0.26100.4349; amd64

```console
$ docker pull openjdk@sha256:35bf60d1ec90f804fefe9ed1189fcfc53f3da6f5578cc44fbcb6d5b7af7ff9e0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3695844343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a99ff3f99048dbcd16128c9b3d0278f08837c2d8e5a9602427c5f26fef2620`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Mon, 16 Jun 2025 17:55:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 16 Jun 2025 17:55:37 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 16 Jun 2025 17:55:38 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 16 Jun 2025 17:55:45 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 16 Jun 2025 17:55:46 GMT
ENV JAVA_VERSION=25-ea+27
# Mon, 16 Jun 2025 17:55:47 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/27/GPL/openjdk-25-ea+27_windows-x64_bin.zip
# Mon, 16 Jun 2025 17:55:48 GMT
ENV JAVA_SHA256=c29b512a7b967525b3286a6451ba478530d950d8d4981c8ce5d681ff715a5c22
# Mon, 16 Jun 2025 17:56:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 16 Jun 2025 17:56:08 GMT
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
	-	`sha256:a65e6063ca6eb7321f879cceb1ae0876d76a3ed977459eded0edd475879a8c40`  
		Last Modified: Mon, 16 Jun 2025 18:00:11 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5f7f1d14123d7121cc44bb38d17fd2c0022c217fccb3e5a33ae589b4035146`  
		Last Modified: Mon, 16 Jun 2025 18:00:15 GMT  
		Size: 404.0 KB (403971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5d724ab680ac67f4d530b3d08e71cda0a526386e9e49d125a1540c2708fa58`  
		Last Modified: Mon, 16 Jun 2025 18:00:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79439d88ca8995aa294a1bf60ebef1eafda673cee9bf15c1b0761e64b828ef70`  
		Last Modified: Mon, 16 Jun 2025 18:00:14 GMT  
		Size: 389.6 KB (389587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8d17f5f9f4e481f9b279ea04b7b7b32fa625d85223a761f0daa63ef702ee1a`  
		Last Modified: Mon, 16 Jun 2025 18:00:13 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37eba052f332da2bed05e42adb1d8a68cdc6ced4bfb6bcf4bc7d8c397306ec1`  
		Last Modified: Mon, 16 Jun 2025 18:00:14 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3707f5b32fd9fc5c2c563fe2d7011f64f6824392b8a9f58759bac5cedab7d2af`  
		Last Modified: Mon, 16 Jun 2025 18:00:13 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff0a3fbd5aed6c72d0470720996dfd6d0dd487a2126e615fec133924ee91bb0`  
		Last Modified: Mon, 16 Jun 2025 18:09:10 GMT  
		Size: 218.9 MB (218868948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9105912477d38db57382c170c12b88a1b9244b76c75b6072307db2ad43378ea5`  
		Last Modified: Mon, 16 Jun 2025 18:00:13 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-jdk-windowsservercore` - windows version 10.0.20348.3807; amd64

```console
$ docker pull openjdk@sha256:673b83d78c5618077113504c32b1cc9c8988e76fc323b52442c84d7ec9df397c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2499778942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502ff5f3e3484b72818bba55ae0e80c935fbe39f9ba39360f07017363b20b33e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Mon, 16 Jun 2025 17:54:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 16 Jun 2025 17:54:26 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 16 Jun 2025 17:54:27 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 16 Jun 2025 17:54:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 16 Jun 2025 17:54:34 GMT
ENV JAVA_VERSION=25-ea+27
# Mon, 16 Jun 2025 17:54:35 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/27/GPL/openjdk-25-ea+27_windows-x64_bin.zip
# Mon, 16 Jun 2025 17:54:36 GMT
ENV JAVA_SHA256=c29b512a7b967525b3286a6451ba478530d950d8d4981c8ce5d681ff715a5c22
# Mon, 16 Jun 2025 17:54:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 16 Jun 2025 17:55:00 GMT
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
	-	`sha256:e52d8e2771faa6bf03122e8a088ead3d0d133d898e97202fd54f59586d3290b7`  
		Last Modified: Mon, 16 Jun 2025 17:56:33 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22caf26579711b3b4d672f08266b383c714ed0b20fbd6cac20ccc1788a90520`  
		Last Modified: Mon, 16 Jun 2025 17:56:33 GMT  
		Size: 357.6 KB (357598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5f73cafe8e470cd078b7506ce89bc4dfcc2040c26bdd4ab3c310eaf67f143a`  
		Last Modified: Mon, 16 Jun 2025 17:56:33 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebaf78da7d05ec9bf5b0fce1db9feb2eab63b4e71083e6a7924f397af725ab45`  
		Last Modified: Mon, 16 Jun 2025 17:56:33 GMT  
		Size: 346.2 KB (346207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97aa9de85d10673a5db71da59d26e340598b14737378e8ef121f425a462846b`  
		Last Modified: Mon, 16 Jun 2025 17:56:33 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9bdab477f4018735a24ce52a2f805a62e868a43329e4f7642bab792d88ae5e`  
		Last Modified: Mon, 16 Jun 2025 17:56:33 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c652090baf3de091e523aab727f25b6a448c035146d56a3018192f3cabecc122`  
		Last Modified: Mon, 16 Jun 2025 17:56:34 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84f4204dd629da2838aed62d52b357d261ae8d771742a4adeb274dd08c11966`  
		Last Modified: Mon, 16 Jun 2025 18:08:37 GMT  
		Size: 218.8 MB (218815846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a110126960289f578c57f7403ba91062fd37ec236ead20480c681ff9094a81f6`  
		Last Modified: Mon, 16 Jun 2025 17:56:34 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
