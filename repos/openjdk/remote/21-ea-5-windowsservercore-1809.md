## `openjdk:21-ea-5-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:04ea19e48640eb8ea662b3189a308efa6f609a8e5e4043dde8bf78122bc1e92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `openjdk:21-ea-5-windowsservercore-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull openjdk@sha256:4532b82f9418e6fb85055fd1a48191725c15ba498c8ef6404a7a42c350f61c2c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1902939983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83469092d0034c5e48e44667a94af4371623664ccee49b9c645dc1fb6afe16a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 05:09:35 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 12 Jan 2023 05:09:36 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 12 Jan 2023 05:10:00 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 13 Jan 2023 00:17:12 GMT
ENV JAVA_VERSION=21-ea+5
# Fri, 13 Jan 2023 00:17:12 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/5/GPL/openjdk-21-ea+5_windows-x64_bin.zip
# Fri, 13 Jan 2023 00:17:13 GMT
ENV JAVA_SHA256=c9fbb10f642e2256f652d9ae955c0ddf2888348ac952217d005d85703711d602
# Fri, 13 Jan 2023 00:18:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 13 Jan 2023 00:18:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fe1d317f0927d209417077d671ba0fb8e3b7ff9c583727da819f0d16252e80`  
		Last Modified: Thu, 12 Jan 2023 05:23:04 GMT  
		Size: 367.5 KB (367453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6807e3d75deac242f3cfe460728c148c2f68e1d8366ad3f0358a3c9237042b6`  
		Last Modified: Thu, 12 Jan 2023 05:23:04 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbe0b64cf9fa2560a38a4c1a75582463f16f8e35e9776b14d87cd13167e4281`  
		Last Modified: Thu, 12 Jan 2023 05:23:04 GMT  
		Size: 320.0 KB (320032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b5ac4713820eb261563d1fe2069bf302d7b7d7d871469f45ab4a9a7f498d6f`  
		Last Modified: Fri, 13 Jan 2023 03:19:34 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b8319f12286006892cf3c15c5eb96edba1029f17186c29461b064b1b78632e`  
		Last Modified: Fri, 13 Jan 2023 03:19:34 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41ba3700464142b6879214949fcf4c9c71b6ae6f5f0326cef6c494c132dc780`  
		Last Modified: Fri, 13 Jan 2023 03:19:34 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f24203ae7b5d1be6726859ed0ada115df9dcd0bc51df3cb59ec5d2ed740341`  
		Last Modified: Fri, 13 Jan 2023 03:19:58 GMT  
		Size: 194.3 MB (194300110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dfaea64713639ec407735b1aba808238d4ada3ab16fc3b4ee98b5885bd85a37`  
		Last Modified: Fri, 13 Jan 2023 03:19:34 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
