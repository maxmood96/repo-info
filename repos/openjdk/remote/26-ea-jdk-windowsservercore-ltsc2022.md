## `openjdk:26-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:56ace84cba914f8f29ebef4549c2166a299149b7dce359de92d6569753ce29d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `openjdk:26-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull openjdk@sha256:da5ebe55a7bc14889eb772cacf7d5963e7a6dc2d9d1e8bc5ae7de5bf9529b3e7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2499712362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269deda5f817de18fab511fb3eff3e9a213b60e5b8c715e0ad017e8679832fa0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Mon, 16 Jun 2025 18:05:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 16 Jun 2025 18:05:46 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 16 Jun 2025 18:05:47 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 16 Jun 2025 18:05:53 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 16 Jun 2025 18:05:54 GMT
ENV JAVA_VERSION=26-ea+2
# Mon, 16 Jun 2025 18:05:55 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_windows-x64_bin.zip
# Mon, 16 Jun 2025 18:05:55 GMT
ENV JAVA_SHA256=a9f823b291381b908d5f1a0ffaf16b5ff2b8749780ab76db3b8e8fde9bf04be0
# Mon, 16 Jun 2025 18:06:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 16 Jun 2025 18:06:18 GMT
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
	-	`sha256:1044e6971b2fe48a264bf7ed3825934b8aa7c92569023b93d2f0ce6abda98ee2`  
		Last Modified: Mon, 16 Jun 2025 18:07:49 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947f5518145b35adc8e880d53095263341127912cc5bacd02ecedf4511b7cd7f`  
		Last Modified: Mon, 16 Jun 2025 18:07:49 GMT  
		Size: 365.4 KB (365396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fb5d508ef09978179f15c45c34d1a1508c1ded91dd704da0876ef2ec7eafa9`  
		Last Modified: Mon, 16 Jun 2025 18:07:50 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508e5855a79a9cf7ea2cb8b197ff769328310584d1bafd8ed3b7f9bc073f0351`  
		Last Modified: Mon, 16 Jun 2025 18:07:51 GMT  
		Size: 354.2 KB (354186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf31ca6e1f89f7353c8d51f7c6e84688887e88ccccb82aa27606b5d45ce9908`  
		Last Modified: Mon, 16 Jun 2025 18:07:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de38d3a9ef694c0c3b9f4d7bbc11786e25f48edc62425cef87babd108921f7f1`  
		Last Modified: Mon, 16 Jun 2025 18:07:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51b735e3aba05cbbe2f202104169cffb2e188fde3a20005141db7afbeb007d3`  
		Last Modified: Mon, 16 Jun 2025 18:07:51 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8f8147acacecead3747701c6b251ebff80129cd95e990e1ab2a5d7dfa822ba`  
		Last Modified: Mon, 16 Jun 2025 19:08:23 GMT  
		Size: 218.7 MB (218733441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f05f40c36e66e78de21a43c3bdbc0967fa1519ab5d9027ecdb17adadde068f9`  
		Last Modified: Mon, 16 Jun 2025 18:07:51 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
