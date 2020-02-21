## `openjdk:15-jdk-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:9f99172b9164631ed9199622316c3e7a7ccc4d2ceea0c8f41de901edb1290616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `openjdk:15-jdk-windowsservercore-ltsc2016` - windows version 10.0.14393.3506; amd64

```console
$ docker pull openjdk@sha256:b65ce6efd500919ac3ddcd3c4c64209b8cf28db89745925aa783666c04cf7d1a
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5936226397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e164652de0ab8ca4ed90fbf3d48cd61b04b66f739e4b60a67e1dada8ac2e8b5f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 01:48:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2020 01:49:57 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Thu, 20 Feb 2020 01:49:59 GMT
ENV JAVA_HOME=C:\openjdk-15
# Thu, 20 Feb 2020 01:51:47 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Fri, 21 Feb 2020 00:26:05 GMT
ENV JAVA_VERSION=15-ea+11
# Fri, 21 Feb 2020 00:26:06 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/11/GPL/openjdk-15-ea+11_windows-x64_bin.zip
# Fri, 21 Feb 2020 00:26:07 GMT
ENV JAVA_SHA256=1abf19d39af7342aca71521dd5b3bd98d6782fc727f44bdc36f8f390ba528bdb
# Fri, 21 Feb 2020 00:28:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 21 Feb 2020 00:28:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:72c4471958f7f0f07260f0f430bcffb0bc07811088c24cffba1439d250ea1ae3`  
		Last Modified: Thu, 20 Feb 2020 03:04:52 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6eada8556f1688b8cc14a7529ed2bd5822b6570a73c142f15a023eda1563d9`  
		Last Modified: Thu, 20 Feb 2020 03:04:58 GMT  
		Size: 5.4 MB (5361808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ce35a0aa37afd4baa3b9058c4be764cc458f70c6849a36a7aaa50e6707e6b2`  
		Last Modified: Thu, 20 Feb 2020 03:04:52 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfc5a4ac5c33ba6e40369cbdb81f258c11758ec88b55da5560b114a6fc2ec2a`  
		Last Modified: Thu, 20 Feb 2020 03:04:55 GMT  
		Size: 5.3 MB (5341588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:701145bf2eec92daf6e8476f108eb1eb179810d0bbd94890ec1c7a1c558825be`  
		Last Modified: Fri, 21 Feb 2020 00:36:21 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b29ad579ef548d2a5d5e686f9f0651aeae33d7b19e7abfc0262cb1a9a4b8ee1`  
		Last Modified: Fri, 21 Feb 2020 00:36:21 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6590eae673002e36aad0a4e8aff7b9b4d411d7a5fb8a369da8999ed5a1e9ea84`  
		Last Modified: Fri, 21 Feb 2020 00:36:21 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7da098aeda0d72f555781c1bcd6b0e106d9628bd3c718e08f2d7fa674fd2bd`  
		Last Modified: Fri, 21 Feb 2020 00:36:47 GMT  
		Size: 198.5 MB (198450908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d7cd67b27dd6705fe210ebac566b41e6ee32c6fb92682fe335ff5214a2d1d8`  
		Last Modified: Fri, 21 Feb 2020 00:36:21 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
