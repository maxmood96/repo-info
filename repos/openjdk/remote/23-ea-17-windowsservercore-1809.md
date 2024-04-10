## `openjdk:23-ea-17-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:10ef75dcdd1d196c76bf39b3b58cc9643c84b441d1208812554d3c9a81e251b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `openjdk:23-ea-17-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull openjdk@sha256:eeaf63009519ffa70f46262d594b1e7b2711f2114153a6cca99c124f65f220b9
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2370906868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c993e6386ef77c1291820da71f7d35d1c1a3417c0d07a73913a7e434abcf2f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Wed, 10 Apr 2024 00:03:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 00:04:17 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 Apr 2024 00:04:18 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 10 Apr 2024 00:04:44 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 10 Apr 2024 00:04:45 GMT
ENV JAVA_VERSION=23-ea+17
# Wed, 10 Apr 2024 00:04:45 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_windows-x64_bin.zip
# Wed, 10 Apr 2024 00:04:46 GMT
ENV JAVA_SHA256=d370ad95643e427d9a9f79c527dc3dfbd3fa07ebda3684fe18acba87d4342d57
# Wed, 10 Apr 2024 00:05:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 10 Apr 2024 00:05:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9085c72dd7084c1461b4921ca6c006335e65569f09c4957ba2a1232318ff77`  
		Last Modified: Wed, 10 Apr 2024 00:05:37 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21f7ce95b5965883d88493fe1f5bcc5835cbf5f27abe69019d9b9e909b3e67f`  
		Last Modified: Wed, 10 Apr 2024 00:05:37 GMT  
		Size: 477.4 KB (477436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c110d3063ed1de78f6339d1685e606319911bcfae7c25c73d36a2a58c6383793`  
		Last Modified: Wed, 10 Apr 2024 00:05:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c10fc1d1af7a79a0233aa07ece995bbefcdc9ab1661a0ce3b080d30a2a22a62`  
		Last Modified: Wed, 10 Apr 2024 00:05:37 GMT  
		Size: 333.7 KB (333662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5917690a2e90792c3203e66eeef6298b740aa5c9a7829671830367ed7954e397`  
		Last Modified: Wed, 10 Apr 2024 00:05:34 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bfdc9ac772e1ae8560bb47d813bb2e16d971f4b465e7fb0071af211a6062a2`  
		Last Modified: Wed, 10 Apr 2024 00:05:34 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d054b50d0fbb0c53b68b1d5ddf8b0bf0838729123bd77db08df55bf691b7b5a`  
		Last Modified: Wed, 10 Apr 2024 00:05:34 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8f49626366b5aaf4b74a0ffdaab7d2a3d1220f5c10e90fe6a2948a13b1ae9a`  
		Last Modified: Wed, 10 Apr 2024 00:05:47 GMT  
		Size: 205.7 MB (205660052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df723a31c98c42416ad776ab0851d6883af55cfda5fd6bae0e50ea5756946564`  
		Last Modified: Wed, 10 Apr 2024 00:05:34 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
