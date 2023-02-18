## `openjdk:21-ea-10-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:cca2f0d7a123315a33d1982ed95e498b14e783c6da7bd778956c271be5073e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1547; amd64

### `openjdk:21-ea-10-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.1547; amd64

```console
$ docker pull openjdk@sha256:6deb1ac603d96bf4230dcf720b326a5cd8e2b4c5f83143a51763aec9dedb685b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1875501602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17eddb27c35482389aba7f5ebe53f1020b9d7aa186ec4de16e826a7efc48714b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Tue, 07 Feb 2023 11:42:22 GMT
RUN Install update 10.0.20348.1547
# Wed, 15 Feb 2023 22:37:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:14:39 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 16 Feb 2023 02:14:40 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 16 Feb 2023 02:15:04 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 18 Feb 2023 00:01:20 GMT
ENV JAVA_VERSION=21-ea+10
# Sat, 18 Feb 2023 00:01:21 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/10/GPL/openjdk-21-ea+10_windows-x64_bin.zip
# Sat, 18 Feb 2023 00:01:24 GMT
ENV JAVA_SHA256=68e0d0fd2ee261104468254cbb5c2087e757f7897c4b0ad7c462af5aef2df3c8
# Sat, 18 Feb 2023 00:04:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 18 Feb 2023 00:04:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d015a9e7adea898d81486dce8b513b0e9cbeca30904cac18c3ea98ab3be7a6`  
		Last Modified: Thu, 16 Feb 2023 00:28:01 GMT  
		Size: 293.3 MB (293317272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9c63a3d1906c0f8f7ca38587ab5f1c84160f9127cce25fb7f57d8a60dc7008`  
		Last Modified: Thu, 16 Feb 2023 00:26:46 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8108d16cd884206ec4969828d09af6c32cb29b30d6f5ac0628fbaa03f5acbfc3`  
		Last Modified: Thu, 16 Feb 2023 02:27:56 GMT  
		Size: 770.5 KB (770457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c865bc76fec4cadb1aba9ec04e94e30b1ae91b8396e43f048cac5d9e9751fb`  
		Last Modified: Thu, 16 Feb 2023 02:27:55 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6f5b31252c305eec6ed404696a45a13faa4edf1d630169d6b56eb13e25229c`  
		Last Modified: Thu, 16 Feb 2023 02:27:55 GMT  
		Size: 570.8 KB (570829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a241c5a5a1bd00c6eff8c509724fa450e588edac3b528386dc7596b0b653d430`  
		Last Modified: Sat, 18 Feb 2023 00:12:19 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81c7f2cef22e3f1fc7bc8942c91e22755903b336ed06ee52229e70605cb0378`  
		Last Modified: Sat, 18 Feb 2023 00:12:19 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b202b864c744668ad5a63d5f636911206b85c30acd3cb063bcd12dd30008b31`  
		Last Modified: Sat, 18 Feb 2023 00:12:18 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d712990be9dbd3968ae8ea18b96c20d86c8fbf343727f874c884e121d2cc9aea`  
		Last Modified: Sat, 18 Feb 2023 00:12:46 GMT  
		Size: 194.8 MB (194805593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa49df0d9277fc59ed4941456d9c8ae2641851ad9b81bf74966c8558712f90b3`  
		Last Modified: Sat, 18 Feb 2023 00:12:19 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
