## `openjdk:24-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:42e4e35367f46b5e491302bb9b05b8cb94ec11b5900e3bb052189b81580295dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `openjdk:24-jdk-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull openjdk@sha256:92e719a0f38236296a0958a7d915edf83f394d6a33ce2089698220db77ebf78f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2111222084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57381027f9cb25b9dc4d5307860cc486af46d5d3ef1b054aad4ad92e5d9a85d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Fri, 25 Oct 2024 23:57:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 25 Oct 2024 23:57:36 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 25 Oct 2024 23:57:37 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 25 Oct 2024 23:57:45 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 25 Oct 2024 23:57:46 GMT
ENV JAVA_VERSION=24-ea+21
# Fri, 25 Oct 2024 23:57:46 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/21/GPL/openjdk-24-ea+21_windows-x64_bin.zip
# Fri, 25 Oct 2024 23:57:47 GMT
ENV JAVA_SHA256=fadb0a1bfaab7f1299965f76ad4c30a3b4e9f2e7325c0f99ff51b4592e12903c
# Fri, 25 Oct 2024 23:58:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 25 Oct 2024 23:58:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ed3b2b2c3dd77056694156efa770a8b250467e4c3cf9f43f7e482aed1aa02b`  
		Last Modified: Fri, 25 Oct 2024 23:58:21 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555eb4088d5829d5bff5d449936fef100d4e6ba62193f77fe5753339dbb090c5`  
		Last Modified: Fri, 25 Oct 2024 23:58:21 GMT  
		Size: 487.7 KB (487674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b24333f336e1601b819fb8dff76bee7885ba55f8c69f106dcaecee0a6638d2b`  
		Last Modified: Fri, 25 Oct 2024 23:58:21 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c5a0b1e7d59a6873e8fddbaecb6bf0c575e2f608fccf072c4a19b74f919784`  
		Last Modified: Fri, 25 Oct 2024 23:58:21 GMT  
		Size: 329.7 KB (329700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ef7a7b0dc2547275914d045103d74d537653a784a16cfd74e6020f76a921d2`  
		Last Modified: Fri, 25 Oct 2024 23:58:19 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f67d7f7cf19a76a5f90b53250e947b7a82133551cd647cb5a6ac3ed1a39b283`  
		Last Modified: Fri, 25 Oct 2024 23:58:19 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8775c711d9aff48939ae8f9c07ad257cdfcc5f8d540211250ec1f07dbb17bbe`  
		Last Modified: Fri, 25 Oct 2024 23:58:19 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f134d2f1b45c52c4d69126aca14dac384ddbb0a6f437e67a8697b445a123605`  
		Last Modified: Fri, 25 Oct 2024 23:58:30 GMT  
		Size: 208.6 MB (208571660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aced454ff11b76f12149d52d9b99eccfe8448298e15cbb0cb62a11278a0320d`  
		Last Modified: Fri, 25 Oct 2024 23:58:19 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
