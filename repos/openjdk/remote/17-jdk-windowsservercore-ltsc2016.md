## `openjdk:17-jdk-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:896fc4118d3a5cf0c26cc2d6a972dd14fd2fe2e28e2901711d9acca4a4134370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4225; amd64

### `openjdk:17-jdk-windowsservercore-ltsc2016` - windows version 10.0.14393.4225; amd64

```console
$ docker pull openjdk@sha256:82c45b0184aee8793d1bc66434abeb3097893954e13b92c65b92789e6c0cbe97
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (6002011505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d184d7b07e13934caccc63315b4058cbff22199f85d9c7b7064222d74934f2b8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Jan 2021 18:11:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Feb 2021 13:17:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Feb 2021 16:42:35 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 Feb 2021 16:42:36 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 10 Feb 2021 16:43:46 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 03 Mar 2021 23:17:06 GMT
ENV JAVA_VERSION=17-ea+12
# Wed, 03 Mar 2021 23:17:07 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk17/12/GPL/openjdk-17-ea+12_windows-x64_bin.zip
# Wed, 03 Mar 2021 23:17:08 GMT
ENV JAVA_SHA256=96f742aa0e6918189a08c2788df7a838d1e861a7ed981ce007acfcaba6d8effa
# Wed, 03 Mar 2021 23:19:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 03 Mar 2021 23:19:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:62c48323ed8ac695b8cbe0ecedcc28ba185a234673ad9241df2b151dd00f9181`  
		Size: 1.7 GB (1725027107 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c03f1c41641d4a4cf6906dee9a590ee67135d926dddab80cfef993cae745a38a`  
		Last Modified: Wed, 10 Feb 2021 13:41:36 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852b6d2d8c5b49e04837d97a06dfd545d620e2355d40bc0014a563f58a5c11c2`  
		Last Modified: Wed, 10 Feb 2021 17:16:55 GMT  
		Size: 10.2 MB (10165560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed9c4a33cf4184ec2758f116995a1883c4e175af9c2087923a3e8073b0380068`  
		Last Modified: Wed, 10 Feb 2021 17:16:51 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27a6f1b8e5829537ed39d3d76ff8d153d99087fc769b430652f6c539854ea31`  
		Last Modified: Wed, 10 Feb 2021 17:16:52 GMT  
		Size: 5.6 MB (5613663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8693f02145bfe2062e3b0183f03046983405d52345835482e76cb26390c9ca2`  
		Last Modified: Wed, 03 Mar 2021 23:27:17 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cd70599157b65761fdbfd3358b09a26fdf54b317e5fc298df2d5dc881193c7`  
		Last Modified: Wed, 03 Mar 2021 23:27:18 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90593a042701ca72a8d5473ef029af4bffb4eda2fbd80c2870988e70d6b2c2e`  
		Last Modified: Wed, 03 Mar 2021 23:27:18 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740e8caa1eae8d70a60a92a5cf5c75e37be1557249af2e64ff60c07fc0866cba`  
		Last Modified: Wed, 03 Mar 2021 23:27:40 GMT  
		Size: 191.2 MB (191210848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7e955879b813199acd98bae4db2e128ab67642c3d7d0005719ec027d1cc8c3`  
		Last Modified: Wed, 03 Mar 2021 23:27:18 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
