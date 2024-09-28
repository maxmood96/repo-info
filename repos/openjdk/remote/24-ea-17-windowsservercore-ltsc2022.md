## `openjdk:24-ea-17-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:eaed13a155a94b7e74a7af4d2a3c3f5afd657876b474d2c2a79471aaafaf6c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `openjdk:24-ea-17-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull openjdk@sha256:d21854c5551a19ff284c91eb3e84bddf149da73a1b40c221ca7a821191892131
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1671192338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c7ad13a2565068f7040c525d46771756329a61b602d3ab2bb268c899f77166`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 28 Sep 2024 01:00:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 28 Sep 2024 01:01:31 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 28 Sep 2024 01:01:32 GMT
ENV JAVA_HOME=C:\openjdk-24
# Sat, 28 Sep 2024 01:01:38 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 28 Sep 2024 01:01:38 GMT
ENV JAVA_VERSION=24-ea+17
# Sat, 28 Sep 2024 01:01:39 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/17/GPL/openjdk-24-ea+17_windows-x64_bin.zip
# Sat, 28 Sep 2024 01:01:39 GMT
ENV JAVA_SHA256=bf219cde78b52efb95b3b6fc5e4204bfdaeaaabfac61261ef44b662f774f44a9
# Sat, 28 Sep 2024 01:02:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 28 Sep 2024 01:02:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401d152ca72320c3b57d2bdfa94bd5c4f1b4a653a70ab8c3abb1c119dc80164d`  
		Last Modified: Sat, 28 Sep 2024 01:02:11 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5261b3c7ab4b1b49c2548781e22322c09da3fc5d64d9a1e3250a1976b74f4969`  
		Last Modified: Sat, 28 Sep 2024 01:02:11 GMT  
		Size: 355.6 KB (355570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f046e44b57982f4e5d74ea5bde56868b830376a56d6d8f977352a2069341f80`  
		Last Modified: Sat, 28 Sep 2024 01:02:11 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1718f343b483c9f2a935dce9a779e038d47557d43153388a543ce04d69419475`  
		Last Modified: Sat, 28 Sep 2024 01:02:11 GMT  
		Size: 339.8 KB (339761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c736cf2779ef9bcaf94df45be8b88861c98bb956dd6058abe20734699eb99f40`  
		Last Modified: Sat, 28 Sep 2024 01:02:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574a362a0f5db47d2dfb673493cc5324dd8c00cb84a8183015c7511225698675`  
		Last Modified: Sat, 28 Sep 2024 01:02:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65cfda3d023408b157ff79746d65db77c8ff284338be753d890985a74b4ecd43`  
		Last Modified: Sat, 28 Sep 2024 01:02:09 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2d4ef60bf7dc6e8b8738b8f7d578dd701b8b526f9a88a4b01f4306a1da3cd0`  
		Last Modified: Sat, 28 Sep 2024 01:02:20 GMT  
		Size: 208.3 MB (208296885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8ed045a6f3b533d8c0ee62cbfede7c0ed8d343b5d744f0c72a80398c3050e1`  
		Last Modified: Sat, 28 Sep 2024 01:02:09 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
