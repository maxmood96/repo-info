## `openjdk:14-jdk-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:ec29499e1dd48543bcc9e0400dd30144082f3ea838fcb24130b3ea8ddb5e2394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64

### `openjdk:14-jdk-windowsservercore-ltsc2016` - windows version 10.0.14393.3384; amd64

```console
$ docker pull openjdk@sha256:ad1f54eceefdf2812908ec5995c3f52ea9a073936738bcff2c1662bd6f87f9dc
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5937091136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133ca6fea7e137cb049fac9723a83671c9f1bacb4c4341c12a740734d952bcf0`
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
# Wed, 11 Dec 2019 18:45:34 GMT
ENV JAVA_HOME=C:\openjdk-14
# Wed, 11 Dec 2019 18:46:45 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Tue, 31 Dec 2019 00:03:23 GMT
ENV JAVA_VERSION=14-ea+29
# Tue, 31 Dec 2019 00:03:24 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk14/29/GPL/openjdk-14-ea+29_windows-x64_bin.zip
# Tue, 31 Dec 2019 00:03:25 GMT
ENV JAVA_SHA256=083c06147216ce2163d4e6e0fdbad095c35769bf98f8020b20801660b22c38e0
# Tue, 31 Dec 2019 00:06:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 31 Dec 2019 00:06:31 GMT
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
	-	`sha256:1d3eaf34da6eedc1087e3f8e21af3d549b7e85b0e1f93c4275a7569076c67f12`  
		Last Modified: Wed, 11 Dec 2019 19:59:55 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef9e5659d610b4fc02e08dc2d00b5d97d8f9e0d0ca73681a31acbef3f3e00a5`  
		Last Modified: Wed, 11 Dec 2019 19:59:58 GMT  
		Size: 5.3 MB (5345980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84af87ab9d1b71b1e6131ed1c53df8704170febb2941814d8da2fd094e5d314`  
		Last Modified: Tue, 31 Dec 2019 00:24:14 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ced9aed42717ad7915fce285edf80a961e89907cb0f3350fb5d818c0ad0315`  
		Last Modified: Tue, 31 Dec 2019 00:24:15 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf493bad33edd3fa7fe0113d737011f9d7adb69aecbd7816c14126d99980e44`  
		Last Modified: Tue, 31 Dec 2019 00:24:14 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e359947fffb1860e53d921df990ef484390775bbfb5f0e907c2eaa7e154b2def`  
		Last Modified: Tue, 31 Dec 2019 00:24:39 GMT  
		Size: 203.7 MB (203668980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a80814be613268cbfccb3d5172b591bde112ffb1eae5fc53607e3111cf78a8`  
		Last Modified: Tue, 31 Dec 2019 00:24:14 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
