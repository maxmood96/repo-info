## `openjdk:25-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:b8f9750a962581141f9ae44ccd2d4e6830a830e09b7ab3ab585d8dd9983b3c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `openjdk:25-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull openjdk@sha256:860df8a554e1356c0797e78b5873dc15ad111978ecb43151301dfa073caebb6a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2499793514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b297fa48354319ac24f01fc002defc1b8d1f1a8c00070750d47eacfa90b533c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Sat, 21 Jun 2025 00:28:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 21 Jun 2025 00:28:25 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 21 Jun 2025 00:28:25 GMT
ENV JAVA_HOME=C:\openjdk-25
# Sat, 21 Jun 2025 00:28:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 21 Jun 2025 00:28:34 GMT
ENV JAVA_VERSION=25-ea+28
# Sat, 21 Jun 2025 00:28:34 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/28/GPL/openjdk-25-ea+28_windows-x64_bin.zip
# Sat, 21 Jun 2025 00:28:35 GMT
ENV JAVA_SHA256=4e1f6ee8523006f5f4e9c5e78283bec3011ecacaac80de81b4e8f75647efc1cc
# Sat, 21 Jun 2025 00:28:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 21 Jun 2025 00:28:57 GMT
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
	-	`sha256:b790e4076f3273d9da88ae8b790e3c86b598981e20bb6b720b49ff0059f9eeff`  
		Last Modified: Sat, 21 Jun 2025 01:07:48 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3468d94d4e83dc63887eae927f28031a88c1eeb497a1cb384e0c8de090f0e1a6`  
		Last Modified: Sat, 21 Jun 2025 01:07:48 GMT  
		Size: 357.8 KB (357784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fedfd2a6b43aaaf68b7a4cba5b13cfd1d7362c53f37c91cbcc7a29ed59a048e6`  
		Last Modified: Sat, 21 Jun 2025 01:07:48 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6dd8e9cb6e61436df4351ecebea6c6db91f42ea2a80bb7374d3d526c6dbd4a`  
		Last Modified: Sat, 21 Jun 2025 01:07:48 GMT  
		Size: 347.0 KB (346952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b809b37c618490ce75f0e5457f90cb2f4b6354619f3b62e91025616af1c2dcca`  
		Last Modified: Sat, 21 Jun 2025 01:07:48 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88f1738bc60fa0f396719db8fab97f223d27039fda55f170a1f57908f0d0ed6`  
		Last Modified: Sat, 21 Jun 2025 01:07:48 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4f456142f3df756eff4e456e83d01b785726af5220560b4722170f47fddaae`  
		Last Modified: Sat, 21 Jun 2025 01:07:49 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa1290fe761aebf6020d89c1f1d34f19b12344eabec793511f43f20ab375681`  
		Last Modified: Sat, 21 Jun 2025 01:08:06 GMT  
		Size: 218.8 MB (218829442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d1332858a239584aca9854f908a935907f2cc022796289b4f40c15da105535`  
		Last Modified: Sat, 21 Jun 2025 01:07:49 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
