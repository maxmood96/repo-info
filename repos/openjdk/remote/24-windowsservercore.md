## `openjdk:24-windowsservercore`

```console
$ docker pull openjdk@sha256:bb06af488b5c9bfca301ded43b5e46370ab12d9ce0d356c5e07dc033e0aac1c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `openjdk:24-windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull openjdk@sha256:a4f1f432abdfb8f34dcdb5d68cb8dd2f190095c449750c47fdce0cf6d85a2617
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1671276500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d5f66e076ca8b2ac4315b1b5ed4874e0e5947f789056e0b014d85252affc2d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Tue, 08 Oct 2024 00:00:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 08 Oct 2024 00:00:37 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 08 Oct 2024 00:00:37 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 08 Oct 2024 00:00:44 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 08 Oct 2024 00:00:44 GMT
ENV JAVA_VERSION=24-ea+18
# Tue, 08 Oct 2024 00:00:45 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/18/GPL/openjdk-24-ea+18_windows-x64_bin.zip
# Tue, 08 Oct 2024 00:00:46 GMT
ENV JAVA_SHA256=6146921a840c402763aa710b209d872b2b91ba63221f33e494fa1312cb2a706c
# Tue, 08 Oct 2024 00:01:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 08 Oct 2024 00:01:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de07772962b1de25b8f990e2e881e51e92df43c0b4dde8bd928ccafb18de80ff`  
		Last Modified: Tue, 08 Oct 2024 00:01:19 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:504a20bafe3f341f5a145f0c003717c9fc7df64836ef39256a5148dd0488a486`  
		Last Modified: Tue, 08 Oct 2024 00:01:19 GMT  
		Size: 365.8 KB (365842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798cc23c9b8e3db5c4cf6be041ce6e1ecb48a42f2042366e7d3e11fea441724c`  
		Last Modified: Tue, 08 Oct 2024 00:01:19 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff92d816334ca57bc62e9914b3f45e484cde0d58a7c094bb44b9bc94685b3050`  
		Last Modified: Tue, 08 Oct 2024 00:01:19 GMT  
		Size: 341.3 KB (341348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00852aa617b496bd66dd9bcf81c5276a49243f72aec71127eab508309fa3e7f`  
		Last Modified: Tue, 08 Oct 2024 00:01:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f6063b4fc1d74c6c31689bf620bafa6063d30f1591f90f901bdc3e3cad4005`  
		Last Modified: Tue, 08 Oct 2024 00:01:17 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:535c4edf0b354addb3c5000acb30557a278609a9a9546a79d9235940533d773b`  
		Last Modified: Tue, 08 Oct 2024 00:01:17 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053388a8997faa75c947599223853ce60a2b5de792f9a55f92b322d31d5c8da6`  
		Last Modified: Tue, 08 Oct 2024 00:01:28 GMT  
		Size: 208.4 MB (208369160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f863ad16b49afec83a450716603d038c23a437972f8a8e5c23ff3eae01f273`  
		Last Modified: Tue, 08 Oct 2024 00:01:17 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull openjdk@sha256:70d4c6281cc76a9ab69e8d595c623063ef2f85d8a9b52b4110f809a785061809
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1929308534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20198f7688f5210b41b0fe815b241414ebb328966c8dd747f863699f871331ea`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 08 Oct 2024 00:00:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 08 Oct 2024 00:01:15 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 08 Oct 2024 00:01:16 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 08 Oct 2024 00:01:23 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 08 Oct 2024 00:01:24 GMT
ENV JAVA_VERSION=24-ea+18
# Tue, 08 Oct 2024 00:01:25 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/18/GPL/openjdk-24-ea+18_windows-x64_bin.zip
# Tue, 08 Oct 2024 00:01:25 GMT
ENV JAVA_SHA256=6146921a840c402763aa710b209d872b2b91ba63221f33e494fa1312cb2a706c
# Tue, 08 Oct 2024 00:01:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 08 Oct 2024 00:02:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83861f2bde8f55c1e1a0def8dc6abe1907e3ba8c8f5805381764ec9538397420`  
		Last Modified: Tue, 08 Oct 2024 00:02:07 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04836aac0e41b3dccb3271f2eee25707bacdab0680cb7e4325898552f59bf7c`  
		Last Modified: Tue, 08 Oct 2024 00:02:07 GMT  
		Size: 331.4 KB (331396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0ea7f6498d1ba2fbd96758a583bf5544f5ac3fe620804eabec63842b5e5d62`  
		Last Modified: Tue, 08 Oct 2024 00:02:07 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7bf1ac579da2882a9a175c867e4ba0f57ee03a061758db3ef72cc8cecedc4cf`  
		Last Modified: Tue, 08 Oct 2024 00:02:07 GMT  
		Size: 324.2 KB (324214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb7b88a93dffa686a55993d034d4c39fd2bdc3341213c7f3aad1c0a5fcf2bca`  
		Last Modified: Tue, 08 Oct 2024 00:02:05 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a05b1e0f7727bf661f2e09c0957a53bb54814a5244a846eb660e00cce369ad5`  
		Last Modified: Tue, 08 Oct 2024 00:02:05 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd5260774a236cbb73b72b94e4818eb8752ff07b7d20fbe17652750f9acffeb`  
		Last Modified: Tue, 08 Oct 2024 00:02:05 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e06d1c211d212f059bd193d0f0e35da3fb991054d5e7d402fefd479a3be769`  
		Last Modified: Tue, 08 Oct 2024 00:02:16 GMT  
		Size: 208.4 MB (208376416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bffc24925ede3b03c311014403d6464c684ef6681bae258f270ed3d751f4e2f`  
		Last Modified: Tue, 08 Oct 2024 00:02:05 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
