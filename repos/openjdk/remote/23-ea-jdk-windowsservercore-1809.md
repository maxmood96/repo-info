## `openjdk:23-ea-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:b84eb5382ec9d489ad3a9160e12fe27882152af337b29e864068aab41576b734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `openjdk:23-ea-jdk-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull openjdk@sha256:6e41489b877186eec4356911042d7a09afc19ca2e66cc7174c4597549d2dc0db
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2323521672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492017700287e379a7303a6ff5c3c0e8b6a0a531e41ec83d8b698c5d462393e9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Sat, 16 Mar 2024 00:09:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 16 Mar 2024 00:10:44 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 16 Mar 2024 00:10:45 GMT
ENV JAVA_HOME=C:\openjdk-23
# Sat, 16 Mar 2024 00:11:06 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 16 Mar 2024 00:11:06 GMT
ENV JAVA_VERSION=23-ea+14
# Sat, 16 Mar 2024 00:11:07 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/14/GPL/openjdk-23-ea+14_windows-x64_bin.zip
# Sat, 16 Mar 2024 00:11:07 GMT
ENV JAVA_SHA256=bda022a1843857170a5addfeffecf490af3c3b93a8925899193a09a093bd8b4b
# Sat, 16 Mar 2024 00:11:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 16 Mar 2024 00:11:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d2f68ae3e563c996f31cd13becfd8280e7e567b09b35afaa510442e0794846`  
		Last Modified: Sat, 16 Mar 2024 00:11:51 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8c9090aff08cac5ebf902591b1f6c6e354d89f7f91e659d0800d653842f2a7`  
		Last Modified: Sat, 16 Mar 2024 00:11:51 GMT  
		Size: 500.7 KB (500694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa70658817ea2b0dac2d1a97be4aebb9bea5cca601bd67fbb7b9d01703a3ccc`  
		Last Modified: Sat, 16 Mar 2024 00:11:50 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c16a365b8c0cb7c82ad301c930294b3b6835ed6e2d7fd4e129345f4cd4f94380`  
		Last Modified: Sat, 16 Mar 2024 00:11:50 GMT  
		Size: 351.4 KB (351443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ac9308262785d3bf45a6b8f57d5943fcb057d9b4dd8fc733fb23b824f37d3`  
		Last Modified: Sat, 16 Mar 2024 00:11:49 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50253595937ab0ff7ec41baf9f92295fbb575b8b134dff7a04e9acdbc27d2a09`  
		Last Modified: Sat, 16 Mar 2024 00:11:49 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014201f5c854e92ee3a5fed7e66168dabb0095fd5ff4e27b3a4504961b868f55`  
		Last Modified: Sat, 16 Mar 2024 00:11:49 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd33e958a3a7687ba829e566091a8d96b571e76df273bcdebd48908c160d5ff`  
		Last Modified: Sat, 16 Mar 2024 00:12:01 GMT  
		Size: 197.6 MB (197561758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14cb96c77054ab52868d42e1b5863192bc1a8e2866a49583c83614817745211a`  
		Last Modified: Sat, 16 Mar 2024 00:11:49 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
