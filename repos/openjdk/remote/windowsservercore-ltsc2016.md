## `openjdk:windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:02b8b2f68cf0dd471a16620fcb7bb717589380022f65676a69520bb897996db9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3986; amd64

### `openjdk:windowsservercore-ltsc2016` - windows version 10.0.14393.3986; amd64

```console
$ docker pull openjdk@sha256:2947da3585e7bcc93a893d098005063fe11da4860109e4307a311028aa511aa2
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5962353287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb38954a244f58a71b63a281e50bb1cbe5cf7d32d4beb217057d8c40225becb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 12:31:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 17:42:04 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 14 Oct 2020 17:49:57 GMT
ENV JAVA_HOME=C:\openjdk-15
# Wed, 14 Oct 2020 17:51:12 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 14 Oct 2020 17:51:13 GMT
ENV JAVA_VERSION=15
# Wed, 14 Oct 2020 17:51:15 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk15/779bf45e88a44cbd9ea6621d33e33db1/36/GPL/openjdk-15_windows-x64_bin.zip
# Wed, 14 Oct 2020 17:51:15 GMT
ENV JAVA_SHA256=764e39a71252a9791118a31ae56a4247c049463bda5eb72497122ec50b1d07f8
# Wed, 14 Oct 2020 17:53:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 14 Oct 2020 17:53:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e300a13db0fbbf48a676ace9db3b0de292c825dfa01e6d82979d96ebc23d3675`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48f75bae068c25f8a226647b58c0be2010ed0c8cd6921bdc70e67addcbf5a03`  
		Last Modified: Wed, 14 Oct 2020 18:30:55 GMT  
		Size: 9.9 MB (9914428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432a0b2b655f368cca05a6b997d7dcc2ad49cb5f07253b6518faa65ce3b25c3c`  
		Last Modified: Wed, 14 Oct 2020 18:35:45 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645488ec1053a7b7a616c7ff1d3067b19ce2152f82dff02bb47f7287b08c8c75`  
		Last Modified: Wed, 14 Oct 2020 18:35:48 GMT  
		Size: 9.8 MB (9849910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179bc44e1bd95d9d118a2547de317082bcd99a6f5c91effe100f13470eddabe4`  
		Last Modified: Wed, 14 Oct 2020 18:35:41 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ac7f7a5e18ec0a6fa6efa118aa6550b834acb75c83a1990b9ee35ac8e4c20f`  
		Last Modified: Wed, 14 Oct 2020 18:35:41 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3896092c313fe04d8d67854680b44875ce4ba6105da011bbbb8a8b3148eef116`  
		Last Modified: Wed, 14 Oct 2020 18:35:41 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b10bb939b2b24b77bae8a317e008c13381d63694748d370d63301599ab8794`  
		Last Modified: Wed, 14 Oct 2020 18:36:10 GMT  
		Size: 201.2 MB (201230464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2128663b2a71cc507c025d81cc2bdd410f88f29c112f6d67a6192bf318a72e59`  
		Last Modified: Wed, 14 Oct 2020 18:35:41 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
