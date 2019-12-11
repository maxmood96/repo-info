## `openjdk:jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:8cef039352c588eca019a148ea863bc9b45f6bf6e5c8b0906d01caeb12ea4a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `openjdk:jdk-windowsservercore-1809` - windows version 10.0.17763.914; amd64

```console
$ docker pull openjdk@sha256:399788bfd0f26e9bcbd45d21d0b7f0409392e51e7d9eae03d293fb89f214a145
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2412713152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8483aa9feb87af3230a51276395bf70582c78199600db8aa38f95e38c95c4ab4`
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
# Wed, 11 Dec 2019 18:51:52 GMT
ENV JAVA_HOME=C:\openjdk-13
# Wed, 11 Dec 2019 18:52:16 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 11 Dec 2019 18:52:17 GMT
ENV JAVA_VERSION=13.0.1
# Wed, 11 Dec 2019 18:52:18 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk13.0.1/cec27d702aa74d5a8630c65ae61e4305/9/GPL/openjdk-13.0.1_windows-x64_bin.zip
# Wed, 11 Dec 2019 18:52:20 GMT
ENV JAVA_SHA256=438a6920f1851b1eeb6f09f05d9f91c4423c6586f7a1a7ccbb19df76ea5901ee
# Wed, 11 Dec 2019 18:54:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2019 18:54:17 GMT
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
	-	`sha256:1a02e96d188099e521c1816a5a7c259bc4f4eff8a3a7377b76b6e171efc4ae81`  
		Last Modified: Wed, 11 Dec 2019 20:02:48 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc4a834e50c3508cf10d0ac23853f32b8db8294825a472d9aca384706f996a1`  
		Last Modified: Wed, 11 Dec 2019 20:02:48 GMT  
		Size: 314.6 KB (314577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a42d4ff2612f7baba32c6dd2f5f97f1a9a4f6f3f8e3f8694c809078cfaf479e`  
		Last Modified: Wed, 11 Dec 2019 20:02:45 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:284f05750e029543fb0bf6fed04982d956d306a7d83d171364f669f8414e3951`  
		Last Modified: Wed, 11 Dec 2019 20:02:45 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f531a850a32f30986f4be1a77d5cb5a5d25f9d02280b3a4bc365070832dac9`  
		Last Modified: Wed, 11 Dec 2019 20:02:45 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e247ac80f46f350ffc0649223d5706842e558b46bbf1da3fc017b178503590`  
		Last Modified: Wed, 11 Dec 2019 20:03:08 GMT  
		Size: 191.5 MB (191509522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a10eeb028af24e6b3902f04eb5b933c9f5adf151a9a952b97fec86bce62e1166`  
		Last Modified: Wed, 11 Dec 2019 20:02:45 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
