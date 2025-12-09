## `openjdk:26-ea-27-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:426af96df9064ec606a78e738346782910928585790cc112e89b218ad5157e7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `openjdk:26-ea-27-jdk-windowsservercore` - windows version 10.0.26100.7462; amd64

```console
$ docker pull openjdk@sha256:3c94a3bf2bb75a1495d64cca2d1c6e11260359ff7dbcf65c5625d7283cabed9c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3479333263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c15eaadf32571cd3e3e703283ca51b40edd821ebc2e2df36ea7859595f0a37`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Tue, 09 Dec 2025 20:35:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:48:02 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:48:03 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 09 Dec 2025 20:48:08 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:48:09 GMT
ENV JAVA_VERSION=26-ea+27
# Tue, 09 Dec 2025 20:48:10 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_windows-x64_bin.zip
# Tue, 09 Dec 2025 20:48:11 GMT
ENV JAVA_SHA256=5fc8523fafe0bbe81e010d1bd57b12836c42cdd1f017e4492f67d56bde06f86a
# Tue, 09 Dec 2025 20:48:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:48:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62c64c7dc565d03eb3e9f39894e67ad9fe74d54f61e84975b3f57b9f2972a79`  
		Last Modified: Tue, 09 Dec 2025 20:45:08 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c71974a87b51cf6f3c1173d0dd549c9cd811ec8f94105839f73f41a7cbb278`  
		Last Modified: Tue, 09 Dec 2025 20:49:04 GMT  
		Size: 335.9 KB (335946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75dccdc57442bae9305519da51c85a0826dc042a40e1b069945e5871ebbcdf11`  
		Last Modified: Tue, 09 Dec 2025 20:49:04 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e64e9b7db1833188529973db2194fe400603af3bd237e0819a5513eed16bb55`  
		Last Modified: Tue, 09 Dec 2025 20:49:04 GMT  
		Size: 326.3 KB (326266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07cc06412dd9f9e6b77373717b849b33caf82ed9ce913f7c0c4b5b45e550eb4a`  
		Last Modified: Tue, 09 Dec 2025 20:49:04 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8582bfcef2f8c5a6823cd3a4e7c8c92dba150854b9e76ea7e4274f25aaca3428`  
		Last Modified: Tue, 09 Dec 2025 20:49:04 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b2e564c314fec71ac31165c3426f30f79c50a8df6f19fa448c4c90ceeb44e8`  
		Last Modified: Tue, 09 Dec 2025 20:49:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e74e314b5e1d28fe97cb517f237c65faa363da469a338106b60ec1079c9348a6`  
		Last Modified: Tue, 09 Dec 2025 20:49:15 GMT  
		Size: 225.5 MB (225542755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e66f7ecd3696ec6ed90f5e9d316b4355d40f1834ccb10726f6d106da364e01`  
		Last Modified: Tue, 09 Dec 2025 20:49:04 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-27-jdk-windowsservercore` - windows version 10.0.20348.4529; amd64

```console
$ docker pull openjdk@sha256:f8006175e6fda2960a40c4618225b8b67ca9ba4ce4f21face48ecaf0a78b6817
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2006273432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b74a67040c0b9b528c203023fd45a6655b73cbd9d6421322c5a362e704718a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 09 Dec 2025 20:32:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:45:09 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:45:09 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 09 Dec 2025 20:45:14 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:45:15 GMT
ENV JAVA_VERSION=26-ea+27
# Tue, 09 Dec 2025 20:45:16 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_windows-x64_bin.zip
# Tue, 09 Dec 2025 20:45:16 GMT
ENV JAVA_SHA256=5fc8523fafe0bbe81e010d1bd57b12836c42cdd1f017e4492f67d56bde06f86a
# Tue, 09 Dec 2025 20:45:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:45:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4337b0b452250939272a24a7d25392c5f6351fbf9da067a0d397cefbb4266c7a`  
		Last Modified: Tue, 09 Dec 2025 20:40:35 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afedf6959d8406aa6f61f5d1cb7e75197da86cb668b124864cc94da0f8aac1dd`  
		Last Modified: Tue, 09 Dec 2025 20:46:08 GMT  
		Size: 485.9 KB (485883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5647abb177001d198611cfbb4d40b1b1ddf4f9121ab23bc84e3cd2ed7a8075f`  
		Last Modified: Tue, 09 Dec 2025 20:46:08 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ae996b14cd7eae41f2fcd94683248c6d4c07e118061ee818560117bef288cc`  
		Last Modified: Tue, 09 Dec 2025 20:46:08 GMT  
		Size: 335.0 KB (335038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1fdebd185af009de4855f36787b8e36d1942f1ee60048cbb39647045441632`  
		Last Modified: Tue, 09 Dec 2025 20:46:09 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c917a6783420ef66a38dd51d49b6f28d585f8b4b9b494388a3a437670ea36d7`  
		Last Modified: Tue, 09 Dec 2025 20:46:08 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa4fa654cd2a97826e9bd38dfc0bff0fc25e0b066be62aefaaf1981709864bb`  
		Last Modified: Tue, 09 Dec 2025 20:46:08 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635c95c1d0ba2c81f9c67aa7e8d8074e8e069a445801d9c87b56f89de3d18991`  
		Last Modified: Tue, 09 Dec 2025 20:46:18 GMT  
		Size: 225.6 MB (225565350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e3a88099edb23e44bed68c6359ec743f8a3f31c8754fbf95535e26716b4da8`  
		Last Modified: Tue, 09 Dec 2025 20:46:08 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
