## `openjdk:windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:77b1b5a40828a4146215e68dc7e1a264af0e5a169f5ae655d1710fdf1aa7b0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4283; amd64

### `openjdk:windowsservercore-ltsc2016` - windows version 10.0.14393.4283; amd64

```console
$ docker pull openjdk@sha256:b3c8477739fd741967e9fa89d0393ac05f311925cd7dfd36fa829c63e7d1596d
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (6002899763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3eac6ee8f913fbe0030bb0cbbb33a3477e5d85f77a27c49ae5a33628b25bac`
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
# Wed, 10 Mar 2021 17:53:59 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 10 Mar 2021 17:55:23 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 10 Mar 2021 17:55:24 GMT
ENV JAVA_VERSION=16
# Wed, 10 Mar 2021 17:55:26 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk16/7863447f0ab643c585b9bdebf67c69db/36/GPL/openjdk-16_windows-x64_bin.zip
# Wed, 10 Mar 2021 17:55:27 GMT
ENV JAVA_SHA256=a78bdeaad186297601edac6772d931224d7af6f682a43372e693c37020bd37d6
# Wed, 10 Mar 2021 17:57:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 10 Mar 2021 17:57:38 GMT
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
	-	`sha256:dc92118a3beb0eaf5efb299feb4417df262dbb493f2f1144f58a6dcf9c0ff235`  
		Last Modified: Wed, 10 Mar 2021 18:35:50 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76e1665f03606114a9dbcce77e7e379404807a77e1a3d7b9aebc51b3548a46c`  
		Last Modified: Wed, 10 Mar 2021 18:35:51 GMT  
		Size: 5.6 MB (5605754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9003a88704cd899ce2fe0c04c750e268fa4c4ef54c638f3e85a198104ca00b7b`  
		Last Modified: Wed, 10 Mar 2021 18:35:47 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4778db5762af3a85c92a5ad115a3d7c41434d14a5f244ded3d47779e48ba611`  
		Last Modified: Wed, 10 Mar 2021 18:35:47 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ef7ba22972e0d375f98fb14246062a0ce4e4b176dfce2afed55e6fc528a054`  
		Last Modified: Wed, 10 Mar 2021 18:35:47 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca6dc3aad53ef90c054e7b4fe9f338fe4d5dec0f14aecab16552876893cb314`  
		Last Modified: Wed, 10 Mar 2021 18:36:11 GMT  
		Size: 190.2 MB (190197717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68aabf0dac2388555d266c9d14b5c7ad227db400c7c2bb2bf75f04e3923316ee`  
		Last Modified: Wed, 10 Mar 2021 18:35:47 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
