## `openjdk:17-ea-windowsservercore`

```console
$ docker pull openjdk@sha256:90dfb9615938750c43d97c458fe600dc7835a351aa9c3712fe0295e7de45e97c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1817; amd64
	-	windows version 10.0.14393.4283; amd64

### `openjdk:17-ea-windowsservercore` - windows version 10.0.17763.1817; amd64

```console
$ docker pull openjdk@sha256:92c51b28cd4e1db5c1bc0cb47d9d97410cf14263c8631c123114e337b35c0abf
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2656846270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f4e4bff4679e46a6abd6dd659b3fe9d013d2a410715fba270d6d2680a3b5e2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 27 Feb 2021 09:32:06 GMT
RUN Install update 1809-amd64
# Wed, 10 Mar 2021 13:08:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Mar 2021 17:43:17 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 Mar 2021 17:43:18 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 10 Mar 2021 17:43:43 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 02 Apr 2021 18:27:27 GMT
ENV JAVA_VERSION=17-ea+16
# Fri, 02 Apr 2021 18:27:28 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk17/16/GPL/openjdk-17-ea+16_windows-x64_bin.zip
# Fri, 02 Apr 2021 18:27:29 GMT
ENV JAVA_SHA256=379902e2bc2ba208dde73bd389a92ad85903ec047352eb4dd06d93dc84e772ad
# Fri, 02 Apr 2021 18:28:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 02 Apr 2021 18:28:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ff1512f88ecd4ff0a91ade34d43733c48834433e35f062f80e6e70d706f8d73`  
		Size: 743.2 MB (743201590 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ebe61daec6d671bc2c1c6fe61ac9825fb552e9cef3672d0a7dbec719d125ae64`  
		Last Modified: Wed, 10 Mar 2021 13:21:09 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5a565fbc6dee6b0e5a6252ca763370a8d3521925db3d451dd6e7ec0efc1b07`  
		Last Modified: Wed, 10 Mar 2021 18:28:58 GMT  
		Size: 9.5 MB (9457788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce65a7afaa8a843f59f4e00b2cde68e50c25b4931a7ce73ff3b55438bd7742bf`  
		Last Modified: Wed, 10 Mar 2021 18:28:54 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2620c5b70d10c22e375ff81365a7e5c381fd1cb523ae714bcb824d42a5a46c51`  
		Last Modified: Wed, 10 Mar 2021 18:28:55 GMT  
		Size: 334.1 KB (334116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0cdfa25d6a5e2416661e55ca305b2e202e593de0484bb65c2ee78c6a147356`  
		Last Modified: Fri, 02 Apr 2021 18:38:49 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e17895d89b63d7d2a2c110eeabcec159b69c12f1ef99e11de89c0c3d1e1ca33`  
		Last Modified: Fri, 02 Apr 2021 18:38:49 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8625c6299fa1f3c09d742dffee70db1995838474ccb84993295de4c731f44c15`  
		Last Modified: Fri, 02 Apr 2021 18:38:49 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2b54cf13ea676660d96ec5067791d8012a700937e4395ae74f4bf8674cb1e2`  
		Last Modified: Fri, 02 Apr 2021 18:39:09 GMT  
		Size: 185.5 MB (185511424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911d3fd4c45161e4bc795c4bc2f78641f3b1381bf71c84c224e00f74564aff74`  
		Last Modified: Fri, 02 Apr 2021 18:38:49 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-ea-windowsservercore` - windows version 10.0.14393.4283; amd64

```console
$ docker pull openjdk@sha256:067bbf12d39e74d9a96bf7a6418262353e7059ece20bd4091a2957695c05052d
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (6003636399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc9a5f960490b60d5afcbcf06064e41c4d449c98576723b9d8c7f7ef82427c3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Mar 2021 18:02:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Mar 2021 13:42:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Mar 2021 17:46:47 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 Mar 2021 17:46:48 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 10 Mar 2021 17:48:10 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 02 Apr 2021 18:28:44 GMT
ENV JAVA_VERSION=17-ea+16
# Fri, 02 Apr 2021 18:28:45 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk17/16/GPL/openjdk-17-ea+16_windows-x64_bin.zip
# Fri, 02 Apr 2021 18:28:47 GMT
ENV JAVA_SHA256=379902e2bc2ba208dde73bd389a92ad85903ec047352eb4dd06d93dc84e772ad
# Fri, 02 Apr 2021 18:31:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 02 Apr 2021 18:31:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30bda99601c5cbd3b2118409f401852ea648e2319bd81518723e476b28d764c5`  
		Size: 1.7 GB (1726924885 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:76680da9dc6db108ddf2e353c494b45e8486a6751619a13ed8fb3ad64b9a16e9`  
		Last Modified: Wed, 10 Mar 2021 14:06:08 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acde2be15530c0b8fb3d57db65ee292b515e7911dbd4b55109e48dbd55c28539`  
		Last Modified: Wed, 10 Mar 2021 18:33:09 GMT  
		Size: 10.2 MB (10177023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db8e176190222d82d02bad5231e85a830ea393cb1c2afab482c0ab55ba9bc304`  
		Last Modified: Wed, 10 Mar 2021 18:32:58 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349d082f4a3335d41d13ed8c56f2b3e9212291e7de2c29a3a7c2bf5d5ed2f7ab`  
		Last Modified: Wed, 10 Mar 2021 18:32:59 GMT  
		Size: 5.6 MB (5605916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64cab78264730fc132967585a854da3f79f56e94a0098bc31db58a1ff6bfc72f`  
		Last Modified: Fri, 02 Apr 2021 18:39:32 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185f19cece2f479b102993a7146ae581eecebad6435ee5e9c3db506eb5767677`  
		Last Modified: Fri, 02 Apr 2021 18:39:32 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0103076d86a9e20707c8085fbfd43709e70ebf1f7fa25722bb481847f6606991`  
		Last Modified: Fri, 02 Apr 2021 18:39:32 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c9b846a4162f913a21b14318f54c2a5113fa03ed28931617dc7c4ac74e9fef`  
		Last Modified: Fri, 02 Apr 2021 18:39:53 GMT  
		Size: 190.9 MB (190934365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35717bbac03964f9781cfd37acdd4a1c8a687c7729d79d6d58d606f035aa1c5`  
		Last Modified: Fri, 02 Apr 2021 18:39:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
