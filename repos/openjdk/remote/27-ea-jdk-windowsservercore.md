## `openjdk:27-ea-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:4e003fd904cdaabae6053ebb30b54b8aae84225c872c41edb8c2a6c0c87e1555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `openjdk:27-ea-jdk-windowsservercore` - windows version 10.0.26100.32860; amd64

```console
$ docker pull openjdk@sha256:5e42de22999e86d20e3db702222b73b14b4a326cd09fa1dce3765f1a820f6a2b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2431919062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41a5353102f2e52e9bf1a27d7aae88006b94893d78577ba291748de2f9012c82`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:39:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:49:49 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 12 May 2026 23:49:50 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 12 May 2026 23:49:55 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 12 May 2026 23:49:56 GMT
ENV JAVA_VERSION=27-ea+21
# Tue, 12 May 2026 23:49:57 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_windows-x64_bin.zip
# Tue, 12 May 2026 23:49:58 GMT
ENV JAVA_SHA256=c141a4db38b2d45883ed5d65a72f4444d1efa690d650027308594335dec2b07b
# Tue, 12 May 2026 23:50:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 12 May 2026 23:50:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b51f7f8f80dada0ff15ebfc020be610f4ccb1f56aa991e13148edd33df8342`  
		Last Modified: Tue, 12 May 2026 23:39:57 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c785968391fa55bac93a778300e57101492475d74584e011ad34b8f8302dba3d`  
		Last Modified: Tue, 12 May 2026 23:50:28 GMT  
		Size: 400.9 KB (400927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e31999aa06627ee760fa15e484accbc378230565b37beecef96c74f6436284b`  
		Last Modified: Tue, 12 May 2026 23:50:27 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351acfd40993c8eb6f51df06e359873f365f081ab36f4926b6f200cf07ed5298`  
		Last Modified: Tue, 12 May 2026 23:50:28 GMT  
		Size: 387.8 KB (387848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2b3bc8ce88f5793bb370b76d107976abdadba667d9d3d6fd524bd26ae98dfe`  
		Last Modified: Tue, 12 May 2026 23:50:26 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e25e10449844aa90328c5b6fac1bfab7abf93d407e6158c20739ae6fcec289`  
		Last Modified: Tue, 12 May 2026 23:50:26 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71253120a4f9881a5f077abf57e8b65b1ce63b761e860d4dd7c711f560ad599`  
		Last Modified: Tue, 12 May 2026 23:50:26 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3007bf0f74e751c15fcf27d97add579df2e2a700388c4d75e52cd550c6a6c88`  
		Last Modified: Tue, 12 May 2026 23:50:42 GMT  
		Size: 225.2 MB (225180444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab2488eb9e70b70165e23d1645f72c8e11bbaa710f8dacd2d7ef2076aa0905f`  
		Last Modified: Tue, 12 May 2026 23:50:26 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-jdk-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull openjdk@sha256:0f042f59d06cf4bc4d4ce0eeda11842d5edd5ffd086c1801dbdd0837dd573642
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348395540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4775a9ef6258f1689584be0f095107317e8620f95e86f066c166e73d4cd0cb94`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:39:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:55:53 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 12 May 2026 23:55:54 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 12 May 2026 23:55:59 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 12 May 2026 23:56:00 GMT
ENV JAVA_VERSION=27-ea+21
# Tue, 12 May 2026 23:56:00 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_windows-x64_bin.zip
# Tue, 12 May 2026 23:56:01 GMT
ENV JAVA_SHA256=c141a4db38b2d45883ed5d65a72f4444d1efa690d650027308594335dec2b07b
# Tue, 12 May 2026 23:56:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 12 May 2026 23:56:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:917dd62015b1447671d0b141b1522081735e979c185e6644bec43931db85c017`  
		Last Modified: Tue, 12 May 2026 23:40:45 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685041c62f433f307e564c68f0285320efafe328f998e28e9f2b3e2cc0be18f6`  
		Last Modified: Tue, 12 May 2026 23:56:27 GMT  
		Size: 493.4 KB (493412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842a46936c6c8a785b9526bcbdeb541275878c2fe8e05625db6ca7d0e5919fed`  
		Last Modified: Tue, 12 May 2026 23:56:27 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25c6b5e0c278b8118655fa6f8cd3f3116a7638e16209fa6f9987ce91997596a`  
		Last Modified: Tue, 12 May 2026 23:56:27 GMT  
		Size: 337.3 KB (337264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60753f8e5193b0cc905edeaf434bd41197c12d05956662123a02fa47f415468f`  
		Last Modified: Tue, 12 May 2026 23:56:25 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f381e27eac1f2f2ec69ca75cce874b777ddf2ec1b172719897897cbfcafb90`  
		Last Modified: Tue, 12 May 2026 23:56:25 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f31a1248789a28678051c1e704764d0790b8cfb9978cea4a09a3a21a55c23ce`  
		Last Modified: Tue, 12 May 2026 23:56:25 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d958b141b9c9e4a90405251e7d47d8c83b89db2a91d906e2a26abbdd5a31ef`  
		Last Modified: Tue, 12 May 2026 23:56:40 GMT  
		Size: 225.1 MB (225136422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20091ec95c2165529715cc029a6cd73fb2010429d0fd7a680a988b7d637a3a6f`  
		Last Modified: Tue, 12 May 2026 23:56:25 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
