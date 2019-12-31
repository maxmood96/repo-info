## `openjdk:15-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:89348924bcd2b303e1baed1c89dbb987218a80525c132f582dbf22ad22ad217d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `openjdk:15-jdk-windowsservercore-1809` - windows version 10.0.17763.914; amd64

```console
$ docker pull openjdk@sha256:e6c9dc50496f50e22ebebac4689a49f2b5a0b264970720bd614311332143e8b8
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2415475029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7a8a2b2cb98875a4aea44cf77f7f21464d6db84ede0982f6a130fc34f07cb0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 29 Nov 2019 04:34:15 GMT
RUN Install update 1809-amd64
# Tue, 10 Dec 2019 21:34:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 18:41:29 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Thu, 19 Dec 2019 01:22:00 GMT
ENV JAVA_HOME=C:\openjdk-15
# Thu, 19 Dec 2019 01:22:27 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Mon, 30 Dec 2019 23:22:38 GMT
ENV JAVA_VERSION=15-ea+3
# Mon, 30 Dec 2019 23:22:39 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/3/GPL/openjdk-15-ea+3_windows-x64_bin.zip
# Mon, 30 Dec 2019 23:22:40 GMT
ENV JAVA_SHA256=f5fa522efcff995e783f91a964103bced301c4d4deb6ab3bd231367f0e14a30a
# Mon, 30 Dec 2019 23:25:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 30 Dec 2019 23:25:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:faf31ee0aa3d3c60a38dd03c7554d632065cef50eab052ef1444590786249d07`  
		Size: 681.6 MB (681618026 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e147f14e0d6a9cbd5261162dea8f3aac7a34db5d9f6a587a9aac6b88722a2da4`  
		Last Modified: Tue, 10 Dec 2019 22:07:34 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0c4a671756d1396180ecdf66a8d6708b4290b154606229618d94780b6ab6b3`  
		Last Modified: Wed, 11 Dec 2019 19:58:31 GMT  
		Size: 4.6 MB (4578585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7042a384d9a06800f72ef1e12158b017c64448477780c16789eca5116506a547`  
		Last Modified: Thu, 19 Dec 2019 01:35:21 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a7c43af5e831564c83a66de8ab18e497dea4bfc0028a6dee76433bef5dffff2`  
		Last Modified: Thu, 19 Dec 2019 01:35:22 GMT  
		Size: 318.1 KB (318105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f66443aa6ee3a74d73af0acb956bca642e1010e0a0b43d305926c08954127a7`  
		Last Modified: Tue, 31 Dec 2019 00:12:39 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b76ebf3a5f66c0ab68e0c2f886867ef624075834d76d98bafffbfdfdc3edc2b`  
		Last Modified: Tue, 31 Dec 2019 00:12:38 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739b6bc985d8ff07100db9007803b3c39a030f7063f18710eb99c157edc1780c`  
		Last Modified: Tue, 31 Dec 2019 00:12:38 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077080cf7a86693f4451dc2664511481673c4d7e0435681d29ab447f80ab36f9`  
		Last Modified: Tue, 31 Dec 2019 00:13:30 GMT  
		Size: 194.3 MB (194267836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7886ba841b0e53f649b91e3187eec62a0303c7677c2cb01f5f810cb75f4c5d90`  
		Last Modified: Tue, 31 Dec 2019 00:12:38 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
