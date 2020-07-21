## `openjdk:16-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:bf9a7a03f6474dfff0bd1d899d5757c270ee6543eec9303072ee4b25f26537c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64

### `openjdk:16-windowsservercore-ltsc2016` - windows version 10.0.14393.3808; amd64

```console
$ docker pull openjdk@sha256:9e6ee2cb41e7f75a90b368b864ab772c66aadaf4ebc79a9846e5062e800115f5
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5954524510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613f79ba209b3a36b2e045ee8947a5e64563d00da28ec7fe93842368d3ad00aa`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jul 2020 18:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Jul 2020 16:57:52 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Tue, 21 Jul 2020 16:57:54 GMT
ENV JAVA_HOME=C:\openjdk-16
# Tue, 21 Jul 2020 17:02:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Tue, 21 Jul 2020 17:02:34 GMT
ENV JAVA_VERSION=16-ea+6
# Tue, 21 Jul 2020 17:02:35 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk16/6/GPL/openjdk-16-ea+6_windows-x64_bin.zip
# Tue, 21 Jul 2020 17:02:37 GMT
ENV JAVA_SHA256=8a1861dfe888d04ab06b21b350d284641b9504515c3ffdfd421b89666d756d63
# Tue, 21 Jul 2020 17:05:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 21 Jul 2020 17:05:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9a64f8d0454dba1fb133615caae6ab4d76b85b8be54102ee2ce5f7fd034edbff`  
		Last Modified: Tue, 14 Jul 2020 19:42:07 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecf5cd76cb63f861b644ea8339d6249d5372f121099524df379003e1bbb30d9`  
		Last Modified: Tue, 21 Jul 2020 17:37:06 GMT  
		Size: 9.9 MB (9859351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63530cffa1eb60604458a400041ef9cbdb94004186de71aa32a3a4bc08e8561d`  
		Last Modified: Tue, 21 Jul 2020 17:37:03 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfeb8a5d9ef6f3cada7404d604fb88f291e3e4ab57b78ebe38a6f9733d83881d`  
		Last Modified: Tue, 21 Jul 2020 17:37:06 GMT  
		Size: 5.4 MB (5366955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a3ccb1ac20f6d8d30e0f01a2784936608d096121b383e0c9dab887e3f20a35`  
		Last Modified: Tue, 21 Jul 2020 17:37:00 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fab818548b69ec677f30c723bd3e3b93613396b58d31a7484584a81eed937ee`  
		Last Modified: Tue, 21 Jul 2020 17:37:00 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a761fd75c27022c4cefe24f24d4122b9de1a9d9f629e48e03255f55089e75d`  
		Last Modified: Tue, 21 Jul 2020 17:37:00 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efbce89c2165ae08170ca6e4591ec97827bd4e65d8911dc691bb310d79032fda`  
		Last Modified: Tue, 21 Jul 2020 17:40:42 GMT  
		Size: 201.8 MB (201829457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935d4865e0a60fb95cc887e36705e2d44d75720530c2179a1f355298b0aad87a`  
		Last Modified: Tue, 21 Jul 2020 17:37:00 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
