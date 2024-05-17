## `openjdk:23-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:44c4fe404e1458f60a907eb4a544ee15aa40f7af3f3866c47d9f9feb2ad661e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `openjdk:23-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull openjdk@sha256:80eebc2616249fea0f58551671a9df3628c084b97cf62f3ee0215ca7872cc391
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2318230645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3df090a5d5781b0bff1b37110d39f63e4a63747b3c4732deab4fd5657c000b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Fri, 17 May 2024 18:53:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 17 May 2024 18:54:48 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 17 May 2024 18:54:48 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 17 May 2024 18:54:57 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 17 May 2024 18:54:58 GMT
ENV JAVA_VERSION=23-ea+23
# Fri, 17 May 2024 18:54:58 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/23/GPL/openjdk-23-ea+23_windows-x64_bin.zip
# Fri, 17 May 2024 18:54:59 GMT
ENV JAVA_SHA256=96ffdf81f3b64db2460741b910af4dedb0efc57ca5a463492843a61328a90ae1
# Fri, 17 May 2024 18:55:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 17 May 2024 18:55:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4327e86024002440f311fb42616ba63c44eaccfdd8840ec915cc6c7f869429e4`  
		Last Modified: Fri, 17 May 2024 18:55:38 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5735ea9c1b8177b2bcbbc031f165fb0294e29a121412977615d9410354fa17`  
		Last Modified: Fri, 17 May 2024 18:55:38 GMT  
		Size: 351.1 KB (351128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9429e5c95aa36e5470629fe6a0163d8b326a0b04d633e15be98722d3cf9a1b`  
		Last Modified: Fri, 17 May 2024 18:55:37 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44be49bd12c534ea428a5c0192cd912e0a99f810485b28be1b5db4c845b7e1eb`  
		Last Modified: Fri, 17 May 2024 18:55:37 GMT  
		Size: 299.9 KB (299864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf161859ee498e1a678191fb2f80e404fe86755ce37bfe03f0d9dd0490fc637`  
		Last Modified: Fri, 17 May 2024 18:55:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac8b521404cef6f52704394fb52d86f1389960f3b40befc91e7de09e9034ad2`  
		Last Modified: Fri, 17 May 2024 18:55:36 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73b6d6ce7dd3d792a8c72323e56d6ad3f32dc68298967c91aa796d85176ba8f`  
		Last Modified: Fri, 17 May 2024 18:55:36 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc1ddb5c15bc4c3b1ead08d466d648ec513bbd74a6ee8a9cffc2763aa8cccaaf`  
		Last Modified: Fri, 17 May 2024 18:55:47 GMT  
		Size: 204.9 MB (204900514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e518aa53b6822edd4273a4a9049be4c1912e2cd44bf42fe13098170a8efd6e2`  
		Last Modified: Fri, 17 May 2024 18:55:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
