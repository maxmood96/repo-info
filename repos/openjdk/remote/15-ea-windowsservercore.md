## `openjdk:15-ea-windowsservercore`

```console
$ docker pull openjdk@sha256:287938a1992c04cbc032f54dbf99a2373de5f281fac8960e39eec53f35fbb144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64
	-	windows version 10.0.14393.3384; amd64

### `openjdk:15-ea-windowsservercore` - windows version 10.0.17763.914; amd64

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

### `openjdk:15-ea-windowsservercore` - windows version 10.0.14393.3384; amd64

```console
$ docker pull openjdk@sha256:c74112b4b7af5a4c6e3dc8d9d0831355fc54c10f9c1c80281fbffd2a403af910
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5932783345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1213b6301297f771a29bd644c9d22ad46dbbfca80c2db04a75e05a3ed2a56c9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 00:35:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 18:45:32 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Thu, 19 Dec 2019 01:24:42 GMT
ENV JAVA_HOME=C:\openjdk-15
# Thu, 19 Dec 2019 01:25:54 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Mon, 30 Dec 2019 23:25:27 GMT
ENV JAVA_VERSION=15-ea+3
# Mon, 30 Dec 2019 23:25:28 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/3/GPL/openjdk-15-ea+3_windows-x64_bin.zip
# Mon, 30 Dec 2019 23:25:29 GMT
ENV JAVA_SHA256=f5fa522efcff995e783f91a964103bced301c4d4deb6ab3bd231367f0e14a30a
# Mon, 30 Dec 2019 23:28:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 30 Dec 2019 23:28:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:530e4240d4261ce165890648d1df6230dc4f9ce5df2e6cf9f0d5876694c3d4f0`  
		Last Modified: Wed, 11 Dec 2019 01:14:39 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ba7ecb82646b9454a7a416c149a513479fd0ab29aaa2dfbe96281b62668931`  
		Last Modified: Wed, 11 Dec 2019 19:59:59 GMT  
		Size: 5.4 MB (5365131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e59ee70e849f790ad2dd4da52ae1d8b3154ca924aed71fdda94b3c19fa0412`  
		Last Modified: Thu, 19 Dec 2019 01:36:45 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb24f179a5c79b0fa807327ebc5529bab3227974c63983f6c404a19b49cc380`  
		Last Modified: Thu, 19 Dec 2019 01:36:47 GMT  
		Size: 5.4 MB (5350253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1063fe04b78e4fb10e2f6474b6e3fcdf39dec745538a5b9918155855713d0e10`  
		Last Modified: Tue, 31 Dec 2019 00:14:32 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102d08220233e5acc66d446459223ebe40b8166de5a12028ed2c0f8c1d069eb3`  
		Last Modified: Tue, 31 Dec 2019 00:14:33 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffdbf44cdc6dfb33e41cc418a4ab9c14e355267b359e54f37fafcab897c2874`  
		Last Modified: Tue, 31 Dec 2019 00:14:32 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7361d70514a2aab916c8646d8da123e66f101fa79b2fd2648ef0f580eb86abc`  
		Last Modified: Tue, 31 Dec 2019 00:15:06 GMT  
		Size: 199.4 MB (199356954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9402d2f4950983fc280544c08749163a28e95103d21977859d751c518571d1ec`  
		Last Modified: Tue, 31 Dec 2019 00:14:32 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
