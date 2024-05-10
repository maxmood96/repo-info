## `openjdk:23-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:4fa8ab715592ad3d3a2d29e969259c5bc388d6db01dd64cb330685f04a7c594e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `openjdk:23-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull openjdk@sha256:71006994dcd6ed8f40071b060ed79346238f86549d5fb64fe5a061bcc5b27119
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2204953422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6995eb40321176fade29b8e2ca4e474cae6ae453d717eda5c7e59ac11fd2afb2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Fri, 10 May 2024 00:51:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 10 May 2024 00:53:16 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 10 May 2024 00:53:16 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 10 May 2024 00:53:22 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 10 May 2024 00:53:23 GMT
ENV JAVA_VERSION=23-ea+22
# Fri, 10 May 2024 00:53:24 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/22/GPL/openjdk-23-ea+22_windows-x64_bin.zip
# Fri, 10 May 2024 00:53:24 GMT
ENV JAVA_SHA256=a849b0c4f58cb28b02e6c43660886859ce8678d18224b4038ad69c1e3ead6249
# Fri, 10 May 2024 00:53:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 10 May 2024 00:53:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d8e710384f03d67c4d0752c5e025bbac255a96e3b9c36f43b1396c795045d0`  
		Last Modified: Fri, 10 May 2024 00:54:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f29716889fe0940673927d5e761c52ec6e313faf5e3cbd498c61adfb04afcb`  
		Last Modified: Fri, 10 May 2024 00:54:03 GMT  
		Size: 501.4 KB (501410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31445172d1e47e8231672edd872290b39b1be436a7f2218eaf2f95072ee747f8`  
		Last Modified: Fri, 10 May 2024 00:54:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa0ddaf1bcbce45ad09199e01f688def0a45550be4db16090cdb9cbcb9b0f6`  
		Last Modified: Fri, 10 May 2024 00:54:03 GMT  
		Size: 319.1 KB (319076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5863fc14ebd7d3e20194e442dd2de38e4058c49ae068e8d4da1eb535642002`  
		Last Modified: Fri, 10 May 2024 00:54:02 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9317a107ed27830ad2c163c83a0a3424c0d05cef36ac1a522269dd934ccc505f`  
		Last Modified: Fri, 10 May 2024 00:54:02 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c9e4c5830fa6ffc5aebaf78ac2786963cb5ae5d99531af15c5479c35fa7bb6`  
		Last Modified: Fri, 10 May 2024 00:54:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb85fab317061bb7ced484802d0e4b598b4ce63c4ef74e5b8e6d07ee71e08f8`  
		Last Modified: Fri, 10 May 2024 00:54:13 GMT  
		Size: 204.8 MB (204751453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f76a6055e60cfbc86ccc23f6c2767ed7508e1983c705d881f723a759c1963b6`  
		Last Modified: Fri, 10 May 2024 00:54:02 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
