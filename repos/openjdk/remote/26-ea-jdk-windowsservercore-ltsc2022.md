## `openjdk:26-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:46ccc1e0291250e530728e59ccb354757768250e890c9d511cff6b93ac78e732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `openjdk:26-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull openjdk@sha256:7b1c33746935745cc979ad695739b8586652d4fcf58a95bbab1c1b2dbcd9d68d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2502003331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbaa92c716015eab11404f10cb469a790eaac6a2289c19d59f75348b2776e43`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:58:45 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 Sep 2025 21:58:46 GMT
ENV JAVA_HOME=C:\openjdk-26
# Wed, 10 Sep 2025 21:58:52 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 10 Sep 2025 21:58:53 GMT
ENV JAVA_VERSION=26-ea+14
# Wed, 10 Sep 2025 21:58:53 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/14/GPL/openjdk-26-ea+14_windows-x64_bin.zip
# Wed, 10 Sep 2025 21:58:54 GMT
ENV JAVA_SHA256=a7542fc9e185b46aef40f54067948209eaeed10cc87b141740dc4b4236bf3d70
# Wed, 10 Sep 2025 21:59:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 10 Sep 2025 21:59:26 GMT
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
	-	`sha256:11dfa0f411d1819cedf10f818f0d607fd88a441730267c2b072a473392e9fb06`  
		Last Modified: Wed, 10 Sep 2025 21:55:46 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf2cfa8fd3755443efa1f2e42a917263235638bfde1ecf06a73e60a38e1b9cc`  
		Last Modified: Wed, 10 Sep 2025 21:59:53 GMT  
		Size: 350.0 KB (349993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460cf8c4143f7d31504de90cf678ace5a0d1de6f8f279dd699874c1c68c021a7`  
		Last Modified: Wed, 10 Sep 2025 21:59:53 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae8f27c47ec8f88387a30745d424df8d95c3093c6ae4970b3ff3e65acdaf1417`  
		Last Modified: Wed, 10 Sep 2025 21:59:53 GMT  
		Size: 334.5 KB (334458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff15707928bd433e8fa5db0b3f486f899d2af5db44883338e4e944a7f731d02`  
		Last Modified: Wed, 10 Sep 2025 21:59:53 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b73501ff79abf4e10617f6c952f509b43f6a10501979e3b06ab947df1ac417`  
		Last Modified: Wed, 10 Sep 2025 21:59:53 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898e954b87cdd9f761264d2a42046f99ac3b1a76ceee966a0502f2dd9c2b4c37`  
		Last Modified: Wed, 10 Sep 2025 21:59:53 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a78f36689ede1e706cc9363d8b548198f8e03706c9b996ba06ccc8752d7424`  
		Last Modified: Wed, 10 Sep 2025 22:21:21 GMT  
		Size: 219.2 MB (219166054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912e502fb33bde8c37a3560acb4cc238494fcad88d527851d1736e2d0a552790`  
		Last Modified: Wed, 10 Sep 2025 21:59:53 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
